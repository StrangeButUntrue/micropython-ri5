:mod:`runtime` -- runtime module
================================

.. module:: runtime
   :synopsis: runtime module

Contains mainly stack and virtual machine details needed to run programs on the
hub.

Raw module data
---------------

::

    object <module 'runtime' from 'runtime/__init__.mpy'> is of type module
      Stack -- <class 'Stack'>
      virtualmachine -- <module 'runtime.virtualmachine' from 'runtime/virtualmachine.mpy'>
      VirtualMachine -- <class 'VirtualMachine'>
      stack -- <module 'runtime.stack' from 'runtime/stack.mpy'>
      __path__ -- runtime
      __file__ -- runtime/__init__.mpy
      __name__ -- runtime
      dirty_dict -- <module 'runtime.dirty_dict' from 'runtime/dirty_dict.mpy'>
      vm_store -- <module 'runtime.vm_store' from 'runtime/vm_store.mpy'>
      MultiMotor -- <class 'MultiMotor'>
      timer -- <module 'runtime.timer' from 'runtime/timer.mpy'>
      multimotor -- <module 'runtime.multimotor' from 'runtime/multimotor.mpy'>
    object <module 'runtime.stack' from 'runtime/stack.mpy'> is of type module
      const -- <function>
      __name__ -- runtime.stack
      notify_stack_start -- <function notify_stack_start at 0x20024ed0>
      __file__ -- runtime/stack.mpy
      notify_stack_stop -- <function notify_stack_stop at 0x20024ee0>
      Stack -- <class 'Stack'>
    object <class 'Stack'> is of type type
      STATUS_RUNNING -- 10
      is_active -- <function is_active at 0x20036de0>
      STATUS_WAITING -- 30
      should_start -- <function should_start at 0x20036df0>
      _check_condition -- <generator>
      ON_GESTURE -- 3
      __qualname__ -- Stack
      ON_BUTTON -- 2
      __init__ -- <function __init__ at 0x20036e20>
      ON_START -- 0
      ON_BROADCAST -- 1
      STATUS_IDLE -- 20
      stop -- <function stop at 0x20036dc0>
      restart -- <function restart at 0x20036dd0>
      __module__ -- runtime.stack
      start -- <function start at 0x20036db0>
      ON_CONDITION -- 4
    object <module 'runtime.virtualmachine' from 'runtime/virtualmachine.mpy'> is of type module
      hub -- <module 'hub'>
      VMStore -- <class 'VMStore'>
      DirtyDict -- <class 'DirtyDict'>
      __file__ -- runtime/virtualmachine.mpy
      reset_time -- <function reset_time at 0x20021460>
      JSONRPC -- <class 'JSONRPC'>
      get_time -- <function get_time at 0x20021830>
      __name__ -- runtime.virtualmachine
      timer -- <module 'runtime.timer' from 'runtime/timer.mpy'>
      PORTS -- {'C': Port(C), 'B': Port(B), 'D': Port(D), 'E': Port(E), 'A': Port(A), 'F': Port(F)}
      VirtualMachine -- <class 'VirtualMachine'>
      Stack -- <class 'Stack'>
      System -- <class 'System'>
    object <class 'VirtualMachine'> is of type type
      register_on_condition -- <function register_on_condition at 0x20039a70>
      register_on_start -- <function register_on_start at 0x20039a30>
      reset_time -- <function reset_time at 0x20039ba0>
      shutdown -- <function shutdown at 0x20039b80>
      register_callback -- <function register_callback at 0x20039af0>
      register_on_gesture -- <function register_on_gesture at 0x20039a60>
      register_on_button -- <function register_on_button at 0x20039a80>
      __module__ -- runtime.virtualmachine
      reset_timer -- <function reset_timer at 0x20039b90>
      stop_stacks -- <function stop_stacks at 0x20039b60>
      schedule_coroutine -- <function schedule_coroutine at 0x20039b30>
      __qualname__ -- VirtualMachine
      __init__ -- <function __init__ at 0x20039a40>
      broadcast -- <function broadcast at 0x20039b00>
      check_all_conditions -- <generator>
      get_time -- <function get_time at 0x20039bb0>
      register_on_broadcast -- <function register_on_broadcast at 0x20039a50>
      start -- <function start at 0x20039b20>
    object <module 'runtime.dirty_dict' from 'runtime/dirty_dict.mpy'> is of type module
      DirtyDict -- <class 'DirtyDict'>
      __name__ -- runtime.dirty_dict
      __file__ -- runtime/dirty_dict.mpy
    object <class 'DirtyDict'> is of type type
      __delitem__ -- <closure>
      _mark_dirty -- <function _mark_dirty at 0x200384c0>
      dict_get -- <function dict_get at 0x20038590>
      list_insert -- <function list_insert at 0x20038530>
      __qualname__ -- DirtyDict
      __init__ -- <closure>
      list_del -- <function list_del at 0x20038560>
      list_clear -- <function list_clear at 0x20038570>
      __setitem__ -- <closure>
      dict_set -- <function dict_set at 0x20038580>
      list_append -- <function list_append at 0x20038550>
      list_set -- <function list_set at 0x20038520>
      __module__ -- runtime.dirty_dict
      dirty_items -- <generator>
      clear -- <closure>
    object <module 'runtime.vm_store' from 'runtime/vm_store.mpy'> is of type module
      _STOP -- 1
      __file__ -- runtime/vm_store.mpy
      DirtyDict -- <class 'DirtyDict'>
      _STALL -- True
      const -- <function>
      _PCALIB -- 17.5
      _LOC -- Billund
      _PAIR -- ('A', 'B')
      SUCCESS -- 0
      __name__ -- runtime.vm_store
      BRAKE -- 1
      _STAT -- 0
      _ACCEL -- (None, None)
      add_prop -- <function add_prop at 0x20038ed0>
      add_port_prop -- <function add_port_prop at 0x20038ee0>
      VMStore -- <class 'VMStore'>
    object <class 'VMStore'> is of type type
      move_speed -- <closure>
      weather_location -- <closure>
      weather_offset -- <closure>
      move_last_status -- <closure>
      motor_acceleration -- <closure>
      move_stop -- <closure>
      motor_stall -- <closure>
      move_calibration -- <closure>
      __module__ -- runtime.vm_store
      music_tempo -- <closure>
      move_acceleration -- <closure>
      sound_pitch -- <closure>
      music_instrument -- <closure>
      __qualname__ -- VMStore
      move_pair -- <closure>
      motor_last_status -- <closure>
      display_brightness -- <closure>
      motor_speed -- <closure>
      sound_volume -- <closure>
      sound_pan -- <closure>
      motor_stop -- <closure>
    object <module 'runtime.multimotor' from 'runtime/multimotor.mpy'> is of type module
      MultiMotor -- <class 'MultiMotor'>
      __name__ -- runtime.multimotor
      __file__ -- runtime/multimotor.mpy
    object <class 'MultiMotor'> is of type type
      __qualname__ -- MultiMotor
      await_all -- <generator>
      run -- <function run at 0x200365f0>
      __module__ -- runtime.multimotor
      __init__ -- <function __init__ at 0x20036600>
    object <module 'runtime.timer' from 'runtime/timer.mpy'> is of type module
      utime -- <module 'utime'>
      __name__ -- runtime.timer
      reset -- <function reset at 0x20037b50>
      __file__ -- runtime/timer.mpy
      get -- <function get at 0x20037b60>
      START_TIME -- 0