:mod:`event_loop` -- event_loop module
======================================

Event loop class - this seems to be the main scheduler on the Hub, called by
the `hub_runtime` module's `start()` procedure.

Raw module data
---------------

::

    object <module 'event_loop' from 'event_loop/__init__.mpy'> is of type module
      __path__ -- event_loop
      event_loop -- <module 'event_loop.event_loop' from 'event_loop/event_loop.mpy'>
      __name__ -- event_loop
      __file__ -- event_loop/__init__.mpy
      _EVENT_LOOP -- <EventLoop object at 20033160>
      EventLoop -- <class 'EventLoop'>
      get_event_loop -- <function get_event_loop at 0x2001ca30>
    object <module 'event_loop.event_loop' from 'event_loop/event_loop.mpy'> is of type module
      __name__ -- event_loop.event_loop
      ucollections -- <module 'ucollections'>
      EventLoop -- <class 'EventLoop'>
      __file__ -- event_loop/event_loop.mpy
      utimeq -- <module 'utimeq'>
      utime -- <module 'utime'>
    object <class 'EventLoop'> is of type type
      _discard -- <function _discard at 0x2001d570>
      __init__ -- <function __init__ at 0x2001d550>
      step -- <generator>
      __qualname__ -- EventLoop
      cancel -- <function cancel at 0x2001d510>
      call_soon -- <function call_soon at 0x2001ce40>
      run_forever -- <function run_forever at 0x2001d5c0>
      __module__ -- event_loop.event_loop
    object <EventLoop object at 20033160> is of type EventLoop
      _discard -- <function _discard at 0x2001d570>
      __init__ -- <function __init__ at 0x2001d550>
      step -- <generator>
      __qualname__ -- EventLoop
      cancel -- <function cancel at 0x2001d510>
      call_soon -- <function call_soon at 0x2001ce40>
      run_forever -- <function run_forever at 0x2001d5c0>
      __module__ -- event_loop.event_loop
