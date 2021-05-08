:mod:`hub_runtime` -- Hub main module
=====================================

.. module:: hub_runtime
   :synopsis: Hub main module

Seems to be the main module on the Hub, in charge of startup and error
handling.

Functions
---------

.. function:: register_ports(???)

   ???

.. function:: __connection_changed(???)

   ???

.. function:: init(???)

   ???

.. function:: start(???)

   ???

.. function:: pop_force_reset(???)

   ???

.. function:: get_event_loop(???)

   ???

.. function:: notify_gesture_event(???)

   ???

Constants
---------

.. data:: TIMER_PACE_HIGH
   :value: 16

   ???

.. data:: BT_VCP
   :value: BT_VCP(0)

   Reference to the BT_VCP object defining the bluetooth connection.

.. data:: USB_VCP
   :value: USB_VCP(0)

   Reference to the USB_VCP object defining the USB connection.

.. data:: error_handler

   Reference to the main error handler object.  (Type `util.error_handler.ErrorHandler`)

.. data:: system

   Reference to the main system object.  (Type `system.System`)

Imports
-------

* Module `hub`
* Module `runtime`
* Module `util.scratch`
* Module `util.sensors`
* Class `commands.LinegraphMonitorMethods`
* Class `commands.SoundMethods`
* Class `programrunner.ProgramRunner`
* Class `ui.hubui.HubUI`
* Class `commands.LightMethods`
* Class `commands.ProgramMethods`
* Class `commands.MotorMethods`
* Class `commands.HubMethods`
* Class `protocol.RPCProtocol`
* Class `commands.WaitMethods`
* Class `util.resetter.RTTimer`
* Class `machine.Timer`
* Class `commands.MoveMethods`