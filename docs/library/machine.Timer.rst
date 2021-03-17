.. currentmodule:: machine
.. _machine.Timer:

class Timer -- control hardware timers
======================================

Hardware timers deal with timing of periods and events. Timers are perhaps
the most flexible and heterogeneous kind of hardware in MCUs and SoCs,
differently greatly from a model to a model. MicroPython's Timer class
defines a baseline operation of executing a callback with a given period
(or once after some delay), and allow specific boards to define more
non-standard behavior (which thus won't be portable to other boards).

See discussion of :ref:`important constraints <machine_callbacks>` on
Timer callbacks.

.. note::

    Memory can't be allocated inside irq handlers (an interrupt) and so
    exceptions raised within a handler don't give much information.  See
    :func:`micropython.alloc_emergency_exception_buf` for how to get around this
    limitation.

.. admonition:: Difference for RI5
   :class: attention

   This Timer class seems to be a bit broken in RI5, or at least it doesn't
   play nicely with the firmware - system failures that require pulling the battery
   and USB seem almost inevitable when trying to use ``init()``, ``deinit()`` or
   ``Timer.PERIODIC``.  (Basically the only thing that will work is a Timer
   that's initialized on construction, runs once and then is discarded.)
   Periodic Timers will work, but of course you can't shut them off successfully
   and they will still try to pop after the program has ended, causing (you
   guessed it) system failure.

   What you'd use instead seems a bit dependent on other requirements of your
   program - there's no obvious drop-in replacement for all circumstances.

Constructors
------------

.. class:: Timer(id=-1, ...)

   Construct a new virtual timer object. Id must equal -1 or be omitted.  If
   more arguments are provided, this runs the ``init()`` function with them,
   causing the timer to be started.  See ``init()`` below for a list.

   .. admonition:: Difference for RI5
      :class: attention

      Base MicroPython allows for various positive id values, specifying
      particular hardware timers.  The RI5 seems to only allow -1 for a virtual
      timer, and the number may alternatively be omitted entirely.

   In RI5 the only way to run ``init()`` successfully seems to be via this
   constructor - running the constructor with no extra parameters seems to
   leave the Timer in a weird half-initialized state that will cause system
   failure if you try to run ``init()`` or ``deinit()`` on it subsequently.

Methods
-------

.. method:: Timer.init(\*, mode=Timer.PERIODIC, period=-1, callback=None, freq=None)

   Initialise the timer. Example::

       tim.init(period=100)                         # periodic with 100ms period
       tim.init(mode=Timer.ONE_SHOT, period=1000)   # one shot firing after 1000ms

   Keyword arguments:

     - ``mode`` can be one of:

       - ``Timer.ONE_SHOT`` - The timer runs once until the configured
         period of the channel expires.
       - ``Timer.PERIODIC`` - The timer runs periodically at the configured
         frequency of the channel.

     - ``freq``
     - ``period``

       If specified, ``freq`` indicates the Hz frequency of when the timer will pop.
       Otherwise, ``period`` sets the number of milliseconds until the pop.  A
       negative or zero value period or frequency causes an immediate pop.

     - ``callback``

       Specifies a function to run when the timer pops.  This function must have
       one positional argument, which will be passed the Timer when it pops.

   .. admonition:: Difference for RI5
      :class: attention

      The STM32 port of Micropython (on which this seems to be based) has some
      extra possible arguments for this function for fuller control over how
      the Timer works.

   .. admonition:: Difference for RI5
      :class: attention

      Note as above - calling this function on any existing Timer on the RI5
      (whether it's stopped or started) causes system failure!  Use the
      constructor only, or give up on this class for the moment.

.. method:: Timer.deinit()

   Deinitialises the timer. Stops the timer.

   .. admonition:: Difference for RI5
      :class: attention

      Note as above - calling this function on any existing Timer on the RI5
      (whether it's stopped or started) causes system failure!  If you need a
      Timer that can be halted, you'll have to find something else for the
      moment.

Constants
---------

.. data:: Timer.ONE_SHOT = 1
          Timer.PERIODIC = 2

   Timer operating mode.
