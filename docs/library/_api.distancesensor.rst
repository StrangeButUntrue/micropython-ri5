:mod:`_api.distancesensor` -- distance sensor functions API
===========================================================

.. module:: _api.distancesensor
   :synopsis: distance sensor functions API

This module contains the API functions for user interaction with a distance
sensor brick.

This module is imported by the `mindstorms` and `spike` modules so that the API
can be branded appropriately in documentation (i.e. so that Mindstorms docs can
tell you to import mindstorms, and Spike Prime docs can tell you to import
spike).

DistanceSensor Class
--------------------
.. class:: DistanceSensor(???)

   ???

   **Methods**

   .. method:: _set_mode(???)

      ???

   .. method:: _set_range_mode(???)

      ???

   .. method:: _is_distance_sensor(???)

      ???

   .. method:: get_distance_cm(???)

      ???

   .. method:: get_distance_inches(???)

      ???

   .. method:: get_distance_percentage(???)

      ???

   .. method:: wait_for_distance_farther_than(???)

      ???

   .. method:: wait_for_distance_closer_than(???)

      ???

   .. method:: light_up(???)

      ???

   .. method:: light_up_all(???)

      ???

   **Constants**

   .. data:: PERCENT
      :value: %

      ???

   .. data:: CM
      :value: cm

      ???

   .. data:: IN
      :value: in

      ???

   .. data:: _LONG_RANGE_MODE
      :value: (0, [(0, 0)])

      ???

   .. data:: _SHORT_RANGE_MODE
      :value: (1, [(1, 0)])

      ???

   .. data:: _LIGHT_MODE
      :value: (5, [(5, 0), (5, 1), (5, 2), (5, 3)])

      ???

Imports
-------
* Function `_api.util.newSensorDisconnectedError`
* Function `utime.sleep_ms`
* Function `util.scratch.clamp`
* Function `util.sensors.is_type`
* Constant `util.constants.LPF2_FLIPPER_DISTANCE` = 62
* Constant `util.constants.PORTS` = {'C': Port(C), 'B': Port(B), 'D': Port(D), 'E': Port(E), 'A': Port(A), 'F': Port(F)}
