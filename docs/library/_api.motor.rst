:mod:`_api.motor` -- motor functions API
========================================

.. module:: _api.motor
   :synopsis: motor functions API

This module contains the API functions for user interaction with a motor brick.

This module is imported by the `mindstorms` and `spike` modules so that the API
can be branded appropriately in documentation (i.e. so that Mindstorms docs can
tell you to import mindstorms, and Spike Prime docs can tell you to import
spike).

Functions
---------

.. function:: _is_motor(???)

   ???


Motor Class
-----------
.. class:: Motor(???)

   ???

   **Methods**

   .. method:: set_degrees_counted(???)

      ???

   .. method:: set_default_speed(???)

      ???

   .. method:: set_stop_action(???)

      ???

   .. method:: set_stall_detection(???)

      ???

   .. method:: get_position(???)

      ???

   .. method:: get_speed(???)

      ???

   .. method:: get_degrees_counted(???)

      ???

   .. method:: get_default_speed(???)

      ???

   .. method:: run_to_degrees_counted(???)

      ???

   .. method:: run_to_position(???)

      ???

   .. method:: run_for_degrees(???)

      ???

   .. method:: run_for_rotations(???)

      ???

   .. method:: run_for_seconds(???)

      ???

   .. method:: was_stalled(???)

      ???

   .. method:: was_interrupted(???)

      ???

   .. method:: start_at_power(???)

      ???

   .. method:: start(???)

      ???

   .. method:: stop(???)

      ???

   **Constants**

   .. data:: BRAKE
      :value: brake

      ???

   .. data:: HOLD
      :value: hold

      ???

   .. data:: COAST
      :value: coast

      ???

Imports
-------
* Module `hub`
* Function `_api.util.newSensorDisconnectedError`
* Function `_api.util.wait_for_async`
* Function `utime.sleep_ms`
* Function `util.motor.clamp_power`
* Function `util.motor.clamp_speed`
* Function `util.sensors.is_type`
* Constant `system.system` = <Main System object>
* Constant `util.constants.MOTOR_TYPES = (65, 48, 49, 75, 76)
* Constant `util.constants.PORTS` = {'C': Port(C), 'B': Port(B), 'D': Port(D), 'E': Port(E), 'A': Port(A), 'F': Port(F)}
