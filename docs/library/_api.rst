:mod:`_api` -- user API
=======================

This module contains most of the API functions that you're meant to call to
operate the system as a user.  The module itself is actually a backend to
modules `mindstorms` and `spike`, which are nearly identical and seem to exist
mainly in order to correctly brand the Hub in documentation (i.e. so that
Mindstorms docs can tell you to import mindstorms, and Spike Prime docs can
tell you to import spike).

One interesting note is that module ``large_technic_hub`` only seems to appear
in this module after you've imported either `mindstorms` or `spike`, so it's
probably better to just use one of those unless you have very odd requirements.

Raw module data
---------------

::

    object <module '_api' from '_api/__init__.mpy'> is of type module
      distancesensor -- <module '_api.distancesensor' from '_api/distancesensor.mpy'>
      DistanceSensor -- <class 'DistanceSensor'>
      forcesensor -- <module '_api.forcesensor' from '_api/forcesensor.mpy'>
      colorsensor -- <module '_api.colorsensor' from '_api/colorsensor.mpy'>
      __name__ -- _api
      motionsensor -- <module '_api.motionsensor' from '_api/motionsensor.mpy'>
      StatusLight -- <class 'StatusLight'>
      statuslight -- <module '_api.statuslight' from '_api/statuslight.mpy'>
      Motor -- <class 'Motor'>
      Button -- <class 'Button'>
      motorpair -- <module '_api.motorpair' from '_api/motorpair.mpy'>
      MotorPair -- <class 'MotorPair'>
      large_technic_hub -- <module '_api.large_technic_hub' from '_api/large_technic_hub.mpy'>
      lightmatrix -- <module '_api.lightmatrix' from '_api/lightmatrix.mpy'>
      motor -- <module '_api.motor' from '_api/motor.mpy'>
      util -- <module '_api.util' from '_api/util.mpy'>
      __file__ -- _api/__init__.mpy
      speaker -- <module '_api.speaker' from '_api/speaker.mpy'>
      LightMatrix -- <class 'LightMatrix'>
      ColorSensor -- <class 'ColorSensor'>
      ForceSensor -- <class 'ForceSensor'>
      app -- <module '_api.app' from '_api/app.mpy'>
      button -- <module '_api.button' from '_api/button.mpy'>
      Speaker -- <class 'Speaker'>
      __path__ -- _api
      App -- <class 'App'>
      MotionSensor -- <class 'MotionSensor'>
    object <module '_api.distancesensor' from '_api/distancesensor.mpy'> is of type module
      is_type -- <function is_type at 0x20021f40>
      LPF2_FLIPPER_DISTANCE -- 62
      __name__ -- _api.distancesensor
      PORTS -- {'C': Port(C), 'B': Port(B), 'D': Port(D), 'E': Port(E), 'A': Port(A), 'F': Port(F)}
      DistanceSensor -- <class 'DistanceSensor'>
      sleep_ms -- <function>
      __file__ -- _api/distancesensor.mpy
      newSensorDisconnectedError -- <function newSensorDisconnectedError at 0x2001fe80>
      clamp -- <function clamp at 0x20021250>
    object <class 'DistanceSensor'> is of type type
      PERCENT -- %
      get_distance_inches -- <function get_distance_inches at 0x20030270>
      CM -- cm
      _set_range_mode -- <function _set_range_mode at 0x2002f620>
      _LONG_RANGE_MODE -- (0, [(0, 0)])
      get_distance_percentage -- <function get_distance_percentage at 0x20030290>
      _SHORT_RANGE_MODE -- (1, [(1, 0)])
      __module__ -- _api.distancesensor
      _set_mode -- <function _set_mode at 0x200301e0>
      IN -- in
      light_up_all -- <function light_up_all at 0x200302f0>
      wait_for_distance_farther_than -- <function wait_for_distance_farther_than at 0x200302b0>
      _LIGHT_MODE -- (5, [(5, 0), (5, 1), (5, 2), (5, 3)])
      __qualname__ -- DistanceSensor
      __init__ -- <function __init__ at 0x2002f660>
      get_distance_cm -- <function get_distance_cm at 0x20030250>
      wait_for_distance_closer_than -- <function wait_for_distance_closer_than at 0x200302d0>
      _is_distance_sensor -- <function _is_distance_sensor at 0x2002f640>
      light_up -- <function light_up at 0x2002fc40>
    object <module '_api.forcesensor' from '_api/forcesensor.mpy'> is of type module
      is_type -- <function is_type at 0x20021f40>
      _get_port_device -- <function _get_port_device at 0x2001feb0>
      __name__ -- _api.forcesensor
      LPF2_FLIPPER_FORCE -- 63
      ForceSensor -- <class 'ForceSensor'>
      _is_force_sensor -- <function _is_force_sensor at 0x2001fea0>
      sleep_ms -- <function>
      __file__ -- _api/forcesensor.mpy
      newSensorDisconnectedError -- <function newSensorDisconnectedError at 0x2001fe80>
      PORTS -- {'C': Port(C), 'B': Port(B), 'D': Port(D), 'E': Port(E), 'A': Port(A), 'F': Port(F)}
    object <class 'ForceSensor'> is of type type
      wait_until_released -- <function wait_until_released at 0x200208c0>
      is_pressed -- <function is_pressed at 0x20020840>
      __module__ -- _api.forcesensor
      wait_until_pressed -- <function wait_until_pressed at 0x200208b0>
      _is_pressed -- <function _is_pressed at 0x20020820>
      __init__ -- <function __init__ at 0x200207e0>
      __qualname__ -- ForceSensor
      get_force_percentage -- <function get_force_percentage at 0x20020830>
      get_force_newton -- <function get_force_newton at 0x20020850>
    object <module '_api.colorsensor' from '_api/colorsensor.mpy'> is of type module
      _AMBIENT_MODE -- (2, [(2, 0)])
      _is_color_sensor -- <function _is_color_sensor at 0x20029080>
      __file__ -- _api/colorsensor.mpy
      _COLORLIST -- ['black', 'violet', None, 'blue', 'cyan', 'green', None, 'yellow', None, 'red', 'white']
      is_type -- <function is_type at 0x20021f40>
      _get_port_device -- <function _get_port_device at 0x200291f0>
      ColorSensor -- <class 'ColorSensor'>
      sleep_ms -- <function>
      get_sensor_value -- <function get_sensor_value at 0x20021f20>
      __name__ -- _api.colorsensor
      _LIGHT_MODE -- (3, [(3, 0), (3, 1), (3, 2)])
      PORTS -- {'C': Port(C), 'B': Port(B), 'D': Port(D), 'E': Port(E), 'A': Port(A), 'F': Port(F)}
      newSensorDisconnectedError -- <function newSensorDisconnectedError at 0x2001fe80>
      clamp -- <function clamp at 0x20021250>
      _COMBI_MODE -- ([(1, 0), (0, 0), (5, 0), (5, 1), (5, 2), (5, 3)],)
      LPF2_FLIPPER_COLOR -- 61
    object <class 'ColorSensor'> is of type type
      light_up_all -- <function light_up_all at 0x2002a320>
      light_up -- <function light_up at 0x20029710>
      get_red -- <function get_red at 0x200296a0>
      get_rgb_intensity -- <function get_rgb_intensity at 0x20029690>
      __qualname__ -- ColorSensor
      get_reflected_light -- <function get_reflected_light at 0x20029620>
      get_green -- <function get_green at 0x200296b0>
      get_blue -- <function get_blue at 0x200296c0>
      get_ambient_light -- <function get_ambient_light at 0x200296d0>
      _set_mode -- <function _set_mode at 0x200295f0>
      __init__ -- <function __init__ at 0x20029680>
      get_color -- <function get_color at 0x20029610>
      wait_until_color -- <function wait_until_color at 0x200296e0>
      __module__ -- _api.colorsensor
      _get_color -- <function _get_color at 0x200294e0>
      wait_for_new_color -- <function wait_for_new_color at 0x200296f0>
    object <module '_api.motionsensor' from '_api/motionsensor.mpy'> is of type module
      hub -- <module 'hub'>
      __name__ -- _api.motionsensor
      MotionSensor -- <class 'MotionSensor'>
      __file__ -- _api/motionsensor.mpy
      sleep_ms -- <function>
    object <class 'MotionSensor'> is of type type
      FRONT -- front
      get_pitch_angle -- <function get_pitch_angle at 0x200228d0>
      FALLING -- falling
      SHAKEN -- shaken
      DOUBLE_TAPPED -- doubletapped
      get_gesture -- <function get_gesture at 0x20022b30>
      RIGHT_SIDE -- rightside
      wait_for_new_orientation -- <function wait_for_new_orientation at 0x20022ab0>
      get_orientation -- <function get_orientation at 0x20022a40>
      reset_yaw_angle -- <function reset_yaw_angle at 0x20022a00>
      __module__ -- _api.motionsensor
      TAPPED -- tapped
      was_gesture -- <function was_gesture at 0x20022c90>
      wait_for_new_gesture -- <function wait_for_new_gesture at 0x20022ce0>
      __qualname__ -- MotionSensor
      __init__ -- <function __init__ at 0x20022900>
      DOWN -- down
      get_roll_angle -- <function get_roll_angle at 0x20022940>
      LEFT_SIDE -- leftside
      get_yaw_angle -- <function get_yaw_angle at 0x20022990>
      BACK -- back
      UP -- up
    object <module '_api.statuslight' from '_api/statuslight.mpy'> is of type module
      hub -- <module 'hub'>
      __name__ -- _api.statuslight
      StatusLight -- <class 'StatusLight'>
      __file__ -- _api/statuslight.mpy
      _COLORMAP -- {'white': 10, 'pink': 1, 'blue': 3, 'yellow': 7, 'orange': 8, 'violet': 2, 'azure': 4, 'red': 9, 'green': 6, 'cyan': 5, 'black': 0}
    object <class 'StatusLight'> is of type type
      __module__ -- _api.statuslight
      on -- <function on at 0x2001e630>
      off -- <function off at 0x2001e450>
      __qualname__ -- StatusLight
    object <module '_api.motor' from '_api/motor.mpy'> is of type module
      hub -- <module 'hub'>
      Motor -- <class 'Motor'>
      __file__ -- _api/motor.mpy
      is_type -- <function is_type at 0x20021f40>
      _is_motor -- <function _is_motor at 0x20034e60>
      sleep_ms -- <function>
      clamp_speed -- <function clamp_speed at 0x200348e0>
      system -- <System object at 20033150>
      __name__ -- _api.motor
      PORTS -- {'C': Port(C), 'B': Port(B), 'D': Port(D), 'E': Port(E), 'A': Port(A), 'F': Port(F)}
      wait_for_async -- <function wait_for_async at 0x2001fe90>
      MOTOR_TYPES -- (65, 48, 49, 75, 76)
      newSensorDisconnectedError -- <function newSensorDisconnectedError at 0x2001fe80>
      clamp_power -- <function clamp_power at 0x20034970>
    object <class 'Motor'> is of type type
      run_for_rotations -- <function run_for_rotations at 0x20036030>
      BRAKE -- brake
      set_stall_detection -- <function set_stall_detection at 0x200355a0>
      stop -- <function stop at 0x20035c30>
      set_stop_action -- <function set_stop_action at 0x20035190>
      HOLD -- hold
      run_to_degrees_counted -- <function run_to_degrees_counted at 0x200356a0>
      COAST -- coast
      was_stalled -- <function was_stalled at 0x20035e10>
      get_degrees_counted -- <function get_degrees_counted at 0x200350a0>
      start_at_power -- <function start_at_power at 0x20035ac0>
      start -- <function start at 0x200361d0>
      get_position -- <function get_position at 0x20034c40>
      was_interrupted -- <function was_interrupted at 0x20035d60>
      __module__ -- _api.motor
      run_to_position -- <function run_to_position at 0x20035dc0>
      run_for_seconds -- <function run_for_seconds at 0x200361b0>
      set_degrees_counted -- <function set_degrees_counted at 0x200350b0>
      set_default_speed -- <function set_default_speed at 0x20035140>
      get_speed -- <function get_speed at 0x20035010>
      __qualname__ -- Motor
      __init__ -- <function __init__ at 0x20034df0>
      get_default_speed -- <function get_default_speed at 0x200350c0>
      run_for_degrees -- <function run_for_degrees at 0x20036010>
    object <module '_api.button' from '_api/button.mpy'> is of type module
      Button -- <class 'Button'>
      __name__ -- _api.button
      __file__ -- _api/button.mpy
    object <class 'Button'> is of type type
      __init__ -- <function __init__ at 0x2001d8a0>
      was_pressed -- <function was_pressed at 0x2001d8d0>
      wait_until_pressed -- <function wait_until_pressed at 0x2001d8b0>
      __qualname__ -- Button
      wait_until_released -- <function wait_until_released at 0x2001d8c0>
      is_pressed -- <function is_pressed at 0x2001d890>
      __module__ -- _api.button
    object <module '_api.motorpair' from '_api/motorpair.mpy'> is of type module
      __file__ -- _api/motorpair.mpy
      clamp_steering -- <function clamp_steering at 0x2003aab0>
      _is_motor -- <function _is_motor at 0x20039270>
      MotorPair -- <class 'MotorPair'>
      _DISCONNECTED_ERROR -- One or both of the motors has been disconnected.
      from_steering -- <function from_steering at 0x20032ff0>
      clamp_speed -- <function clamp_speed at 0x200348e0>
      system -- <System object at 20033150>
      __name__ -- _api.motorpair
      PORTS -- {'C': Port(C), 'B': Port(B), 'D': Port(D), 'E': Port(E), 'A': Port(A), 'F': Port(F)}
      wait_for_async -- <function wait_for_async at 0x2001fe90>
      clamp_power -- <function clamp_power at 0x20034970>
      _MOTOR_PAIRING_ERROR -- The motors could not be paired.
    object <class 'MotorPair'> is of type type
      BRAKE -- brake
      DEGREES -- degrees
      stop -- <function stop at 0x200397b0>
      set_stop_action -- <function set_stop_action at 0x20039eb0>
      start_tank -- <function start_tank at 0x2003a5e0>
      set_motor_rotation -- <function set_motor_rotation at 0x2003bff0>
      HOLD -- hold
      COAST -- coast
      IN -- in
      start -- <function start at 0x2003bfd0>
      start_at_power -- <function start_at_power at 0x2003c050>
      CM -- cm
      start_tank_at_power -- <function start_tank_at_power at 0x2003aa40>
      move_tank -- <function move_tank at 0x2003c030>
      was_interrupted -- <function was_interrupted at 0x2003a3d0>
      move -- <function move at 0x2003bfb0>
      SECONDS -- seconds
      __module__ -- _api.motorpair
      __qualname__ -- MotorPair
      set_default_speed -- <function set_default_speed at 0x20039dc0>
      ROTATIONS -- rotations
      _move_with_speed -- <function _move_with_speed at 0x2003be10>
      __init__ -- <function __init__ at 0x200396d0>
      get_default_speed -- <function get_default_speed at 0x200399a0>
    object <module '_api.lightmatrix' from '_api/lightmatrix.mpy'> is of type module
      hub -- <module 'hub'>
      LightMatrix -- <class 'LightMatrix'>
      __name__ -- _api.lightmatrix
      __file__ -- _api/lightmatrix.mpy
    object <class 'LightMatrix'> is of type type
      show_image -- <function show_image at 0x2001cae0>
      off -- <function off at 0x2001cb00>
      write -- <function write at 0x2001cb40>
      __module__ -- _api.lightmatrix
      set_pixel -- <function set_pixel at 0x2001cb20>
      __qualname__ -- LightMatrix
    object <module '_api.util' from '_api/util.mpy'> is of type module
      __name__ -- _api.util
      wait_for_async -- <function wait_for_async at 0x2001fe90>
      __file__ -- _api/util.mpy
      newSensorDisconnectedError -- <function newSensorDisconnectedError at 0x2001fe80>
      utime -- <module 'utime'>
    object <module '_api.speaker' from '_api/speaker.mpy'> is of type module
      hub -- <module 'hub'>
      system -- <System object at 20033150>
      __name__ -- _api.speaker
      __file__ -- _api/speaker.mpy
      wait_for_async -- <function wait_for_async at 0x2001fe90>
      Speaker -- <class 'Speaker'>
    object <class 'Speaker'> is of type type
      start_beep -- <function start_beep at 0x200254f0>
      beep -- <function beep at 0x20025140>
      set_volume -- <function set_volume at 0x20023c90>
      __qualname__ -- Speaker
      get_volume -- <function get_volume at 0x20023c70>
      stop -- <function stop at 0x20023bd0>
      __module__ -- _api.speaker
    object <module '_api.app' from '_api/app.mpy'> is of type module
      BT_VCP -- BT_VCP(0)
      __name__ -- _api.app
      ticks_diff -- <function>
      JSONRPC -- <class 'JSONRPC'>
      USB_VCP -- USB_VCP(0)
      _NOT_CONNECTED_ERROR -- The programming app is not connected to the hub.
      ticks_ms -- <function>
      __file__ -- _api/app.mpy
      App -- <class 'App'>
    object <class 'App'> is of type type
      __qualname__ -- App
      play_sound -- <function play_sound at 0x2002c010>
      _play_sound -- <function _play_sound at 0x2002aa30>
      __module__ -- _api.app
      start_sound -- <function start_sound at 0x2002bfd0>
      __init__ -- <function __init__ at 0x2002aa70>
    object <module '_api.large_technic_hub' from '_api/large_technic_hub.mpy'> is of type module
      LightMatrix -- <class 'LightMatrix'>
      MotionSensor -- <class 'MotionSensor'>
      __name__ -- _api.large_technic_hub
      StatusLight -- <class 'StatusLight'>
      Speaker -- <class 'Speaker'>
      hub -- <module 'hub'>
      LargeTechnicHub -- <class 'LargeTechnicHub'>
      __file__ -- _api/large_technic_hub.mpy
      Button -- <class 'Button'>
    object <class 'LargeTechnicHub'> is of type type
      PORT_B -- B
      PORT_A -- A
      status_light -- <property>
      _left_button -- <Button object at 2003c900>
      PORT_E -- E
      PORT_D -- D
      PORT_F -- F
      __module__ -- _api.large_technic_hub
      right_button -- <property>
      _motion_sensor -- <MotionSensor object at 2003c9f0>
      _status_light -- <StatusLight object at 2003c8c0>
      _right_button -- <Button object at 2003c950>
      __qualname__ -- LargeTechnicHub
      _light_matrix -- <LightMatrix object at 2003c8d0>
      speaker -- <property>
      left_button -- <property>
      _speaker -- <Speaker object at 2003cae0>
      motion_sensor -- <property>
      light_matrix -- <property>
      PORT_C -- C