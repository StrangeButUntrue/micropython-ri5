:mod:`hub_runtime` -- Hub main module
=====================================

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

.. data:: TIMER_PACE_HIGH = 16

   ???

.. data:: BT_VCP = BT_VCP(0)

   Reference to the BT_VCP object defining the bluetooth connection.

.. data:: USB_VCP = USB_VCP(0)

   Reference to the USB_VCP object defining the USB connection.

.. data:: error_handler

   Reference to the main error handler object (type util.error_handler.ErrorHandler).

.. data:: system

   Reference to the main system object (type system.System).

Imports
-------

* Module hub
* Module runtime
* Module util.scratch
* Module util.sensors
* Class LinegraphMonitorMethods from commands module
* Class SoundMethods from commands module
* Class ProgramRunner from programrunner module
* Class HubUI from ui module
* Class LightMethods from commands module
* Class ProgramMethods from commands module
* Class MotorMethods from commands module
* Class HubMethods from commands module
* Class RPCProtocol from protocol module
* Class WaitMethods from commands module
* Class RTTimer from util.resetter module
* Class Timer from machine module
* Class MoveMethods from commands module