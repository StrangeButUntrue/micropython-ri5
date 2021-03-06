:mod:`_onewire` -- OneWire Protocol
===================================

.. module:: _onewire
   :synopsis: Implementation of the OneWire protocol

This module allows sending and receiving of data on a Pin according to the
`OneWire protocol <https://en.wikipedia.org/wiki/1-Wire>`_.

Functions which take a ``pin`` argument expect an argument that can be used
to reference a Pin, i.e. something you can feed to the ``machine.Pin()``
function.  In the RI5's case, this is a str.

Functions
---------

.. function:: reset(pin)

   Does a OneWire reset on the given pin.  Returns true if a device presence
   pulse was detected, otherwise false.

.. function:: readbit(pin)

   Reads and returns a single bit from the given pin, assuming the Onewire
   protocol.

.. function:: readbyte(pin)

   Reads 8 bits from the given pin using the Onewire protocol, then returns
   them as an integer.  (Assumes a low-bit-first model.)

.. function:: writebit(pin, bitval)

   Writes a single bit with value ``bitval`` to the given pin, assuming the
   Onewire protocol.

.. function:: writebyte(pin, byteval)

   From byte ``byteval``, writes 8 bits to the given pin using the Onewire
   protocol.  (Assumes a low-bit-first model.)

.. function:: crc8(bytearray)

   Computes the 8-bit CRC-remainder of the given bytearray (or other buffered
   object).  As expected for the Onewire protocol, it seems to use the
   CRC-8/MAXIM version.
