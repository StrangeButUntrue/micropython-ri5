.. currentmodule:: machine
.. _machine.ADC:

class ADC -- analog to digital conversion
=========================================

Read analog values from a pin.

.. admonition:: Difference for RI5
   :class: attention

   Functions ``channel()`` (and associated class), ``init()`` and ``deinit()``
   are not implemented for the RI5.  Instead the ``read_u16()`` function allows
   analog reading, and the constants below are added too.

Constructors
------------

.. class:: ADC(channel)

   Create an ADC object with the given ``channel`` (a signed integer).  This
   allows you to then read analog values on that channel.  It's not clear to
   me yet what sources most of these channels represent - every one I tried
   did receive data from somewhere...  The constants below seem to represent
   a few important ones though.

.. class:: ADC(pin_name)

   Create an ADC object from the Pin corresponding to string ``pin_name``.

   On the RI5, this seems to be possible only on PA0, PB0, PB1, PC0-5
   (although using it on PC2 or PC3 seems to conflict with something in the
   firmware, causing runtime errors after use).

Methods
-------

.. method:: read_u16()

   Read the current channel value.

Constants
---------

Channel numbers to get particular information from.

.. data:: machine.ADC.VREF = 65535

   According to the STM32 port code, this channel just constantly reports the
   maximum ADC value, which seems to be 65535.

.. data:: machine.ADC.CORE_VREF = 17

   Perhaps this is core voltage data?  In a test it seemed to get a
   variety of values of the form 0x3??3 (from 0x3B23 to 0x3CB3) and 0x4??4
   (from 0x4274 to 0x45A4).

.. data:: machine.ADC.CORE_TEMP = 16

   Presumably gets core temperature sensor data.  Running at room temperature I
   was seeing integer values around 11026 (0x2B12), varying in multiples of 16
   to around +-200.  Possibly the last hex digit is not relevant given the fact
   that it always seems to be the same as the first in these readings?

.. data:: machine.ADC.CORE_VBAT = 18

   Presumably this gets battery charge or voltage level data?  In a test it
   seemed to get integer values around 2768 (0x0AD0), varying in multiples of 16
   to around +-150.  Possibly the last hex digit is not relevant given the fact
   that it always seems to be the same as the first in these readings?

Other Experiments
-----------------
Experiments often showed slightly different initial values settling down to a
more steady range of values.  I also found the sources for the rest of the
channels below 16, apart from channel 1:

PA0 for a while reported values from 0x1341 to 0x1501.  Printing the ADC showed
it's probably equal to channel 0 (i.e. ADC(0)).

PA2 for a while reported values from 0x1001 to 0x1041.  It presents as channel 2.

PA3 for a while reported values from 0x11A1 to 0x12B1.  It presents as channel 3.

PA4 for a while reported values from 0x1041 to 0x1101.  It presents as channel 4.

PA5 for a while reported values from 0x1181 to 0x12A1.  It presents as channel 5.

PA6 for a while reported values from 0x0FB0 to 0x1011.  It presents as channel 6.

PA7 for a while reported values from 0x1241 to 0x1391.  It presents as channel 7.

PB0 for a while reported values from 0x25C2 to 0x2672.  It presents as channel 8.

PB1 for a while reported values from 0x11C1 to 0x1471.  It presents as channel 9.

PC0 for a while reported values from 0x10F1 to 0x1221.  It presents as channel 10.

PC1 for a while reported values from 0x3003 to 0x3173 and on another occasion
reported values from 0xB23B to 0xBA8B.  It presents as channel 11.

PC2 for a while reported values from 0x1331 to 0x1EA1.  It presents as channel
12.  Although if you access channel 12 directly you tend to get much lower
values it seems, and no runtime errors...

PC3 gave two much higher readings of 0xAFEA and 0x2152, then settled down into
lower readings between 0x1241 and 0x1551.  It presents as channel 13, but if
you access channel 12 directly you tend to get much lower values it seems, and
no runtime errors...

PC4 for a while reported values from 0xA0AA to 0xCA9C.  It presents as channel 14.

PC5 gave one much higher reading of 0x4E94, then for a while reported values
from 0x0860 to 0x0AB0.  It presents as channel 15.