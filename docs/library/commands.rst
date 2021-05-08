:mod:`commands` -- commands module
==================================

.. module:: commands
   :synopsis: commands module

Module containing a lot of high-level concepts, but no obvious theme beyond that.

Raw module data
---------------

::

    object <module 'commands' from 'commands/__init__.mpy'> is of type module
      ProgramMethods -- <class 'ProgramMethods'>
      sound_methods -- <module 'commands.sound_methods' from 'commands/sound_methods.mpy'>
      __file__ -- commands/__init__.mpy
      LightMethods -- <class 'LightMethods'>
      motor_methods -- <module 'commands.motor_methods' from 'commands/motor_methods.mpy'>
      __name__ -- commands
      program_methods -- <module 'commands.program_methods' from 'commands/program_methods.mpy'>
      __path__ -- commands
      move_methods -- <module 'commands.move_methods' from 'commands/move_methods.mpy'>
      SoundMethods -- <class 'SoundMethods'>
      linegraphmonitor_methods -- <module 'commands.linegraphmonitor_methods' from 'commands/linegraphmonitor_methods.mpy'>
      light_methods -- <module 'commands.light_methods' from 'commands/light_methods.mpy'>
      abstract_handler -- <module 'commands.abstract_handler' from 'commands/abstract_handler.mpy'>
      LinegraphMonitorMethods -- <class 'LinegraphMonitorMethods'>
      hub_methods -- <module 'commands.hub_methods' from 'commands/hub_methods.mpy'>
      HubMethods -- <class 'HubMethods'>
      wait_methods -- <module 'commands.wait_methods' from 'commands/wait_methods.mpy'>
      MotorMethods -- <class 'MotorMethods'>
      WaitMethods -- <class 'WaitMethods'>
      MoveMethods -- <class 'MoveMethods'>
    object <module 'commands.abstract_handler' from 'commands/abstract_handler.mpy'> is of type module
      AbstractHandler -- <class 'AbstractHandler'>
      __name__ -- commands.abstract_handler
      __file__ -- commands/abstract_handler.mpy
    object <class 'AbstractHandler'> is of type type
      __init__ -- <function __init__ at 0x20025640>
      __qualname__ -- AbstractHandler
      __module__ -- commands.abstract_handler
      get_methods -- <function get_methods at 0x20025670>
      _rpc -- None
    object <module 'commands.linegraphmonitor_methods' from 'commands/linegraphmonitor_methods.mpy'> is of type module
      const -- <function>
      os -- <module 'uos'>
      ticks_ms -- <function>
      __file__ -- commands/linegraphmonitor_methods.mpy
      AbstractHandler -- <class 'AbstractHandler'>
      ticks_diff -- <function>
      ENOENT -- 2
      __name__ -- commands.linegraphmonitor_methods
      LINEGRAPH_DIR -- /data/linegraph
      math -- <module 'math'>
      LinegraphMonitorMethods -- <class 'LinegraphMonitorMethods'>
      sleep_ms -- <function>
    object <class 'LinegraphMonitorMethods'> is of type type
      handle_delete_file -- <function handle_delete_file at 0x20027740>
      handle_get_linegraph_monitor_info -- <function handle_get_linegraph_monitor_info at 0x20027710>
      __init__ -- <closure>
      __qualname__ -- LinegraphMonitorMethods
      _error_if_running -- <function _error_if_running at 0x20027750>
      handle_get_linegraph_monitor_package -- <function handle_get_linegraph_monitor_package at 0x20027760>
      get_methods -- <function get_methods at 0x20027770>
      __module__ -- commands.linegraphmonitor_methods
    object <module 'commands.sound_methods' from 'commands/sound_methods.mpy'> is of type module
      hub -- <module 'hub'>
      AbstractHandler -- <class 'AbstractHandler'>
      __name__ -- commands.sound_methods
      __file__ -- commands/sound_methods.mpy
      SoundMethods -- <class 'SoundMethods'>
    object <class 'SoundMethods'> is of type type
      handle_sound_beep_for_time -- <function handle_sound_beep_for_time at 0x2002ad30>
      __init__ -- <closure>
      handle_play_sound -- <function handle_play_sound at 0x2002ad20>
      __qualname__ -- SoundMethods
      handle_sound_off -- <function handle_sound_off at 0x2002ad10>
      get_methods -- <function get_methods at 0x2002ad40>
      handle_sound_beep -- <function handle_sound_beep at 0x2002ace0>
      __module__ -- commands.sound_methods
    object <module 'commands.light_methods' from 'commands/light_methods.mpy'> is of type module
      LightMethods -- <class 'LightMethods'>
      AbstractHandler -- <class 'AbstractHandler'>
      percent_to_int -- <function percent_to_int at 0x200213a0>
      NO_STATUS -- -1
      __file__ -- commands/light_methods.mpy
      PORTS -- {'C': Port(C), 'B': Port(B), 'D': Port(D), 'E': Port(E), 'A': Port(A), 'F': Port(F)}
      __name__ -- commands.light_methods
      hub -- <module 'hub'>
      number_color_to_rgb -- <function number_color_to_rgb at 0x200213e0>
      rotate_hub_display -- <function rotate_hub_display at 0x20026820>
      rotate_hub_display_to_value -- <function rotate_hub_display_to_value at 0x20026b80>
      set_display_sync -- <function set_display_sync at 0x20022170>
    object <class 'LightMethods'> is of type type
      handle_display_rotate_direction -- <function handle_display_rotate_direction at 0x20026d30>
      _merge_display_params -- <staticmethod>
      handle_display_rotate_orientation -- <function handle_display_rotate_orientation at 0x20026d40>
      handle_ultrasonic_light_up -- <function handle_ultrasonic_light_up at 0x20026d80>
      handle_display_clear -- <function handle_display_clear at 0x20026cc0>
      get_methods -- <function get_methods at 0x20026da0>
      handle_display_animation -- <function handle_display_animation at 0x20026d20>
      __module__ -- commands.light_methods
      handle_center_button_lights -- <function handle_center_button_lights at 0x20026d70>
      DEFAULT_DISPLAY_PARAMS -- {'fade': 0, 'delay': 500, 'wait': False, 'loop': False, 'clear': False}
      __qualname__ -- LightMethods
      __init__ -- <closure>
      handle_display_set_pixel -- <function handle_display_set_pixel at 0x20026c40>
      handle_display_sync -- <function handle_display_sync at 0x20026d90>
      handle_display_image_for -- <function handle_display_image_for at 0x20026d10>
      show_frames -- <function show_frames at 0x20026ce0>
      handle_display_image -- <function handle_display_image at 0x20026d50>
      handle_display_text -- <function handle_display_text at 0x20026d60>
    object <module 'commands.program_methods' from 'commands/program_methods.mpy'> is of type module
      ProgramMethods -- <class 'ProgramMethods'>
      __file__ -- commands/program_methods.mpy
      start_time -- <function start_time at 0x20021840>
      a2b_base64 -- <function>
      storage -- <module 'util.storage' from 'util/storage.mpy'>
      const -- <function>
      sys -- <module 'sys'>
      urandom -- <module 'urandom'>
      get_time -- <function get_time at 0x20021830>
      __name__ -- commands.program_methods
      reset_time -- <function reset_time at 0x20021460>
      utime -- <module 'utime'>
      notifications -- <module 'protocol.notifications' from 'protocol/notifications.mpy'>
      AbstractHandler -- <class 'AbstractHandler'>
      _TRANSFER_HANDLE -- {}
      _PRINT_OVERRIDE -- from util.print_override import spikeprint;print = spikeprint

    object <class 'ProgramMethods'> is of type type
      handle_write_package -- <function handle_write_package at 0x2002a490>
      handle_program_reset_time -- <function handle_program_reset_time at 0x2002a510>
      handle_program_start_time -- <function handle_program_start_time at 0x2002a520>
      handle_soft_reset -- <function handle_soft_reset at 0x2002a530>
      get_methods -- <function get_methods at 0x2002a540>
      __qualname__ -- ProgramMethods
      _handle_write_print_override -- <function _handle_write_print_override at 0x2002a480>
      handle_program_execute -- <function handle_program_execute at 0x2002a4d0>
      handle_start_write_program -- <function handle_start_write_program at 0x2002a4a0>
      handle_remove_project -- <function handle_remove_project at 0x2002a4c0>
      handle_program_terminate -- <function handle_program_terminate at 0x2002a4e0>
      handle_program_modechange -- <function handle_program_modechange at 0x2002a4f0>
      __init__ -- <closure>
      handle_program_get_time -- <function handle_program_get_time at 0x2002a500>
      __module__ -- commands.program_methods
      handle_storage_status -- <function handle_storage_status at 0x2002a3b0>
      handle_move_project -- <function handle_move_project at 0x2002a4b0>
    object <module 'commands.motor_methods' from 'commands/motor_methods.mpy'> is of type module
      NO_STATUS -- -1
      MotorMethods -- <class 'MotorMethods'>
      __name__ -- commands.motor_methods
      get_event_loop -- <function get_event_loop at 0x2001ca30>
      __file__ -- commands/motor_methods.mpy
      AbstractHandler -- <class 'AbstractHandler'>
      hub -- <module 'hub'>
      PORTS -- {'C': Port(C), 'B': Port(B), 'D': Port(D), 'E': Port(E), 'A': Port(A), 'F': Port(F)}
    object <class 'MotorMethods'> is of type type
      handle_motor_pwm -- <function handle_motor_pwm at 0x20028840>
      handle_motor_go_direction_to_position -- <function handle_motor_go_direction_to_position at 0x20028800>
      __qualname__ -- MotorMethods
      __init__ -- <closure>
      handle_motor_run_timed -- <function handle_motor_run_timed at 0x200287f0>
      handle_motor_stop -- <function handle_motor_stop at 0x20028830>
      handle_motor_start -- <function handle_motor_start at 0x20028820>
      handle_motor_run_for_degrees -- <function handle_motor_run_for_degrees at 0x20028810>
      handle_motor_set_position -- <function handle_motor_set_position at 0x20028850>
      get_methods -- <function get_methods at 0x20028870>
      handle_motor_go_to_relative_position -- <function handle_motor_go_to_relative_position at 0x200287e0>
      __module__ -- commands.motor_methods
      handle_motor_adjust_offset -- <function handle_motor_adjust_offset at 0x20028860>
      handle_motor_position -- <function handle_motor_position at 0x20028770>
    object <module 'commands.hub_methods' from 'commands/hub_methods.mpy'> is of type module
      ENOENT -- 2
      AbstractHandler -- <class 'AbstractHandler'>
      __name__ -- commands.hub_methods
      notifications -- <module 'protocol.notifications' from 'protocol/notifications.mpy'>
      hub -- <module 'hub'>
      HubMethods -- <class 'HubMethods'>
      a2b_base64 -- <function>
      __file__ -- commands/hub_methods.mpy
      write_local_name -- <function write_local_name at 0x20024db0>
      version -- <module 'version' from 'version.py'>
    object <class 'HubMethods'> is of type type
      handle_trigger_current_state -- <function handle_trigger_current_state at 0x200253a0>
      get_methods -- <function get_methods at 0x20025790>
      __module__ -- commands.hub_methods
      handle_set_port_mode -- <function handle_set_port_mode at 0x20025760>
      __init__ -- <closure>
      handle_set_hub_name -- <function handle_set_hub_name at 0x20025770>
      __qualname__ -- HubMethods
      handle_get_hub_info -- <function handle_get_hub_info at 0x20025780>
      handle_reset_yaw -- <function handle_reset_yaw at 0x20025750>
    object <module 'commands.wait_methods' from 'commands/wait_methods.mpy'> is of type module
      WaitMethods -- <class 'WaitMethods'>
      AbstractHandler -- <class 'AbstractHandler'>
      __name__ -- commands.wait_methods
      __file__ -- commands/wait_methods.mpy
    object <class 'WaitMethods'> is of type type
      handle_when_sensor_changed -- <function handle_when_sensor_changed at 0x2002b5c0>
      __init__ -- <closure>
      get_methods -- <function get_methods at 0x2002b620>
      __qualname__ -- WaitMethods
      handle_when_sensor_force_bumped -- <function handle_when_sensor_force_bumped at 0x2002b5f0>
      handle_when_sensor_force_released -- <function handle_when_sensor_force_released at 0x2002b610>
      handle_wait_gesture -- <function handle_wait_gesture at 0x2002b600>
      __module__ -- commands.wait_methods
    object <module 'commands.move_methods' from 'commands/move_methods.mpy'> is of type module
      __name__ -- commands.move_methods
      AbstractHandler -- <class 'AbstractHandler'>
      NO_STATUS -- -1
      __file__ -- commands/move_methods.mpy
      MoveMethods -- <class 'MoveMethods'>
    object <class 'MoveMethods'> is of type type
      handle_move_tank_degrees -- <function handle_move_tank_degrees at 0x20029310>
      get_methods -- <function get_methods at 0x20029330>
      handle_move_tank_time -- <function handle_move_tank_time at 0x200292c0>
      handle_move_start_powers -- <function handle_move_start_powers at 0x20029300>
      __module__ -- commands.move_methods
      __init__ -- <closure>
      __qualname__ -- MoveMethods
      handle_move_stop -- <function handle_move_stop at 0x20029320>
      handle_move_start_speeds -- <function handle_move_start_speeds at 0x200292f0>