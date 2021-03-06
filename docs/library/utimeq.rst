:mod:`utimeq` -- heap queue with times
======================================

.. module:: utimeq
   :synopsis: heap queue with times

.. admonition:: Difference to CPython
   :class: attention

   This is a MicroPython specific module.  It's based on :mod:`python:heapq` but
   its implementation is more specialized than that, and it's not possible to
   use list operations like indexing on it.

This module uses the heap queue algorithm (priority queue algorithm) to create
a heap queue where entries are popped based on which has the earliest time.

Classes
-------

.. class:: utimeq(n)

   Create a utimeq heap queue with space for n entries.  This size is static,
   and an attempt to push too many entries onto it will throw an IndexError with
   message 'queue overflow'.

   The queue sorts itself by entries' `time` parameters, and then by the order
   in which entries were pushed for entries with equal times.  So entries with
   lower `time` parameters get popped first, and for entries with the same `time`
   the first only that was pushed gets popped first.

   The heap queue can be tested for non-emptiness with "if(heap)".

   .. method:: push(time, obj, userdata)

      Push an entry onto the heap queue.

      * The `time` parameter should be a number of ticks (see the utime module)
        compatible with ``utime.ticks_diff()``.

      * The `obj` and `userdata` parameters are not used internally, so the user
        can set them to anything.  (The underlying MicroPython code suggests a
        callback and its arguments.)

   .. method:: pop(list)

      Takes the entry with lowest `time` off the heap queue.  Populates the
      first three items of the given list (which must already exist) with:

      * The entry's `time`.

      * The entry's `obj`.

      * The entry's `userdata`.

      Returns None.

   .. method:: peektime()

      Returns the `time` of the current top item (i.e. the one that will be
      popped next) but without popping it.



