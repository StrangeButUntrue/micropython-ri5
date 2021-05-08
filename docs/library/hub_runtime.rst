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

* Module :mod:`hub`
* Module :mod:`runtime`
* Module :mod:`util.scratch`
* Module :mod:`util.sensors`
* Class :class:`LinegraphMonitorMethods` from :mod:`commands` module
* Class :class:`SoundMethods` from :mod:`commands` module
* Class :class:`programrunner.ProgramRunner`
* Class :class:`HubUI` from :mod:`ui.hubui` module
* Class :class:`LightMethods` from :mod:`commands` module
* Class :class:`ProgramMethods` from :mod:`commands` module
* Class :class:`MotorMethods` from :mod:`commands` module
* Class :class:`HubMethods` from :mod:`commands` module
* Class :class:`RPCProtocol` from :mod:`protocol` module
* Class :class:`WaitMethods` from :mod:`commands` module
* Class :class:`RTTimer` from :mod:`util.resetter` module
* Class :class:`machine.Timer`
* Class :class:`MoveMethods` from :mod:`commands` module