:mod:`_api.motorpair` -- paired motor functions API
===================================================

.. module:: _api.motorpair
   :synopsis: paired motor functions API

This module contains the API functions for user interaction with pairs of
motors.  (Motors linked together in code to make dual-wheel vehicles easy to
operate.)

This module is imported by the `mindstorms` and `spike` modules so that the API
can be branded appropriately in documentation (i.e. so that Mindstorms docs can
tell you to import mindstorms, and Spike Prime docs can tell you to import
spike).

Functions
---------

.. function:: clamp_steering(???)

   ???

.. function:: _is_motor(???)

   ???

Constants
---------

.. data:: _DISCONNECTED_ERROR
   :value: One or both of the motors has been disconnected.

   ???

.. data:: _MOTOR_PAIRING_ERROR
   :value: The motors could not be paired.

   ???

MotorPair Class
---------------
.. class:: MotorPair(???)

   ???

   **Methods**

   .. method:: get_default_speed(???)

      ???

   .. method:: set_default_speed(???)

      ???

   .. method:: set_stop_action(???)

      ???

   .. method:: set_motor_rotation(???)

      ???

   .. method:: start(???)

      ???

   .. method:: start_at_power(???)

      ???

   .. method:: start_tank(???)

      ???

   .. method:: start_tank_at_power(???)

      ???

   .. method:: stop(???)

      ???

   .. method:: move(???)

      ???

   .. method:: move_tank(???)

      ???

   .. method:: _move_with_speed(???)

      ???

   .. method:: was_interrupted(???)

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

   .. data:: CM
      :value: cm

      ???

   .. data:: IN
      :value: in

      ???

   .. data:: DEGREES
      :value: degrees

      ???

   .. data:: SECONDS
      :value: seconds

      ???

   .. data:: ROTATIONS
      :value: rotations

      ???

Imports
-------
* Function `_api.util.wait_for_async`
* Function `system.movewrapper.from_steering`
* Function `util.motor.clamp_power`
* Function `util.motor.clamp_speed`
* Constant `system.system` = <Main System object>
* Constant `util.constants.PORTS` = {'C': Port(C), 'B': Port(B), 'D': Port(D), 'E': Port(E), 'A': Port(A), 'F': Port(F)}
