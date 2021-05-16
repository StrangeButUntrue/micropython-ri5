:mod:`_api.colorsensor` -- color sensor functions API
=====================================================

.. module:: _api.colorsensor
   :synopsis: color sensor functions API

This module contains the API functions for user interaction with a color
sensor brick.

This module is imported by the `mindstorms` and `spike` modules so that the API
can be branded appropriately in documentation (i.e. so that Mindstorms docs can
tell you to import mindstorms, and Spike Prime docs can tell you to import
spike).

Functions
---------

.. function:: _get_port_device(???)

   ???

.. function:: _is_color_sensor(???)

   ???

Constants
---------

.. data:: _COLORLIST
   :value: ['black', 'violet', None, 'blue', 'cyan', 'green', None, 'yellow', None, 'red', 'white']

   A list to allow easy mapping from color values to color names.

.. data:: _AMBIENT_MODE
   :value: (2, [(2, 0)])

   ???

.. data:: _LIGHT_MODE
   :value: (3, [(3, 0), (3, 1), (3, 2)])

   ???

.. data:: _COMBI_MODE
   :value: ([(1, 0), (0, 0), (5, 0), (5, 1), (5, 2), (5, 3)],)

   ???

ColorSensor Class
-----------------
.. class:: ColorSensor(???)

   ???

   **Methods**

   .. method:: light_up_all(???)

      ???

   .. method:: light_up(???)

      ???

   .. method:: get_reflected_light(???)

      ???

   .. method:: get_rgb_intensity(???)

      ???

   .. method:: get_red(???)

      ???

   .. method:: get_green(???)

      ???

   .. method:: get_blue(???)

      ???

   .. method:: get_ambient_light(???)

      ???

   .. method:: get_color(???)

      ???

   .. method:: _get_color(???)

      ???

   .. method:: _set_mode(???)

      ???

   .. method:: wait_until_color(???)

      ???

   .. method:: wait_for_new_color(???)

      ???

Imports
-------
* Function `_api.util.newSensorDisconnectedError`
* Function `utime.sleep_ms`
* Function `util.scratch.clamp`
* Function `util.sensors.get_sensor_value`
* Function `util.sensors.is_type`
* Constant `util.constants.LPF2_FLIPPER_COLOR` = 61
* Constant `util.constants.PORTS` = {'C': Port(C), 'B': Port(B), 'D': Port(D), 'E': Port(E), 'A': Port(A), 'F': Port(F)}
