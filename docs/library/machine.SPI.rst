.. currentmodule:: machine
.. _machine.SPI:

class SPI -- a Serial Peripheral Interface bus protocol (master side)
=====================================================================

SPI is a synchronous serial protocol that is driven by a master. At the
physical level, a bus consists of 3 lines: SCK, MOSI, MISO. Multiple devices
can share the same bus. Each device should have a separate, 4th signal,
SS (Slave Select), to select a particular device on a bus with which
communication takes place. Management of an SS signal should happen in
user code (via machine.Pin class).

Constructors
------------

.. class:: SPI(id=-1, ...)

   Construct an SPI object on the given bus, ``id``. Values of ``id`` depend
   on a particular port and its hardware. Values 0, 1, etc. are commonly used
   to select hardware SPI block #0, #1, etc. Value -1 can be used for
   bitbanging (software) implementation of SPI.  In this case sck/mosi/miso
   parameters must be specified.

   Any extra parameters are passed to ``init()``.

   .. admonition:: Difference for RI5
      :class: attention

      Unlike the specification in the base MicroPython docs, this constructor
      seems to always call ``init()``, whether or not more parameters are
      provided to it.

   .. admonition:: Difference for RI5
      :class: attention

      The hardware SPI blocks on the RI5 and their default details are shown below.
      Pin details aren't printed when printing the object, so they've been
      deduced from machine.Pin() printing and
      https://github.com/micropython/micropython/blob/master/ports/stm32/boards/stm32f413_af.csv.

   All SPIs have default baudrate=375000, polarity=0, phase=0, bits=8.  Be
   careful with altering or deinitializing any of these, as any changes will
   persist beyond the life of your program, and can cause system failure.

   SPI(1) - MISO=A6, MOSI=A7, SCK=A5, NSS=A4 or A15(?).
   No obvious effect if you slow it down or speed it up, but if you deinit it,
   the system slows to a crawl...  A basic read gets the following set of bytes
   followed by zeros: 0,0,0,0,0,0,0x2F,0xC0,0,0,0,0,0x11,0x80,0x23,0,0x7F,0x80.

   SPI(2) - MISO=C2, MOSI=C3, SCK=B13, NSS=A11 or B9 or B12(?).
   Seems to affect lots of systems like the screen/sound/lights/program loading
   if you slow it down...  A basic read gets all zeros.

   SPI(3) - MISO=B4, MOSI=B5, SCK=B3 or B12 or C10(?), NSS=A4 or A15(?).
   No obvious effect if you slow it down or deinit it.  A basic read gets one zero
   and times out if you read more than one byte at a time.

Methods
-------

.. method:: SPI.init(baudrate=500000, \*, polarity=0, phase=0, bits=8, firstbit=SPI.MSB, sck=None, mosi=None, miso=None)

   Initialise the SPI bus with the given parameters:

     - ``baudrate`` is the SCK clock rate.  Note that the default value isn't an
       available hardware baudrate, so those actually default to 375000 in
       practice.
     - ``polarity`` can be 0 or 1, and is the level the idle clock line sits at.
       (Although it can actually take any byte value.)
     - ``phase`` can be 0 or 1 to sample data on the first or second clock edge
       respectively.  (Although it can actually take any byte value.)
     - ``bits`` is the width in bits of each transfer. Must be 8.
     - ``firstbit`` must be ``SPI.MSB`` (0).
     - ``sck``, ``mosi``, ``miso`` are pins (machine.Pin) objects (or strings
       naming pins) to use for bus signals. For most hardware SPI blocks (as
       selected by ``id`` parameter to the constructor), pins are fixed and
       cannot be changed. In some cases, hardware blocks allow 2-3 alternative pin sets for
       a hardware SPI block. Arbitrary pin assignments are possible only for a bitbanging SPI driver
       (``id`` = -1).

   The actual clock frequency may be lower than the requested baudrate.  They
   are rounded down to the nearest available one.  On RI5:

   Hardware baudrates: 12000000, 6000000, 3000000, 1500000, 750000, 375000, 187500, 93750

   Software baudrates = 16000000/(32*N) = 500000, 250000, 166666, 125000, 100000, 83333, ..., 1

   The actual rate may be determined by printing the SPI object.

.. method:: SPI.deinit()

   Turn off the SPI bus.

.. method:: SPI.read(nbytes, write=0x00)

    Read a number of bytes specified by ``nbytes`` while continuously writing
    the single byte given by ``write``.
    Returns a ``bytes`` object with the data that was read.

.. method:: SPI.readinto(buf, write=0x00)

    Read into the buffer specified by ``buf`` while continuously writing the
    single byte given by ``write``.
    Returns ``None``.

.. method:: SPI.write(buf)

    Write the bytes contained in ``buf``.
    Returns ``None``.

.. method:: SPI.write_readinto(write_buf, read_buf)

    Write the bytes from ``write_buf`` while reading into ``read_buf``.  The
    buffers can be the same or different, but both buffers must have the
    same length.
    Returns ``None``.

Constants
---------

.. data:: SPI.MSB = 0

   set the first bit to be the most significant bit

.. data:: SPI.LSB = 128

   Set the first bit to be the least significant bit.  (Cannot be used on RI5.)
