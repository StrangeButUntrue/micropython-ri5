:mod:`event_loop` -- event_loop module
======================================

.. module:: event_loop
   :synopsis: event_loop module

Home of the Event loop class - this seems to be the main scheduler on the Hub,
called by the `hub_runtime` module's `start()` procedure.  The EventLoop class
(along with the imports) seem to technically live inside an event_loop.event_loop
submodule, but the class is also available inside event_loop itself, so the
submodule isn't necessary to know about.

Functions
---------
.. function:: get_event_loop(???)

   ???

Constants
---------
.. data:: _EVENT_LOOP

   Reference to the main event loop object (type EventLoop).

Class EventLoop
---------------

.. class:: EventLoop(???)

   ???

   .. method:: _discard(???)

      ???

   .. method:: step(???)

      Generator function.  ???

   .. method:: cancel(???)

      ???

   .. method:: call_soon(???)

      ???

   .. method:: run_forever(???)

      ???

Imports
-------
* Module `ucollections`
* Module `utimeq`
* Module `utime`