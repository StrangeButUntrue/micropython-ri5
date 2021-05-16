:mod:`_api.app` -- application functions API
============================================

.. module:: _api.app
   :synopsis: application functions API

This module contains the API functions for user interaction with the
controlling application (i.e. computer or phone).

This module is imported by the `mindstorms` and `spike` modules so that the API
can be branded appropriately in documentation (i.e. so that Mindstorms docs can
tell you to import mindstorms, and Spike Prime docs can tell you to import
spike).

Constants
---------
.. data:: _NOT_CONNECTED_ERROR
   :value: The programming app is not connected to the hub.

   Error text for when the app and the hub have become disconnected.

App Class
---------
.. class:: App(???)

   ???

   **Methods**

   .. method:: play_sound(???)

      ???

   .. method:: _play_sound(???)

      ???

   .. method:: start_sound(???)

      ???

Imports
-------
* Class `protocol.ujsonrpc.JSONRPC`
* Function `utime.ticks_diff`
* Function `utime.ticks_ms`
* Constant `util.constants.BT_VCP` = BT_VCP(0)
* Constant `util.constants.USB_VCP` = USB_VCP(0)
