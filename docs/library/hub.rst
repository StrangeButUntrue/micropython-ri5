:mod:`hub` -- hub brick functionality
=====================================

.. module:: hub
   :synopsis: hub brick functionality

Classes and functions related to simple parts and abilities of the Hub brick
itself, like buttons, ports, and internal sensors.

These are lower-level functions than the API ones (the API seems to import this
module a lot) and as such they provide greater control, although with a
corresponding amount of risk of things going wrong if you use them improperly.

Constants
---------

.. data:: __version__
   :value: v1.0.06.0034-b0c335b

Functions
---------

.. function:: info(???)

   ???

.. function:: power_off(???)

   ???

.. function:: repl_restart(???)

   ???

.. function:: status(???)

   ???

.. function:: led(???)

   ???

.. function:: temperature(???)

   ???

.. function:: file_transfer(???)

   ???

Imports
-------
* Class `util.constants.Image`

Objects and Classes
-------------------
It's not quite clear from MicroPython help text whether these are classes or
instances of classes.  For the moment I'm assuming both, since some have
different names from the object they point to.  But if that's the case it's not
clear where the class lives!

.. data:: port

.. class:: Port(???)

   ???

   **Constants**

   .. data:: DETACHED
      :value: 0

      ???

   .. data:: ATTACHED
      :value: 1

      ???

   .. data:: A
      :value: Port(A)
   .. data:: B
      :value: Port(B)
   .. data:: C
      :value: Port(C)
   .. data:: D
      :value: Port(D)
   .. data:: E
      :value: Port(E)
   .. data:: F
      :value: Port(F)

      ???

   .. data:: MODE_DEFAULT
      :value: 0

      ???

   .. data:: MODE_FULL_DUPLEX
      :value: 1

      ???

   .. data:: MODE_HALF_DUPLEX
      :value: 2

      ???

   .. data:: MODE_GPIO
      :value: 3

      ???

   **Port(X)**

   These are objects in their own right, with the following contents:

   **Methods**
   .. method:: callback(???)

      ???

   .. method:: info(???)

      ???

   .. method:: mode(???)

      ???

   .. method:: pwm(???)

      ???

   **Variables**
   .. data:: device

      ???  Observed value: None
   .. data:: motor

      ???  Observed value: None

.. data:: display

.. class:: Display(???)

   ???

   .. method:: pixel(???)

      ???

   .. method:: show(???)

      ???

   .. method:: callback(???)

      ???

   .. method:: clear(???)

      ???

   .. method:: rotation(???)

      ???

.. data:: button

.. class:: Button(???)

   ???

   **Members**

   .. data:: center
      :value: center
   .. data:: left
      :value: left
   .. data:: right
      :value: right
   .. data:: connect
      :value: connect

      Represent each of the four buttons on the Hub (the main button in the
      center, left, right, and the bluetooth connect button).  The values are
      objects with the following contents:

   .. method:: is_pressed(???)

      ???

   .. method:: was_pressed(???)

      ???

   .. method:: presses(???)

      ???

   .. method:: callback(???)

      ???

   .. method:: on_change(???)

      ???

.. data:: sound

.. class:: Sound(???)

   ???

   **Methods**

   .. method:: volume(???)

      ???

   .. method:: beep(???)

      ???

   .. method:: play(???)

      ???

   .. method:: callback(???)

      ???

   **Constants**

   .. data:: SOUND_SIN
      :value: 0

      ???

   .. data:: SOUND_SQUARE
      :value: 1

      ???

   .. data:: SOUND_TRIANGLE
      :value: 2

      ???

   .. data:: SOUND_SAWTOOTH
      :value: 3

      ???

.. data:: motion

.. class:: Motion(???)

   ???

   **Methods**

   .. method:: gyroscope(???)

      ???

   .. method:: gyroscope_filter(???)

      ???

   .. method:: accelerometer(???)

      ???

   .. method:: accelerometer_filter(???)

      ???

   .. method:: position(???)

      ???

   .. method:: reset_yaw(???)

      ???

   .. method:: preset_yaw(???)

      ???

   .. method:: orientation(???)

      ???

   .. method:: gesture(???)

      ???

   .. method:: was_gesture(???)

      ???

   .. method:: callback(???)

      ???

   **Constants**

   .. data:: NONE
      :value: NULL

      ???

   .. data:: LEFTSIDE
      :value: leftside

      ???

   .. data:: RIGHTSIDE
      :value: rightside

      ???

   .. data:: DOWN
      :value: down

      ???

   .. data:: UP
      :value: up

      ???

   .. data:: FRONT
      :value: front

      ???

   .. data:: BACK
      :value: back

      ???

   .. data:: TAPPED
      :value: tapped

      ???

   .. data:: DOUBLETAPPED
      :value: doubletapped

      ???

   .. data:: SHAKE
      :value: shake

      ???

   .. data:: FREEFALL
      :value: freefall

      ???

.. data:: battery

.. class:: Battery(???)

   ???

   **Methods**

   .. method:: voltage(???)

      ???

   .. method:: current(???)

      ???

   .. method:: temperature(???)

      ???

   .. method:: charger_detect(???)

      ???

   .. method:: info(???)

      ???

   .. method:: capacity_left(???)

      ???

   **Constants**

   .. data:: BATTERY_NO_ERROR
      :value: 0

      ???

   .. data:: BATTERY_HUB_TEMPERATURE_CRITICAL_OUT_OF_RANGE
      :value: -2

      ???

   .. data:: BATTERY_TEMPERATURE_OUT_OF_RANGE
      :value: -2

      ???

   .. data:: BATTERY_TEMPERATURE_SENSOR_FAIL
      :value: -3

      ???

   .. data:: BATTERY_BAD_BATTERY
      :value: -4

      ???

   .. data:: BATTERY_VOLTAGE_TOO_LOW
      :value: -5

      ???

   .. data:: USB_CH_PORT_NONE
      :value: 0

      ???

   .. data:: USB_CH_PORT_SDP
      :value: 1

      ???

   .. data:: USB_CH_PORT_CDP
      :value: 2

      ???

   .. data:: USB_CH_PORT_DCP
      :value: 3

      ???

   .. data:: CHARGER_STATE_FAIL
      :value: -1

      ???

   .. data:: CHARGER_STATE_DISCHARGING
      :value: 0

      ???

   .. data:: CHARGER_STATE_CHARGING_ONGOING
      :value: 1

      ???

   .. data:: CHARGER_STATE_CHARGING_COMPLETED
      :value: 2

      ???

.. data:: bluetooth

.. class:: bt(???)

   ???

   .. method:: info(???)

      ???

   .. method:: discoverable(???)

      ???

.. data:: ble

.. class:: bluetooth(???)

   ???

   .. method:: rssi(???)

      ???

   .. method:: mac(???)

      ???

   .. method:: scan(???)

      ???

   .. method:: scan_result(???)

      ???

   .. method:: connect(???)

      ???

   .. method:: callback(???)

      ???

.. data:: supervision

.. class:: supervision(???)

   ???

   .. method:: info(???)

      ???

.. data:: BT_VCP

.. class:: BT_VCP(???)

   ???

   .. method:: setinterrupt(???)

      ???

   .. method:: isconnected(???)

      ???

   .. method:: any(???)

      ???

   .. method:: send(???)

      ???

   .. method:: recv(???)

      ???

   .. method:: read(???)

      ???

   .. method:: readinto(???)

      ???

   .. method:: readline(???)

      ???

   .. method:: readlines(???)

      ???

   .. method:: write(???)

      ???

   .. method:: close(???)

      ???

   .. method:: __del__(???)

      ???

   .. method:: __enter__(???)

      ???

   .. method:: __exit__(???)

      ???

   .. method:: callback(???)

      ???

.. data:: USB_VCP

.. class:: USB_VCP(???)

   ???  Has all the same contents as BT_VCP, with these extras:

   **Methods**

   .. method:: init(???)

      ???

   **Constants**

   .. data:: RTS
      :value: 1

      ???

   .. data:: CTS
      :value: 2

      ???
