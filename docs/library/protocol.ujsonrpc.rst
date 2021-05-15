:mod:`protocol.ujsonrpc` -- ???
===============================

.. module:: protocol.ujsonrpc
   :synopsis: ???

???

Constants
---------

.. data:: _ID_PREFIX
   :value: b'{"i":'

   ???

.. data:: _PARAMS
   :value: b',"p":'

   ???

.. data:: _ID
   :value: b',"i":'

   ???

.. data:: _ERROR
   :value: b',"e":'

   ???

.. data:: _SUFFIX
   :value: b'}\r'

   ???

.. data:: _SUSPENDED_MSG_PATH_
   :value: ./suspended_msg

   ???

.. data:: _CARRIAGE_RETURN
   :value: b'\r'

   ???

.. data:: NO_RESPONSE
   :value: {}

   ???

.. data:: _METHOD_PREFIX
   :value: b'{"m":'

   ???

.. data:: _RESPONSE
   :value: b',"r":'

   ???

JSONRPC Class
-------------
.. class:: JSONRPC(???)

   ???

   *Methods*

   .. method:: _pop_suspend_message(???)

      ???

   .. method:: clear_methods(???)

      ???

   .. method:: emit_large(???)

      ???

   .. method:: reply(???)

      ???

   .. method:: _handle_message(???)

      ???

   .. method:: suspend_current_message(???)

      ???

   .. method:: error(???)

      ???

   .. method:: add_method(???)

      ???

   .. method:: parse_chunk(???)

      ???

   .. method:: cancel_call(???)

      ???

   .. method:: parse_buffer(???)

      ???

   .. method:: emit(???)

      ???

   .. method:: call(???)

      ???

   .. method:: resume_suspended_msg(???)

      ???

   .. property:: stream

      ???

   *Fields*
   .. data:: pending
      ???  Default value = {}

   *Method Dictionary*

   .. data:: methods
      :value: {'scratch.display_animation': <bound_method>, 'scratch.motor_pwm': <bound_method>, 'set_hub_name': <bound_method>, 'scratch.play_sound': <bound_method>, 'get_linegraph_monitor_info': <bound_method>, 'reset_program_time': <bound_method>, 'set_port_mode': <bound_method>, 'scratch.motor_go_direction_to_position': <bound_method>, 'sync_display': <bound_method>, 'scratch.reset_yaw': <bound_method>, 'scratch.when_sensor_changed': <bound_method>, 'scratch.motor_run_timed': <bound_method>, 'scratch.move_stop': <bound_method>, 'program_execute': <bound_method>, 'scratch.when_sensor_force_released': <bound_method>, 'remove_project': <bound_method>, 'start_write_program': <bound_method>, 'get_storage_status': <bound_method>, 'scratch.sound_beep': <bound_method>, 'scratch.sound_off': <bound_method>, 'scratch.display_set_pixel': <bound_method>, 'scratch.ultrasonic_light_up': <bound_method>, 'scratch.motor_start': <bound_method>, 'delete_linegraph_file': <bound_method>, 'program_terminate': <bound_method>, 'scratch.display_rotate_direction': <bound_method>, 'scratch.display_image': <bound_method>, 'scratch.move_start_powers': <bound_method>, 'scratch.sound_beep_for_time': <bound_method>, 'get_program_time': <bound_method>, 'move_project': <bound_method>, 'get_hub_info': <bound_method>, 'scratch.center_button_lights': <bound_method>, 'scratch.motor_position': <bound_method>, 'scratch.move_start_speeds': <bound_method>, 'program_modechange': <bound_method>, 'scratch.move_tank_degrees': <bound_method>, 'scratch.motor_go_to_relative_position': <bound_method>, 'write_package': <bound_method>, 'scratch.display_rotate_orientation': <bound_method>, 'scratch.display_image_for': <bound_method>, 'scratch.when_sensor_force_bumped': <bound_method>, 'scratch.move_tank_time': <bound_method>, 'scratch.wait_gesture': <bound_method>, 'scratch.motor_run_for_degrees': <bound_method>, 'trigger_current_state': <bound_method>, 'scratch.display_clear': <bound_method>, 'scratch.motor_stop': <bound_method>, 'scratch.motor_adjust_offset': <bound_method>, 'start_program_time': <bound_method>, 'scratch.motor_set_position': <bound_method>, 'scratch.display_text': <bound_method>, 'get_linegraph_monitor_package': <bound_method>}

      Seems to be a lookup table binding scratch API commands to specific
      methods?

Imports
-------
* Module `ujson`
* Module `uos`
* Module `urandom`
* Function `ubinascii.b2a_base64`
* Function `utime.sleep_ms`
* Constant `uerrno.ENOENT` = 2
* Class `uio.StringIO`