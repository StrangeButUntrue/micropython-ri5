:mod:`system` -- system module
==============================

.. module:: system
   :synopsis: system module

Module containing a lot of high-level concepts, but no obvious theme beyond
that.

Classes `system.callbacks.Callbacks`, `system.display.DisplayWrapper`,
`system.move.Movement`, `system.motors.Motors`, `system.sound.SoundWrapper`
have aliases in the main namespace for convenience.

Constants
---------
.. data:: system

   Reference to the main System object.

System Class
------------

.. class:: System(???)

   ???

   .. method:: reset(???)

      ???

Submodules
----------

.. toctree::
   :maxdepth: 1

   system.callbacks.rst
   system.motors.rst
   system.motorwrapper.rst
   system.sound.rst
   system.move.rst
   system.movewrapper.rst
   system.abstractwrapper.rst
   system.display.rst

Imports
-------
* Module `hub`
* Function `event_loop.get_event_loop`


Raw module data
---------------

::

    object <module 'system.callbacks' from 'system/callbacks/__init__.mpy'> is of type module
      hub -- <module 'hub'>
      mp_schedule -- <function>
      BT_VCP -- BT_VCP(0)
      ConnectionCallbacks -- <class 'ConnectionCallbacks'>
      error_handler -- <ErrorHandler object at 2002c090>
      ButtonCallbacks -- <class 'ButtonCallbacks'>
      PortCallbacks -- <class 'PortCallbacks'>
      customcallbacks -- <module 'system.callbacks.customcallbacks' from 'system/callbacks/customcallbacks.mpy'>
      CallbackHandler -- <class 'CallbackHandler'>
      USB_VCP -- USB_VCP(0)
      Callbacks -- <class 'Callbacks'>
      notify_button_event -- <function notify_button_event at 0x20024ec0>
      CustomSensorCallbackManager -- <class 'CustomSensorCallbackManager'>
    object <class 'Callbacks'> is of type type
      reset -- <function reset at 0x2002ed00>
      __module__ -- system.callbacks
      hard_reset -- <function hard_reset at 0x2002ece0>
      __init__ -- <function __init__ at 0x2002ecf0>
    object <class 'ConnectionCallbacks'> is of type type
      __uch -- <function __uch at 0x2002fa50>
      __module__ -- system.callbacks
      check_state -- <function check_state at 0x2002fa10>
      __init__ -- <function __init__ at 0x2002fa20>
    object <class 'ButtonCallbacks'> is of type type
      hard_reset -- <function hard_reset at 0x2002f980>
      reset -- <function reset at 0x2002fa30>
      __init__ -- <function __init__ at 0x2002f970>
      __getitem__ -- <function __getitem__ at 0x2002f990>
      register_rpc_handlers -- <function register_rpc_handlers at 0x2002f960>
      __module__ -- system.callbacks
    object <class 'PortCallbacks'> is of type type
      reset -- <function reset at 0x2002fb70>
      hard_reset -- <function hard_reset at 0x2002fc30>
      __init__ -- <function __init__ at 0x2002fb80>
      init_attach -- <function init_attach at 0x2002fc20>
      __getitem__ -- <function __getitem__ at 0x2002fc10>
      __module__ -- system.callbacks
    object <class 'CallbackHandler'> is of type type
      reset -- <function reset at 0x2002fd10>
      register_persistent -- <function register_persistent at 0x2002fc60>
      __module__ -- system.callbacks
      hard_reset -- <function hard_reset at 0x2002fd30>
      __init__ -- <function __init__ at 0x2002fcf0>
      register_single -- <function register_single at 0x2002fd00>
      register -- <function register at 0x2002fd20>
      callback -- <function callback at 0x2002fd40>

    object <module 'system.callbacks.customcallbacks' from 'system/callbacks/customcallbacks.mpy'> is of type module
      const -- <function>
      CustomSensorCallbackManager -- <class 'CustomSensorCallbackManager'>
      get_event_loop -- <function get_event_loop at 0x2001ca30>
      utime -- <module 'utime'>
      get_sensor_value -- <function get_sensor_value at 0x20021f20>
      LPF2_FLIPPER_FORCE -- 63
    object <class 'CustomSensorCallbackManager'> is of type type
      until_force_bumped -- <generator>
      until_changed -- <generator>
      wait_until_less_than -- <function wait_until_less_than at 0x2002f7c0>
      _start_test_task -- <function _start_test_task at 0x2002f830>
      until_less_than -- <generator>
      is_less_than -- <staticmethod>
      __init__ -- <function __init__ at 0x2002f680>
      did_change -- <staticmethod>
      clear_tasks -- <function clear_tasks at 0x2002f710>
      until -- <generator>
      wait_until_force_bumped -- <function wait_until_force_bumped at 0x2002f7a0>
      remove_task -- <function remove_task at 0x2002f840>
      wait_until_changed -- <function wait_until_changed at 0x2002f810>
      __module__ -- system.callbacks.customcallbacks
      _active_tasks -- []
      did_bump -- <staticmethod>

    object <module 'system.motors' from 'system/motors.mpy'> is of type module
      Motors -- <class 'Motors'>
      hub -- <module 'hub'>
      _PORT_TO_IDX -- ['A', 'B', 'C', 'D', 'E', 'F']
      MotorWrapper -- <class 'MotorWrapper'>
      PORTS -- {'C': Port(C), 'B': Port(B), 'D': Port(D), 'E': Port(E), 'A': Port(A), 'F': Port(F)}
    object <class 'Motors'> is of type type
      register_port_callback_handlers -- <function register_port_callback_handlers at 0x20031bb0>
      on_port -- <function on_port at 0x20031b80>
      is_motor -- <function is_motor at 0x20031bc0>
      _update -- <function _update at 0x20031ba0>
      wrappers -- {}
      __module__ -- system.motors

    object <module 'system.motorwrapper' from 'system/motorwrapper.mpy'> is of type module
      FLOAT -- 0
      MotorWrapper -- <class 'MotorWrapper'>
      const -- <function>
      HOLD -- 2
      _counterclockwise -- <function _counterclockwise at 0x20031760>
      SUCCESS -- 0
      BRAKE -- 1
      AbstractWrapper -- <class 'AbstractWrapper'>
      _shortest -- <function _shortest at 0x20031770>
      _calc_degrees -- <function _calc_degrees at 0x20031740>
      _clockwise -- <function _clockwise at 0x20031750>
    object <class 'MotorWrapper'> is of type type
      run_for_degrees_async -- <generator>
      get -- <function get at 0x200319d0>
      run_to_position_async -- <generator>
      run_to_relative_position -- <function run_to_relative_position at 0x200319a0>
      motor -- None
      run_to_relative_position_async -- <generator>
      float -- <function float at 0x20031a50>
      preset -- <function preset at 0x200319e0>
      __module__ -- system.motorwrapper
      run_at_speed -- <function run_at_speed at 0x200317a0>
      run_for_degrees -- <function run_for_degrees at 0x200318b0>
      run_to_position -- <function run_to_position at 0x20031920>
      run_at_speed_async -- <generator>
      __init__ -- <closure>
      run_for_time -- <function run_for_time at 0x20031830>
      pwm -- <function pwm at 0x20031970>
      brake -- <function brake at 0x20031990>
      stop -- <function stop at 0x20031980>
      run_for_time_async -- <generator>
      hold -- <function hold at 0x200319c0>

    object <module 'system.sound' from 'system/sound.mpy'> is of type module
      hub -- <module 'hub'>
      note_to_frequency -- <function note_to_frequency at 0x200213f0>
      AbstractWrapper -- <class 'AbstractWrapper'>
      SoundWrapper -- <class 'SoundWrapper'>
    object <class 'SoundWrapper'> is of type type
      __module__ -- system.sound
      play -- <function play at 0x20033610>
      __init__ -- <closure>
      play_async -- <generator>
      beep_async -- <generator>
      beep -- <function beep at 0x200335b0>

    object <module 'system.move' from 'system/move.mpy'> is of type module
      Movement -- <class 'Movement'>
      PORTS -- {'C': Port(C), 'B': Port(B), 'D': Port(D), 'E': Port(E), 'A': Port(A), 'F': Port(F)}
      MoveWrapper -- <class 'MoveWrapper'>
    object <class 'Movement'> is of type type
      __module__ -- system.move
      _pairs -- {}
      on_pair -- <function on_pair at 0x20032ca0>

    object <module 'system.movewrapper' from 'system/movewrapper.mpy'> is of type module
      SUCCESS -- 0
      FLOAT -- 0
      AbstractWrapper -- <class 'AbstractWrapper'>
      MoveWrapper -- <class 'MoveWrapper'>
      HOLD -- 2
      BRAKE -- 1
      from_steering -- <function from_steering at 0x20032ff0>
    object <class 'MoveWrapper'> is of type type
      from_steering -- <function from_steering at 0x20032ea0>
      move_for_time -- <function move_for_time at 0x20032d30>
      float -- <function float at 0x20032e50>
      from_direction -- <function from_direction at 0x20032e80>
      move_for_time_async -- <generator>
      move_differential_speed_async -- <generator>
      __module__ -- system.movewrapper
      start_at_speeds -- <function start_at_speeds at 0x20032db0>
      start_at_powers -- <function start_at_powers at 0x20032d50>
      move_differential_speed -- <function move_differential_speed at 0x20032e20>
      is_valid -- <function is_valid at 0x20032c60>
      _direction_to_steering -- <function _direction_to_steering at 0x20032e70>
      __init__ -- <closure>
      brake -- <function brake at 0x20032e40>
      hold -- <function hold at 0x20032e60>
      pair -- None
      stop -- <function stop at 0x20032e10>
      move_at_power -- <function move_at_power at 0x20032e00>
      unpair -- <function unpair at 0x20032cd0>

    object <module 'system.abstractwrapper' from 'system/abstractwrapper.mpy'> is of type module
      const -- <function>
      INTERRUPTED -- 1
      get_event_loop -- <function get_event_loop at 0x2001ca30>
      SUCCESS -- 0
      AbstractWrapper -- <class 'AbstractWrapper'>
    object <class 'AbstractWrapper'> is of type type
      __init__ -- <function __init__ at 0x20031550>
      await_callback -- <generator>
      _callback -- <function _callback at 0x20031580>
      _register -- <function _register at 0x200315c0>
      cancel -- <function cancel at 0x200315e0>
      __module__ -- system.abstractwrapper

    object <module 'system.display' from 'system/display.mpy'> is of type module
      DisplayWrapper -- <class 'DisplayWrapper'>
      hub -- <module 'hub'>
      sanitize -- <function sanitize at 0x20033d00>
      SUCCESS -- 0
      AbstractWrapper -- <class 'AbstractWrapper'>
    object <class 'DisplayWrapper'> is of type type
      write -- <function write at 0x20033da0>
      show_async -- <generator>
      __module__ -- system.display
      show -- <function show at 0x20033de0>
      __init__ -- <closure>
      clear -- <function clear at 0x20033ee0>
      pixel -- <function pixel at 0x20033e60>
      write_async -- <generator>
