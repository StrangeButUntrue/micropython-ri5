:mod:`_api.motionsensor` -- motion sensor functions API
=======================================================

.. module:: _api.motionsensor
   :synopsis: motion sensor functions API

This module contains the API functions for user interaction with the motion
sensor inside the Hub.

This module is imported by the `mindstorms` and `spike` modules so that the API
can be branded appropriately in documentation (i.e. so that Mindstorms docs can
tell you to import mindstorms, and Spike Prime docs can tell you to import
spike).

MotionSensor Class
---------------
.. class:: MotionSensor(???)

   ???

   **Methods**

   .. method:: get_pitch_angle(???)

      ???

   .. method:: get_roll_angle(???)

      ???

   .. method:: get_yaw_angle(???)

      ???

   .. method:: get_orientation(???)

      ???

   .. method:: get_gesture(???)

      ???

   .. method:: reset_yaw_angle(???)

      ???

   .. method:: was_gesture(???)

      ???

   .. method:: wait_for_new_orientation(???)

      ???

   .. method:: wait_for_new_gesture(???)

      ???

   **Constants**

   .. data:: FALLING
      :value: falling

      ???

   .. data:: SHAKEN
      :value: shaken

      ???

   .. data:: TAPPED
      :value: tapped

      ???

   .. data:: DOUBLE_TAPPED
      :value: doubletapped

      ???

   .. data:: LEFT_SIDE
      :value: leftside

      ???

   .. data:: RIGHT_SIDE
      :value: rightside

      ???

   .. data:: FRONT
      :value: front

      ???

   .. data:: BACK
      :value: back

      ???

   .. data:: UP
      :value: up

      ???

   .. data:: DOWN
      :value: down

      ???

Imports
-------
* Module `hub`
* Function `utime.sleep_ms`
