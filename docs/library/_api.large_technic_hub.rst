:mod:`_api.large_technic_hub` -- central hub API
================================================

.. module:: _api.large_technic_hub
   :synopsis: central hub API

This module contains the specific instances of other API classes for user
interaction with various aspects of the central hub brick.

The class in this module is superclassed by the `mindstorms.MSHub` and
`spike.PrimeHub` classes so that the API can be branded appropriately in
documentation (i.e. so that Mindstorms docs can tell you to import mindstorms,
and Spike Prime docs can tell you to import spike).

LargeTechnicHub Class
---------------------
.. class:: LargeTechnicHub(???)

   ???

   **Properties**

   .. property:: status_light

      ???

   .. property:: light_matrix

      ???

   .. property:: left_button

      ???

   .. property:: right_button

      ???

   .. property:: motion_sensor

      ???

   .. property:: speaker

      ???

   **Constants**

   .. data:: PORT_A
      :value: A

   .. data:: PORT_B
      :value: B

   .. data:: PORT_C
      :value: C

   .. data:: PORT_D
      :value: D

   .. data:: PORT_E
      :value: E

   .. data:: PORT_F
      :value: F

      Constants to specify specific ports on the Hub.

   .. data:: _status_light

      A reference to the specific `_api.statuslight.StatusLight` object
      representing the status light under the main button on the Hub.

   .. data:: _light_matrix

      A reference to the specific `_api.lightmatrix.LightMatrix` object
      representing the 5x5 display on the Hub.

   .. data:: _left_button

      A reference to the specific `_api.button.Button` object representing the
      left button on the Hub.

   .. data:: _right_button

      A reference to the specific `_api.button.Button` object representing the
      right button on the Hub.

   .. data:: _motion_sensor

      A reference to the specific `_api.motionsensor.MotionSensor` object
      representing the motion sensor in the Hub.

   .. data:: _speaker

      A reference to the specific `_api.speaker.Speaker` object representing
      the speaker in the Hub.

Imports
-------
* Module `hub`
* Function `_api.button.Button`
* Function `_api.lightmatrix.LightMatrix`
* Function `_api.motionsensor.MotionSensor`
* Function `_api.speaker.Speaker`
* Function `_api.statuslight.StatusLight`
