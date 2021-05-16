:mod:`_api.forcesensor` -- force sensor functions API
=====================================================

.. module:: _api.forcesensor
   :synopsis: force sensor functions API

This module contains the API functions for user interaction with a force
sensor brick.  (Included with Spike Prime but not in the Robot Inventor kit.)

This module is imported by the `mindstorms` and `spike` modules so that the API
can be branded appropriately in documentation (i.e. so that Mindstorms docs can
tell you to import mindstorms, and Spike Prime docs can tell you to import
spike).

Functions
---------

.. function:: _get_port_device(???)

   ???

.. function:: _is_force_sensor(???)

   ???

ForceSensor Class
-----------------
.. class:: ForceSensor(???)

   ???

   **Methods**

   .. method:: wait_until_released(???)

      ???

   .. method:: is_pressed(???)

      ???

   .. method:: wait_until_pressed(???)

      ???

   .. method:: _is_pressed(???)

      ???

   .. method:: get_force_percentage(???)

      ???

   .. method:: get_force_newton(???)

      ???

Imports
-------
* Function `_api.util.newSensorDisconnectedError`
* Function `utime.sleep_ms`
* Function `util.sensors.is_type`
* Constant `util.constants.LPF2_FLIPPER_FORCE` = 63
* Constant `util.constants.PORTS` = {'C': Port(C), 'B': Port(B), 'D': Port(D), 'E': Port(E), 'A': Port(A), 'F': Port(F)}
