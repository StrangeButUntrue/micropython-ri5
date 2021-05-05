:mod:`protocol` -- RI5 communication protocol
=============================================

This module handles the communication protocol that the RI5 uses when talking
over USB/Bluetooth to a controller app.  The protocol uses a specific json
format.

Raw module data
---------------

::

    object <module 'protocol' from 'protocol/__init__.mpy'> is of type module
      __path__ -- protocol
      ujsonrpc -- <module 'protocol.ujsonrpc' from 'protocol/ujsonrpc.mpy'>
      __name__ -- protocol
      notifications -- <module 'protocol.notifications' from 'protocol/notifications.mpy'>
      __file__ -- protocol/__init__.mpy
      rpc_protocol -- <module 'protocol.rpc_protocol' from 'protocol/rpc_protocol.mpy'>
      RPCProtocol -- <class 'RPCProtocol'>
    object <module 'protocol.ujsonrpc' from 'protocol/ujsonrpc.mpy'> is of type module
      _ID_PREFIX -- b'{"i":'
      __file__ -- protocol/ujsonrpc.mpy
      _PARAMS -- b',"p":'
      urandom -- <module 'urandom'>
      _ID -- b',"i":'
      b2a_base64 -- <function>
      ENOENT -- 2
      ujson -- <module 'ujson'>
      __name__ -- protocol.ujsonrpc
      sleep_ms -- <function>
      _ERROR -- b',"e":'
      StringIO -- <class 'StringIO'>
      _SUFFIX -- b'}\r'
      _SUSPENDED_MSG_PATH_ -- ./suspended_msg
      _CARRIAGE_RETURN -- b'\r'
      uos -- <module 'uos'>
      NO_RESPONSE -- {}
      JSONRPC -- <class 'JSONRPC'>
      _METHOD_PREFIX -- b'{"m":'
      _RESPONSE -- b',"r":'
    object <class 'JSONRPC'> is of type type
      _pop_suspend_message -- <function _pop_suspend_message at 0x20023290>
      clear_methods -- <function clear_methods at 0x200232b0>
      emit_large -- <function emit_large at 0x200232d0>
      reply -- <function reply at 0x20023240>
      _handle_message -- <function _handle_message at 0x20023270>
      methods -- {'scratch.display_animation': <bound_method>, 'scratch.motor_pwm': <bound_method>, 'set_hub_name': <bound_method>, 'scratch.play_sound': <bound_method>, 'get_linegraph_monitor_info': <bound_method>, 'reset_program_time': <bound_method>, 'set_port_mode': <bound_method>, 'scratch.motor_go_direction_to_position': <bound_method>, 'sync_display': <bound_method>, 'scratch.reset_yaw': <bound_method>, 'scratch.when_sensor_changed': <bound_method>, 'scratch.motor_run_timed': <bound_method>, 'scratch.move_stop': <bound_method>, 'program_execute': <bound_method>, 'scratch.when_sensor_force_released': <bound_method>, 'remove_project': <bound_method>, 'start_write_program': <bound_method>, 'get_storage_status': <bound_method>, 'scratch.sound_beep': <bound_method>, 'scratch.sound_off': <bound_method>, 'scratch.display_set_pixel': <bound_method>, 'scratch.ultrasonic_light_up': <bound_method>, 'scratch.motor_start': <bound_method>, 'delete_linegraph_file': <bound_method>, 'program_terminate': <bound_method>, 'scratch.display_rotate_direction': <bound_method>, 'scratch.display_image': <bound_method>, 'scratch.move_start_powers': <bound_method>, 'scratch.sound_beep_for_time': <bound_method>, 'get_program_time': <bound_method>, 'move_project': <bound_method>, 'get_hub_info': <bound_method>, 'scratch.center_button_lights': <bound_method>, 'scratch.motor_position': <bound_method>, 'scratch.move_start_speeds': <bound_method>, 'program_modechange': <bound_method>, 'scratch.move_tank_degrees': <bound_method>, 'scratch.motor_go_to_relative_position': <bound_method>, 'write_package': <bound_method>, 'scratch.display_rotate_orientation': <bound_method>, 'scratch.display_image_for': <bound_method>, 'scratch.when_sensor_force_bumped': <bound_method>, 'scratch.move_tank_time': <bound_method>, 'scratch.wait_gesture': <bound_method>, 'scratch.motor_run_for_degrees': <bound_method>, 'trigger_current_state': <bound_method>, 'scratch.display_clear': <bound_method>, 'scratch.motor_stop': <bound_method>, 'scratch.motor_adjust_offset': <bound_method>, 'start_program_time': <bound_method>, 'scratch.motor_set_position': <bound_method>, 'scratch.display_text': <bound_method>, 'get_linegraph_monitor_package': <bound_method>}
      suspend_current_message -- <function suspend_current_message at 0x20023280>
      __module__ -- protocol.ujsonrpc
      error -- <function error at 0x20023260>
      add_method -- <function add_method at 0x200232a0>
      parse_chunk -- <function parse_chunk at 0x20023170>
      stream -- <property>
      cancel_call -- <function cancel_call at 0x20023330>
      __init__ -- <function __init__ at 0x20023100>
      __qualname__ -- JSONRPC
      parse_buffer -- <function parse_buffer at 0x20023110>
      emit -- <function emit at 0x20023300>
      call -- <function call at 0x20023320>
      pending -- {}
      resume_suspended_msg -- <function resume_suspended_msg at 0x20023120>
    object <module 'protocol.notifications' from 'protocol/notifications.mpy'> is of type module
      notify_error_event -- <function notify_error_event at 0x20024f10>
      notify_sensor_data -- <function notify_sensor_data at 0x200218d0>
      hub -- <module 'hub'>
      notify_storage_status -- <function notify_storage_status at 0x200218e0>
      __name__ -- protocol.notifications
      notify_stack_start -- <function notify_stack_start at 0x20024ed0>
      notify_battery_status -- <function notify_battery_status at 0x200218f0>
      sensor_data -- [[0, ()], [0, ()], [0, ()], [0, ()], [0, ()], [0, ()], (0, -805, 585), (3, 3, 0), (-3, 0, 54), '', 0]
      get_storage_information -- <function get_storage_information at 0x20024d60>
      notify_program_running -- <function notify_program_running at 0x20024f30>
      notify_gesture_event -- <function notify_gesture_event at 0x20024ef0>
      notify_info_status -- <function notify_info_status at 0x20023cb0>
      mem_alloc -- <function>
      b2a_base64 -- <function>
      _RQ_LEN -- run_queue_len
      battery_status -- [8.36, 100, True]
      notify_vm_state -- <function notify_vm_state at 0x20024f00>
      notify_stack_stop -- <function notify_stack_stop at 0x20024ee0>
      __file__ -- protocol/notifications.mpy
      const -- <function>
      notify_linegraph_timer_reset -- <function notify_linegraph_timer_reset at 0x20024f50>
      _MEM -- mem_alloc
      _D -- mem_delta
      _DEBUG_PAYLOAD -- {'wait_queue_len': 0, 'mem_delta': 0, 'run_queue_len': 0, 'mem_alloc': 0}
      _WQ_LEN -- wait_queue_len
      read_local_name -- <function read_local_name at 0x20024da0>
      notify_debug_event -- <function notify_debug_event at 0x200250c0>
      notify_button_event -- <function notify_button_event at 0x20024ec0>
      notify_gesture_status -- <function notify_gesture_status at 0x20023ca0>
    object <module 'protocol.rpc_protocol' from 'protocol/rpc_protocol.mpy'> is of type module
      const -- <function>
      update_sensor_data -- <function update_sensor_data at 0x20022130>
      notify_debug_event -- <function notify_debug_event at 0x200250c0>
      get_event_loop -- <function get_event_loop at 0x2001ca30>
      __file__ -- protocol/rpc_protocol.mpy
      __name__ -- protocol.rpc_protocol
      RPCProtocol -- <class 'RPCProtocol'>
      JSONRPC -- <class 'JSONRPC'>
      update_battery_status -- <function update_battery_status at 0x20022140>
      notify_sensor_data -- <function notify_sensor_data at 0x200218d0>
      notify_battery_status -- <function notify_battery_status at 0x200218f0>
    object <class 'RPCProtocol'> is of type type
      register_method_handlers -- <function register_method_handlers at 0x20025190>
      stream -- <property>
      __init__ -- <function __init__ at 0x20023390>
      __qualname__ -- RPCProtocol
      _register_method_handler -- <function _register_method_handler at 0x200233a0>
      looper -- <generator>
      __module__ -- protocol.rpc_protocol
