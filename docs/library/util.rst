:mod:`util` -- misc utility module
==================================

Contains various miscellaneous utility sub-modules.

Raw module data
---------------

::

    object <module 'util' from 'util/__init__.mpy'> is of type module
      resetter -- <module 'util.resetter' from 'util/resetter.mpy'>
      color -- <module 'util.color' from 'util/color.mpy'>
      __file__ -- util/__init__.mpy
      animations -- <module 'util.animations' from 'util/animations.mpy'>
      motor -- <module 'util.motor' from 'util/motor.mpy'>
      scratch -- <module 'util.scratch' from 'util/scratch.mpy'>
      storage -- <module 'util.storage' from 'util/storage.mpy'>
      sensors -- <module 'util.sensors' from 'util/sensors.mpy'>
      time -- <module 'util.time' from 'util/time.mpy'>
      error_handler -- <module 'util.error_handler' from 'util/error_handler.mpy'>
      __name__ -- util
      log -- <module 'util.log' from 'util/log.mpy'>
      schedule -- <module 'util.schedule' from 'util/schedule.mpy'>
      print_override -- <module 'util.print_override' from 'util/print_override.mpy'>
      constants -- <module 'util.constants' from 'util/constants.mpy'>
      __path__ -- util
      rotation -- <module 'util.rotation' from 'util/rotation.mpy'>
    object <module 'util.rotation' from 'util/rotation.mpy'> is of type module
      _CURRENT_ROTATION -- 0
      rotate_hub_display -- <function rotate_hub_display at 0x20026820>
      hub -- <module 'hub'>
      __name__ -- util.rotation
      __file__ -- util/rotation.mpy
      dir_to_rotation -- <function dir_to_rotation at 0x20026810>
      rotate_hub_display_to_value -- <function rotate_hub_display_to_value at 0x20026b80>
      rotate_hub_display_to_orientation -- <function rotate_hub_display_to_orientation at 0x20026b90>
    object <module 'util.constants' from 'util/constants.mpy'> is of type module
      LINEGRAPH_DIR -- /data/linegraph
      LPF2_ORIENTATION -- 59
      LPF2_GYRO -- 58
      const -- <function>
      STALLED -- 2
      LONG_PRESS_MS -- 3000
      INACTIVE_SHUTDOWN_MS -- 300000
      DEFAULT_IMAGE -- (Image('09090:99999:99999:09990:00900:'), Image('09000:09900:09990:09900:09000:'))
      LOCAL_NAME -- /local_name.txt
      LPF2_FLIPPER_MOTOR_SMALL -- 65
      USB_VCP -- USB_VCP(0)
      hub -- <module 'hub'>
      NUMBER -- 0
      HOLD -- 2
      MOTOR_TYPES -- (65, 48, 49, 75, 76)
      PORTS -- {'C': Port(C), 'B': Port(B), 'D': Port(D), 'E': Port(E), 'A': Port(A), 'F': Port(F)}
      INACTIVE_SHUTDOWN_BT_MS -- 1200000
      NO_KEY -- -1
      LPF2_FLIPPER_FORCE -- 63
      LPF2_FLIPPER_MOTOR_LARGE -- 49
      STRING -- 1
      SUCCESS -- 0
      LPF2_FLIPPER_MOTOR_MEDIUM -- 48
      LPF2_FLIPPER_COLOR -- 61
      LPF2_STONE_GREY_MOTOR_LARGE -- 76
      __file__ -- util/constants.mpy
      Image -- <class 'Image'>
      BRAKE -- 1
      BT_VCP -- BT_VCP(0)
      SLOTS_IMAGE -- (Image('09990:09090:09090:09090:09990:'), Image('00900:09900:00900:00900:09990:'), Image('09990:00090:09990:09000:09990:'), Image('09990:00090:09990:00090:09990:'), Image('09090:09090:09990:00090:00090:'), Image('09990:09000:09990:00090:09990:'), Image('09990:09000:09990:09090:09990:'), Image('09990:00090:00900:09000:09000:'), Image('09990:09090:09990:09090:09990:'), Image('09990:09090:09990:00090:09990:'), Image('90999:90909:90909:90909:90999:'), Image('09009:99099:09009:09009:09009:'), Image('90999:90009:90999:90900:90999:'), Image('90999:90009:90999:90009:90999:'), Image('90909:90909:90999:90009:90009:'), Image('90999:90900:90999:90009:90999:'), Image('90999:90900:90999:90909:90999:'), Image('90999:90009:90090:90900:90900:'), Image('90999:90909:90999:90909:90999:'), Image('90999:90909:90999:90009:90999:'))
      BOOLEAN -- 2
      LPF2_ACCELERATION -- 57
      LPF2_STONE_GREY_MOTOR_MEDIUM -- 75
      DATA_DIR -- /data
      TIMER_PACE_LOW -- 48
      __name__ -- util.constants
      TIMER_PACE_HIGH -- 16
      LPF2_FLIPPER_DISTANCE -- 62
      NO_STATUS -- -1
      FLOAT -- 0
      VAR_DEFAULTS -- {0: 0, 1: '', 2: False}
      INTERRUPTED -- 1
      Sounds -- <class 'Sounds'>
    object <class 'Sounds'> is of type type
      __module__ -- util.constants
      NAVIGATION -- sounds/menu_click
      NAVIGATION_FAST -- sounds/menu_fastback
      __qualname__ -- Sounds
      STARTUP -- sounds/startup
      SHUTDOWN -- sounds/menu_shutdown
      PROGRAM_STOP -- sounds/menu_program_stop
      PROGRAM_START -- sounds/menu_program_start
    object <class 'Image'> is of type type
      width -- <function>
      height -- <function>
      get_pixel -- <function>
      set_pixel -- <function>
      shift_left -- <function>
      shift_right -- <function>
      shift_up -- <function>
      shift_down -- <function>
      HEART -- Image(
        '09090:'
        '99999:'
        '99999:'
        '09990:'
        '00900:'
    )
      HEART_SMALL -- Image(
        '00000:'
        '09090:'
        '09990:'
        '00900:'
        '00000:'
    )
      HAPPY -- Image(
        '00000:'
        '09090:'
        '00000:'
        '90009:'
        '09990:'
    )
      SMILE -- Image(
        '00000:'
        '00000:'
        '00000:'
        '90009:'
        '09990:'
    )
      SAD -- Image(
        '00000:'
        '09090:'
        '00000:'
        '09990:'
        '90009:'
    )
      CONFUSED -- Image(
        '00000:'
        '09090:'
        '00000:'
        '09090:'
        '90909:'
    )
      ANGRY -- Image(
        '90009:'
        '09090:'
        '00000:'
        '99999:'
        '90909:'
    )
      ASLEEP -- Image(
        '00000:'
        '99099:'
        '00000:'
        '09990:'
        '00000:'
    )
      SURPRISED -- Image(
        '09090:'
        '00000:'
        '00900:'
        '09090:'
        '00900:'
    )
      SILLY -- Image(
        '90009:'
        '00000:'
        '99999:'
        '00909:'
        '00999:'
    )
      FABULOUS -- Image(
        '99999:'
        '99099:'
        '00000:'
        '09090:'
        '09990:'
    )
      MEH -- Image(
        '09090:'
        '00000:'
        '00090:'
        '00900:'
        '09000:'
    )
      YES -- Image(
        '00000:'
        '00009:'
        '00090:'
        '90900:'
        '09000:'
    )
      NO -- Image(
        '90009:'
        '09090:'
        '00900:'
        '09090:'
        '90009:'
    )
      CLOCK12 -- Image(
        '00900:'
        '00900:'
        '00900:'
        '00000:'
        '00000:'
    )
      CLOCK1 -- Image(
        '00090:'
        '00090:'
        '00900:'
        '00000:'
        '00000:'
    )
      CLOCK2 -- Image(
        '00000:'
        '00099:'
        '00900:'
        '00000:'
        '00000:'
    )
      CLOCK3 -- Image(
        '00000:'
        '00000:'
        '00999:'
        '00000:'
        '00000:'
    )
      CLOCK4 -- Image(
        '00000:'
        '00000:'
        '00900:'
        '00099:'
        '00000:'
    )
      CLOCK5 -- Image(
        '00000:'
        '00000:'
        '00900:'
        '00090:'
        '00090:'
    )
      CLOCK6 -- Image(
        '00000:'
        '00000:'
        '00900:'
        '00900:'
        '00900:'
    )
      CLOCK7 -- Image(
        '00000:'
        '00000:'
        '00900:'
        '09000:'
        '09000:'
    )
      CLOCK8 -- Image(
        '00000:'
        '00000:'
        '00900:'
        '99000:'
        '00000:'
    )
      CLOCK9 -- Image(
        '00000:'
        '00000:'
        '99900:'
        '00000:'
        '00000:'
    )
      CLOCK10 -- Image(
        '00000:'
        '99000:'
        '00900:'
        '00000:'
        '00000:'
    )
      CLOCK11 -- Image(
        '09000:'
        '09000:'
        '00900:'
        '00000:'
        '00000:'
    )
      ARROW_N -- Image(
        '00900:'
        '09990:'
        '90909:'
        '00900:'
        '00900:'
    )
      ARROW_NE -- Image(
        '00999:'
        '00099:'
        '00909:'
        '09000:'
        '90000:'
    )
      ARROW_E -- Image(
        '00900:'
        '00090:'
        '99999:'
        '00090:'
        '00900:'
    )
      ARROW_SE -- Image(
        '90000:'
        '09000:'
        '00909:'
        '00099:'
        '00999:'
    )
      ARROW_S -- Image(
        '00900:'
        '00900:'
        '90909:'
        '09990:'
        '00900:'
    )
      ARROW_SW -- Image(
        '00009:'
        '00090:'
        '90900:'
        '99000:'
        '99900:'
    )
      ARROW_W -- Image(
        '00900:'
        '09000:'
        '99999:'
        '09000:'
        '00900:'
    )
      ARROW_NW -- Image(
        '99900:'
        '99000:'
        '90900:'
        '00090:'
        '00009:'
    )
      GO_RIGHT -- Image(
        '09000:'
        '09900:'
        '09990:'
        '09900:'
        '09000:'
    )
      GO_LEFT -- Image(
        '00090:'
        '00990:'
        '09990:'
        '00990:'
        '00090:'
    )
      GO_UP -- Image(
        '00000:'
        '00900:'
        '09990:'
        '99999:'
        '00000:'
    )
      GO_DOWN -- Image(
        '00000:'
        '99999:'
        '09990:'
        '00900:'
        '00000:'
    )
      TRIANGLE -- Image(
        '00000:'
        '00900:'
        '09090:'
        '99999:'
        '00000:'
    )
      TRIANGLE_LEFT -- Image(
        '90000:'
        '99000:'
        '90900:'
        '90090:'
        '99999:'
    )
      CHESSBOARD -- Image(
        '09090:'
        '90909:'
        '09090:'
        '90909:'
        '09090:'
    )
      DIAMOND -- Image(
        '00900:'
        '09090:'
        '90009:'
        '09090:'
        '00900:'
    )
      DIAMOND_SMALL -- Image(
        '00000:'
        '00900:'
        '09090:'
        '00900:'
        '00000:'
    )
      SQUARE -- Image(
        '99999:'
        '90009:'
        '90009:'
        '90009:'
        '99999:'
    )
      SQUARE_SMALL -- Image(
        '00000:'
        '09990:'
        '09090:'
        '09990:'
        '00000:'
    )
      RABBIT -- Image(
        '90900:'
        '90900:'
        '99990:'
        '99090:'
        '99990:'
    )
      COW -- Image(
        '90009:'
        '90009:'
        '99999:'
        '09990:'
        '00900:'
    )
      MUSIC_CROTCHET -- Image(
        '00900:'
        '00900:'
        '00900:'
        '99900:'
        '99900:'
    )
      MUSIC_QUAVER -- Image(
        '00900:'
        '00990:'
        '00909:'
        '99900:'
        '99900:'
    )
      MUSIC_QUAVERS -- Image(
        '09999:'
        '09009:'
        '09009:'
        '99099:'
        '99099:'
    )
      PITCHFORK -- Image(
        '90909:'
        '90909:'
        '99999:'
        '00900:'
        '00900:'
    )
      XMAS -- Image(
        '00900:'
        '09990:'
        '00900:'
        '09990:'
        '99999:'
    )
      PACMAN -- Image(
        '09999:'
        '99090:'
        '99900:'
        '99990:'
        '09999:'
    )
      TARGET -- Image(
        '00900:'
        '09990:'
        '99099:'
        '09990:'
        '00900:'
    )
      ALL_CLOCKS -- (Image('00900:00900:00900:00000:00000:'), Image('00090:00090:00900:00000:00000:'), Image('00000:00099:00900:00000:00000:'), Image('00000:00000:00999:00000:00000:'), Image('00000:00000:00900:00099:00000:'), Image('00000:00000:00900:00090:00090:'), Image('00000:00000:00900:00900:00900:'), Image('00000:00000:00900:09000:09000:'), Image('00000:00000:00900:99000:00000:'), Image('00000:00000:99900:00000:00000:'), Image('00000:99000:00900:00000:00000:'), Image('09000:09000:00900:00000:00000:'))
      ALL_ARROWS -- (Image('00900:09990:90909:00900:00900:'), Image('00999:00099:00909:09000:90000:'), Image('00900:00090:99999:00090:00900:'), Image('90000:09000:00909:00099:00999:'), Image('00900:00900:90909:09990:00900:'), Image('00009:00090:90900:99000:99900:'), Image('00900:09000:99999:09000:00900:'), Image('99900:99000:90900:00090:00009:'))
      TSHIRT -- Image(
        '99099:'
        '99999:'
        '09990:'
        '09990:'
        '09990:'
    )
      ROLLERSKATE -- Image(
        '00099:'
        '00099:'
        '99999:'
        '99999:'
        '09090:'
    )
      DUCK -- Image(
        '09900:'
        '99900:'
        '09999:'
        '09990:'
        '00000:'
    )
      HOUSE -- Image(
        '00900:'
        '09990:'
        '99999:'
        '09990:'
        '09090:'
    )
      TORTOISE -- Image(
        '00000:'
        '09990:'
        '99999:'
        '09090:'
        '00000:'
    )
      BUTTERFLY -- Image(
        '99099:'
        '99999:'
        '00900:'
        '99999:'
        '99099:'
    )
      STICKFIGURE -- Image(
        '00900:'
        '99999:'
        '00900:'
        '09090:'
        '90009:'
    )
      GHOST -- Image(
        '99999:'
        '90909:'
        '99999:'
        '99999:'
        '90909:'
    )
      SWORD -- Image(
        '00900:'
        '00900:'
        '00900:'
        '09990:'
        '00900:'
    )
      GIRAFFE -- Image(
        '99000:'
        '09000:'
        '09000:'
        '09990:'
        '09090:'
    )
      SKULL -- Image(
        '09990:'
        '90909:'
        '99999:'
        '09990:'
        '09990:'
    )
      UMBRELLA -- Image(
        '09990:'
        '99999:'
        '00900:'
        '90900:'
        '09900:'
    )
      SNAKE -- Image(
        '99000:'
        '99099:'
        '09090:'
        '09990:'
        '00000:'
    )
    object <module 'util.print_override' from 'util/print_override.mpy'> is of type module
      _NOT_CONNECTED_ERROR -- The programming app is not connected to the hub.
      spikeprint -- <function spikeprint at 0x2001aa00>
      ticks_ms -- <function>
      USB_VCP -- USB_VCP(0)
      __file__ -- util/print_override.mpy
      uio -- <module 'uio'>
      __name__ -- util.print_override
      ticks_diff -- <function>
      b2a_base64 -- <function>
      BT_VCP -- BT_VCP(0)
      JSONRPC -- <class 'JSONRPC'>
      builtins -- <module 'builtins'>
    object <module 'util.schedule' from 'util/schedule.mpy'> is of type module
      micropython -- <module 'micropython'>
      mp_schedule -- <function>
      __name__ -- util.schedule
      __file__ -- util/schedule.mpy
    object <module 'util.log' from 'util/log.mpy'> is of type module
      log_to_file -- <function log_to_file at 0x2002c560>
      log_critical_error -- <function log_critical_error at 0x2002c510>
      clear_log -- <function clear_log at 0x2002c0b0>
      __file__ -- util/log.mpy
      gc -- <module 'gc'>
      _write_to_log -- <function _write_to_log at 0x2002c520>
      timed_fn_buffer -- []
      sys -- <module 'sys'>
      __name__ -- util.log
      _LOG_FILE -- ./runtime.log
      uio -- <module 'uio'>
      utime -- <module 'utime'>
      timed_function -- <function timed_function at 0x2002c550>
      cat_log -- <function cat_log at 0x2002c0a0>
      uos -- <module 'uos'>
    object <module 'util.error_handler' from 'util/error_handler.mpy'> is of type module
      hub -- <module 'hub'>
      __file__ -- util/error_handler.mpy
      notifications -- <module 'protocol.notifications' from 'protocol/notifications.mpy'>
      __name__ -- util.error_handler
      uio -- <module 'uio'>
      b2a_base64 -- <function>
      RED -- (255, 0, 0)
      PROGRAM_EXECUTION_MEMORY_ERROR -- 1
      get_event_loop -- <function get_event_loop at 0x2001ca30>
      error_handler -- <ErrorHandler object at 2002c090>
      log_critical_error -- <function log_critical_error at 0x2002c510>
      const -- <function>
      BLACK -- (0, 0, 0)
      sys -- <module 'sys'>
      ure -- <module 'ure'>
      ErrorHandler -- <class 'ErrorHandler'>
      version -- <module 'version' from 'version.py'>
      PROGRAM_EXECUTION_ERROR -- 0
    object <class 'ErrorHandler'> is of type type
      __module__ -- util.error_handler
      handle_user_program_error -- <function handle_user_program_error at 0x2002c060>
      handle_notify_error -- <function handle_notify_error at 0x2002c080>
      __qualname__ -- ErrorHandler
      handle_runtime_error -- <function handle_runtime_error at 0x2002c050>
      initialize -- <function initialize at 0x2002c040>
      _emit_runtime_error -- <function _emit_runtime_error at 0x20024eb0>
      _handle_error -- <function _handle_error at 0x2002c070>
    object <ErrorHandler object at 2002c090> is of type ErrorHandler
      __module__ -- util.error_handler
      handle_user_program_error -- <function handle_user_program_error at 0x2002c060>
      handle_notify_error -- <function handle_notify_error at 0x2002c080>
      __qualname__ -- ErrorHandler
      handle_runtime_error -- <function handle_runtime_error at 0x2002c050>
      initialize -- <function initialize at 0x2002c040>
      _emit_runtime_error -- <function _emit_runtime_error at 0x20024eb0>
      _handle_error -- <function _handle_error at 0x2002c070>
    object <module 'util.time' from 'util/time.mpy'> is of type module
      _STOPPED_AT -- 0
      _STARTED_AT -- 1680
      ticks_ms -- <function>
      __file__ -- util/time.mpy
      ticks_diff -- <function>
      __name__ -- util.time
      start_time -- <function start_time at 0x20021840>
      _RUNNING -- False
      get_time -- <function get_time at 0x20021830>
      reset_time -- <function reset_time at 0x20021460>
      stop_time -- <function stop_time at 0x20021850>
    object <module 'util.sensors' from 'util/sensors.mpy'> is of type module
      _PORTS -- [Port(A), Port(B), Port(C), Port(D), Port(E), Port(F)]
      LPF2_FLIPPER_COLOR -- 61
      LPF2_FLIPPER_MOTOR_MEDIUM -- 48
      sensor_data -- [[0, ()], [0, ()], [0, ()], [0, ()], [0, ()], [0, ()], (0, -805, 585), (3, 3, 0), (-3, 0, 54), '', 0]
      register_ports -- <function register_ports at 0x200219a0>
      _REVERSE_MODES -- {48: [3, 0, 1, 2], 65: [3, 0, 1, 2], 49: [3, 0, 1, 2], 75: [3, 0, 1, 2], 76: [3, 0, 1, 2], 61: [1, 0, 2, 3, 4], 62: [0], 63: [0, 1, -1, -1, 2]}
      LPF2_FLIPPER_MOTOR_LARGE -- 49
      LPF2_FLIPPER_DISTANCE -- 62
      _EVENT_MODE -- [[], [], [], [], [], []]
      __file__ -- util/sensors.mpy
      is_type -- <function is_type at 0x20021f40>
      LPF2_FLIPPER_MOTOR_SMALL -- 65
      battery_status -- [8.36, 100, True]
      set_display_sync -- <function set_display_sync at 0x20022170>
      _PORT_INDEX_MAP -- ['A', 'B', 'C', 'D', 'E', 'F', 'ACCELEROMETER', 'GYROSCOPE', 'POSITION', 'ORIENTATION', 'TIMER']
      get_sensor_value -- <function get_sensor_value at 0x20021f20>
      current_motion -- <function current_motion at 0x20022180>
      _PORT_TYPE -- [0, 0, 0, 0, 0, 0]
      get_time -- <function get_time at 0x20021830>
      LPF2_STONE_GREY_MOTOR_LARGE -- 76
      __name__ -- util.sensors
      orientation_to_number -- <function orientation_to_number at 0x20021330>
      const -- <function>
      hub -- <module 'hub'>
      _is_motor -- <function _is_motor at 0x20021ec0>
      _NO_DATA -- ()
      update_battery_status -- <function update_battery_status at 0x20022140>
      update_sensor_data -- <function update_sensor_data at 0x20022130>
      _type_change_handler -- <function _type_change_handler at 0x20022150>
      LPF2_STONE_GREY_MOTOR_MEDIUM -- 75
      _SYNC_DISPLAY -- False
      _DEFAULT_MODE -- {48: [(1, 0), (2, 2), (3, 1), (0, 0)], 65: [(1, 0), (2, 2), (3, 1), (1, 0)], 49: [(1, 0), (2, 2), (3, 1), (0, 0)], 75: [(1, 0), (2, 2), (3, 1), (0, 0)], 76: [(1, 0), (2, 2), (3, 1), (0, 0)], 61: [(1, 0), (0, 0), (5, 0), (5, 1), (5, 2)], 62: [(0, 0)], 63: [(0, 0), (1, 0), (4, 0)]}
      LPF2_FLIPPER_FORCE -- 63
      reset_to_default_mode -- <function reset_to_default_mode at 0x20022160>
      _MOTOR_TYPES -- [65, 48, 49, 75, 76]
    object <module 'util.storage' from 'util/storage.mpy'> is of type module
      _move_slot_lookup -- <function _move_slot_lookup at 0x20024dd0>
      get_storage_information -- <function get_storage_information at 0x20024d60>
      get_path -- <function get_path at 0x20024d30>
      uos -- <module 'uos'>
      __STORAGE_PATH__ -- ./projects
      move_slot -- <function move_slot at 0x20024dc0>
      _set_metadata -- <function _set_metadata at 0x20024e00>
      close_program -- <function close_program at 0x20024cd0>
      EEXIST -- 17
      PROGRAM_TYPE_PYTHON -- python
      __file__ -- util/storage.mpy
      write_local_name -- <function write_local_name at 0x20024db0>
      get_program_project_id -- <function get_program_project_id at 0x20024cf0>
      ENOENT -- 2
      set_force_reset -- <function set_force_reset at 0x20024e10>
      __FORCE_RESET_PATH__ -- ./reset
      read_local_name -- <function read_local_name at 0x20024da0>
      PROGRAM_TYPE_SCRATCH -- scratch
      generate_project_id -- <function generate_project_id at 0x20024d70>
      urandom -- <module 'urandom'>
      pop_force_reset -- <function pop_force_reset at 0x20024e20>
      __name__ -- util.storage
      _file_to_slotid -- <function _file_to_slotid at 0x20024e30>
      ure -- <module 'ure'>
      LOCAL_NAME -- /local_name.txt
      __META_PATH__ -- ./projects/.slots
      get_program_type -- <function get_program_type at 0x20024d00>
      get_used_slots -- <function get_used_slots at 0x20024d80>
      open_program -- <function open_program at 0x20024c60>
      _BT_PREFIX -- LEGO Hub@
      read_program -- <function read_program at 0x20024d90>
      clear_slot -- <function clear_slot at 0x20024d50>
      _ensure_folder_exists -- <function _ensure_folder_exists at 0x20024de0>
      __PROGRAM_PATH_EXT__ -- ./projects/{0}.py
      _get_metadata -- <function _get_metadata at 0x20024df0>
      __PROGRAM_PATH__ -- ./projects/{0}
    object <module 'util.scratch' from 'util/scratch.mpy'> is of type module
      tan -- <function tan at 0x2001faf0>
      sanitize_ports -- <function sanitize_ports at 0x20021350>
      color_to_number -- <function color_to_number at 0x200213c0>
      note_to_frequency -- <function note_to_frequency at 0x200213f0>
      clamp -- <function clamp at 0x20021250>
      NUMBER -- 0
      to_number -- <function to_number at 0x2001d660>
      number_color_to_rgb -- <function number_color_to_rgb at 0x200213e0>
      number_to_orientation -- <function number_to_orientation at 0x20021340>
      convert_animation_frame -- <function convert_animation_frame at 0x20021220>
      math -- <module 'math'>
      __file__ -- util/scratch.mpy
      color -- <module 'util.color' from 'util/color.mpy'>
      compare -- <function compare at 0x2001fae0>
      partition_image_str -- <function partition_image_str at 0x200212c0>
      NO_KEY -- -1
      VAR_DEFAULTS -- {0: 0, 1: '', 2: False}
      is_int -- <function is_int at 0x2001fad0>
      convert_brightness -- <function convert_brightness at 0x200212a0>
      to_boolean -- <function to_boolean at 0x2001d670>
      __name__ -- util.scratch
      orientation_to_number -- <function orientation_to_number at 0x20021330>
      number_to_color -- <function number_to_color at 0x200213d0>
      PAIR_REGEX -- <re 20021360>
      ure -- <module 'ure'>
      BOOLEAN -- 2
      ORIENTATIONS -- ('', 'front', 'back', 'up', 'down', 'rightside', 'leftside')
      sanitize_movement_ports -- <function sanitize_movement_ports at 0x20021390>
      adjust_brightness -- <function adjust_brightness at 0x200212b0>
      percent_to_int -- <function percent_to_int at 0x200213a0>
      percent_to_frequency -- <function percent_to_frequency at 0x200213b0>
      wrap_clamp -- <function wrap_clamp at 0x20021280>
      convert_image -- <function convert_image at 0x200212e0>
      get_variable -- <function get_variable at 0x20021400>
      pitch_to_freq -- <function pitch_to_freq at 0x20021410>
    object <module 'util.motor' from 'util/motor.mpy'> is of type module
      clamp_speed -- <function clamp_speed at 0x200348e0>
      __name__ -- util.motor
      dir_to_speed -- <function dir_to_speed at 0x20034930>
      __file__ -- util/motor.mpy
      clamp_power -- <function clamp_power at 0x20034970>
    object <module 'util.animations' from 'util/animations.mpy'> is of type module
      shift_out_to_top -- <generator>
      Image -- <class 'Image'>
      get_color_percentage -- <function get_color_percentage at 0x2001fab0>
      streaming_animation -- <function streaming_animation at 0x2003d850>
      shift_in_from_right -- <generator>
      shift_in_from_bottom_left -- <generator>
      shift_left -- <function shift_left at 0x2003d830>
      shift_out_to_bottom -- <generator>
      SHUTDOWN_FRAMES -- (Image('99999:90009:90009:90009:99999:'), Image('55555:57775:57075:57775:55555:'), Image('00000:09990:09090:09990:00000:'), Image('00000:05550:05750:05550:00000:'), Image('00000:00000:00900:00000:00000:'), Image('00000:00000:00500:00000:00000:'), Image('00000:00000:00000:00000:00000:'))
      shutdown_animation -- <function shutdown_animation at 0x2003d950>
      BLACK -- (0, 0, 0)
      __file__ -- util/animations.mpy
      led_fade_to -- <generator>
      led_fade_in_out -- <generator>
      shift_out_to_left -- <generator>
      utime -- <module 'utime'>
      DISPLAY_WIDTH -- 5
      __name__ -- util.animations
      download_animation -- <function download_animation at 0x2003d860>
      shift_in_from_left -- <generator>
      hub -- <module 'hub'>
      DIM_WHITE -- (135, 25, 10)
      BOOTUP_FRAMES -- (Image('00000:00000:09000:00000:00000:'), Image('00000:00000:07000:00000:00000:'), Image('00000:00000:07000:00009:00000:'), Image('00000:00000:07000:00007:00000:'), Image('00000:00000:07000:90007:00000:'), Image('00000:00000:07000:70007:00000:'), Image('00000:90000:07000:70007:00000:'), Image('00000:70000:07000:70007:00000:'), Image('00000:70000:07000:70007:00900:'), Image('00000:70000:07000:70007:00700:'), Image('00000:70900:07000:70007:00700:'), Image('00090:70800:07000:70007:00700:'), Image('00080:70800:07000:79007:00700:'), Image('00080:70700:07090:78007:00700:'), Image('00070:70700:07080:78007:90700:'), Image('09070:70700:07070:77007:80700:'), Image('08070:70700:07070:77007:80709:'), Image('08079:70700:07070:77007:70708:'), Image('07078:70700:07070:77907:70708:'), Image('07078:79700:07070:77707:70707:'), Image('07077:78700:07079:77707:70707:'), Image('07077:78700:07078:77707:79707:'), Image('07977:78700:07078:77707:78707:'), Image('07877:77700:07078:77797:78707:'), Image('07877:77709:07077:77787:78707:'), Image('07877:77708:97077:77787:77707:'), Image('07777:77708:87077:77787:77797:'), Image('07777:77798:87077:77777:77787:'), Image('97777:77787:87077:77777:77787:'), Image('87777:77787:87977:77777:77787:'), Image('99999:99999:99999:99999:99999:'), Image('77777:77777:77777:77777:77777:'), Image('66669:66669:66669:66669:66669:'), Image('55599:55595:55595:55595:55599:'), Image('44999:44949:44949:44949:44999:'), Image('39993:39393:39393:39393:39993:'), Image('09990:09090:09090:09090:09990:'))
      shift_right -- <function shift_right at 0x2003d840>
      bootup_animation -- <function bootup_animation at 0x2003d940>
      chain_animations -- <generator>
      shift_in_from_bottom -- <generator>
      bt_animation -- <generator>
      DISPLAY_HEIGHT -- 5
      shift_out_to_right -- <generator>
      color_percentage -- <function color_percentage at 0x2001fa10>
      shift_in_from_top_right -- <generator>
      shift_in_from_top -- <generator>
    object <class 'Image'> is of type type
      width -- <function>
      height -- <function>
      get_pixel -- <function>
      set_pixel -- <function>
      shift_left -- <function>
      shift_right -- <function>
      shift_up -- <function>
      shift_down -- <function>
      HEART -- Image(
        '09090:'
        '99999:'
        '99999:'
        '09990:'
        '00900:'
    )
      HEART_SMALL -- Image(
        '00000:'
        '09090:'
        '09990:'
        '00900:'
        '00000:'
    )
      HAPPY -- Image(
        '00000:'
        '09090:'
        '00000:'
        '90009:'
        '09990:'
    )
      SMILE -- Image(
        '00000:'
        '00000:'
        '00000:'
        '90009:'
        '09990:'
    )
      SAD -- Image(
        '00000:'
        '09090:'
        '00000:'
        '09990:'
        '90009:'
    )
      CONFUSED -- Image(
        '00000:'
        '09090:'
        '00000:'
        '09090:'
        '90909:'
    )
      ANGRY -- Image(
        '90009:'
        '09090:'
        '00000:'
        '99999:'
        '90909:'
    )
      ASLEEP -- Image(
        '00000:'
        '99099:'
        '00000:'
        '09990:'
        '00000:'
    )
      SURPRISED -- Image(
        '09090:'
        '00000:'
        '00900:'
        '09090:'
        '00900:'
    )
      SILLY -- Image(
        '90009:'
        '00000:'
        '99999:'
        '00909:'
        '00999:'
    )
      FABULOUS -- Image(
        '99999:'
        '99099:'
        '00000:'
        '09090:'
        '09990:'
    )
      MEH -- Image(
        '09090:'
        '00000:'
        '00090:'
        '00900:'
        '09000:'
    )
      YES -- Image(
        '00000:'
        '00009:'
        '00090:'
        '90900:'
        '09000:'
    )
      NO -- Image(
        '90009:'
        '09090:'
        '00900:'
        '09090:'
        '90009:'
    )
      CLOCK12 -- Image(
        '00900:'
        '00900:'
        '00900:'
        '00000:'
        '00000:'
    )
      CLOCK1 -- Image(
        '00090:'
        '00090:'
        '00900:'
        '00000:'
        '00000:'
    )
      CLOCK2 -- Image(
        '00000:'
        '00099:'
        '00900:'
        '00000:'
        '00000:'
    )
      CLOCK3 -- Image(
        '00000:'
        '00000:'
        '00999:'
        '00000:'
        '00000:'
    )
      CLOCK4 -- Image(
        '00000:'
        '00000:'
        '00900:'
        '00099:'
        '00000:'
    )
      CLOCK5 -- Image(
        '00000:'
        '00000:'
        '00900:'
        '00090:'
        '00090:'
    )
      CLOCK6 -- Image(
        '00000:'
        '00000:'
        '00900:'
        '00900:'
        '00900:'
    )
      CLOCK7 -- Image(
        '00000:'
        '00000:'
        '00900:'
        '09000:'
        '09000:'
    )
      CLOCK8 -- Image(
        '00000:'
        '00000:'
        '00900:'
        '99000:'
        '00000:'
    )
      CLOCK9 -- Image(
        '00000:'
        '00000:'
        '99900:'
        '00000:'
        '00000:'
    )
      CLOCK10 -- Image(
        '00000:'
        '99000:'
        '00900:'
        '00000:'
        '00000:'
    )
      CLOCK11 -- Image(
        '09000:'
        '09000:'
        '00900:'
        '00000:'
        '00000:'
    )
      ARROW_N -- Image(
        '00900:'
        '09990:'
        '90909:'
        '00900:'
        '00900:'
    )
      ARROW_NE -- Image(
        '00999:'
        '00099:'
        '00909:'
        '09000:'
        '90000:'
    )
      ARROW_E -- Image(
        '00900:'
        '00090:'
        '99999:'
        '00090:'
        '00900:'
    )
      ARROW_SE -- Image(
        '90000:'
        '09000:'
        '00909:'
        '00099:'
        '00999:'
    )
      ARROW_S -- Image(
        '00900:'
        '00900:'
        '90909:'
        '09990:'
        '00900:'
    )
      ARROW_SW -- Image(
        '00009:'
        '00090:'
        '90900:'
        '99000:'
        '99900:'
    )
      ARROW_W -- Image(
        '00900:'
        '09000:'
        '99999:'
        '09000:'
        '00900:'
    )
      ARROW_NW -- Image(
        '99900:'
        '99000:'
        '90900:'
        '00090:'
        '00009:'
    )
      GO_RIGHT -- Image(
        '09000:'
        '09900:'
        '09990:'
        '09900:'
        '09000:'
    )
      GO_LEFT -- Image(
        '00090:'
        '00990:'
        '09990:'
        '00990:'
        '00090:'
    )
      GO_UP -- Image(
        '00000:'
        '00900:'
        '09990:'
        '99999:'
        '00000:'
    )
      GO_DOWN -- Image(
        '00000:'
        '99999:'
        '09990:'
        '00900:'
        '00000:'
    )
      TRIANGLE -- Image(
        '00000:'
        '00900:'
        '09090:'
        '99999:'
        '00000:'
    )
      TRIANGLE_LEFT -- Image(
        '90000:'
        '99000:'
        '90900:'
        '90090:'
        '99999:'
    )
      CHESSBOARD -- Image(
        '09090:'
        '90909:'
        '09090:'
        '90909:'
        '09090:'
    )
      DIAMOND -- Image(
        '00900:'
        '09090:'
        '90009:'
        '09090:'
        '00900:'
    )
      DIAMOND_SMALL -- Image(
        '00000:'
        '00900:'
        '09090:'
        '00900:'
        '00000:'
    )
      SQUARE -- Image(
        '99999:'
        '90009:'
        '90009:'
        '90009:'
        '99999:'
    )
      SQUARE_SMALL -- Image(
        '00000:'
        '09990:'
        '09090:'
        '09990:'
        '00000:'
    )
      RABBIT -- Image(
        '90900:'
        '90900:'
        '99990:'
        '99090:'
        '99990:'
    )
      COW -- Image(
        '90009:'
        '90009:'
        '99999:'
        '09990:'
        '00900:'
    )
      MUSIC_CROTCHET -- Image(
        '00900:'
        '00900:'
        '00900:'
        '99900:'
        '99900:'
    )
      MUSIC_QUAVER -- Image(
        '00900:'
        '00990:'
        '00909:'
        '99900:'
        '99900:'
    )
      MUSIC_QUAVERS -- Image(
        '09999:'
        '09009:'
        '09009:'
        '99099:'
        '99099:'
    )
      PITCHFORK -- Image(
        '90909:'
        '90909:'
        '99999:'
        '00900:'
        '00900:'
    )
      XMAS -- Image(
        '00900:'
        '09990:'
        '00900:'
        '09990:'
        '99999:'
    )
      PACMAN -- Image(
        '09999:'
        '99090:'
        '99900:'
        '99990:'
        '09999:'
    )
      TARGET -- Image(
        '00900:'
        '09990:'
        '99099:'
        '09990:'
        '00900:'
    )
      ALL_CLOCKS -- (Image('00900:00900:00900:00000:00000:'), Image('00090:00090:00900:00000:00000:'), Image('00000:00099:00900:00000:00000:'), Image('00000:00000:00999:00000:00000:'), Image('00000:00000:00900:00099:00000:'), Image('00000:00000:00900:00090:00090:'), Image('00000:00000:00900:00900:00900:'), Image('00000:00000:00900:09000:09000:'), Image('00000:00000:00900:99000:00000:'), Image('00000:00000:99900:00000:00000:'), Image('00000:99000:00900:00000:00000:'), Image('09000:09000:00900:00000:00000:'))
      ALL_ARROWS -- (Image('00900:09990:90909:00900:00900:'), Image('00999:00099:00909:09000:90000:'), Image('00900:00090:99999:00090:00900:'), Image('90000:09000:00909:00099:00999:'), Image('00900:00900:90909:09990:00900:'), Image('00009:00090:90900:99000:99900:'), Image('00900:09000:99999:09000:00900:'), Image('99900:99000:90900:00090:00009:'))
      TSHIRT -- Image(
        '99099:'
        '99999:'
        '09990:'
        '09990:'
        '09990:'
    )
      ROLLERSKATE -- Image(
        '00099:'
        '00099:'
        '99999:'
        '99999:'
        '09090:'
    )
      DUCK -- Image(
        '09900:'
        '99900:'
        '09999:'
        '09990:'
        '00000:'
    )
      HOUSE -- Image(
        '00900:'
        '09990:'
        '99999:'
        '09990:'
        '09090:'
    )
      TORTOISE -- Image(
        '00000:'
        '09990:'
        '99999:'
        '09090:'
        '00000:'
    )
      BUTTERFLY -- Image(
        '99099:'
        '99999:'
        '00900:'
        '99999:'
        '99099:'
    )
      STICKFIGURE -- Image(
        '00900:'
        '99999:'
        '00900:'
        '09090:'
        '90009:'
    )
      GHOST -- Image(
        '99999:'
        '90909:'
        '99999:'
        '99999:'
        '90909:'
    )
      SWORD -- Image(
        '00900:'
        '00900:'
        '00900:'
        '09990:'
        '00900:'
    )
      GIRAFFE -- Image(
        '99000:'
        '09000:'
        '09000:'
        '09990:'
        '09090:'
    )
      SKULL -- Image(
        '09990:'
        '90909:'
        '99999:'
        '09990:'
        '09990:'
    )
      UMBRELLA -- Image(
        '09990:'
        '99999:'
        '00900:'
        '90900:'
        '09900:'
    )
      SNAKE -- Image(
        '99000:'
        '99099:'
        '09090:'
        '09990:'
        '00000:'
    )
    object <module 'util.color' from 'util/color.mpy'> is of type module
      VIOLET -- (255, 8, 23)
      GREEN -- (0, 195, 0)
      __file__ -- util/color.mpy
      color_percentage -- <function color_percentage at 0x2001fa10>
      RED -- (255, 0, 0)
      BLACK -- (0, 0, 0)
      YELLOW -- (255, 35, 0)
      BLUE -- (0, 0, 80)
      AZURE -- (0, 57, 57)
      rgb_percentage -- <function rgb_percentage at 0x2001faa0>
      __name__ -- util.color
      DIM_WHITE -- (135, 25, 10)
      get_rgb_percentage -- <function get_rgb_percentage at 0x2001fac0>
      get_color_percentage -- <function get_color_percentage at 0x2001fab0>
      WHITE -- (255, 70, 35)
    object <module 'util.resetter' from 'util/resetter.mpy'> is of type module
      RTTimer -- <class 'RTTimer'>
      ticks_diff -- <function>
      __name__ -- util.resetter
      _STARTED_AT -- 3380
      hub -- <module 'hub'>
      sleep_ms -- <function>
      schedule -- <function>
      __file__ -- util/resetter.mpy
      ticks_ms -- <function>
      wait_until_ready_after_restart -- <function wait_until_ready_after_restart at 0x2002b7d0>
    object <class 'RTTimer'> is of type type
      __qualname__ -- RTTimer
      __repl_reset -- <function __repl_reset at 0x2002cca0>
      repl_reset -- <function repl_reset at 0x2002cce0>
      __module__ -- util.resetter
      start -- <function start at 0x2002ccc0>
      __init__ -- <function __init__ at 0x2002cc90>
