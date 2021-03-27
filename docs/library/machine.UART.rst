.. currentmodule:: machine
.. _machine.UART:

class UART -- duplex serial communication bus
=============================================

UART implements the standard UART/USART duplex serial communications protocol.  At
the physical level it consists of 2 lines: RX and TX.  The unit of communication
is a character (not to be confused with a string character) which can be 8 or 9
bits wide.

UART objects can be created and initialised using::

    from machine import UART

    uart = UART(1, 9600)                         # init with given baudrate
    uart.init(9600, bits=8, parity=None, stop=1) # init with given parameters

Supported parameters differ on different boards.

On the RI5, it appears that no UARTs are actually available - at least I
couldn't find an ID that would allow me to create one.  So available
parameters are unknown and the rest of this section is a little light on
RI5-specific detail as it's difficult to do experiments when you can't create
the base object!  It's based on the STM32 port code instead since that'll
probably be quite similar...

A UART object acts like a `stream` object and reading and writing is done
using the standard stream methods::

    uart.read(10)       # read 10 characters, returns a bytes object
    uart.read()         # read all available characters
    uart.readline()     # read a line
    uart.readinto(buf)  # read and store into the given buffer
    uart.write('abc')   # write the 3 characters

Constructors
------------

.. class:: UART(id, ...)

   Construct a UART object of the given id.  Any additional parameters are
   passed on to the init function.

Methods
-------

.. method:: UART.init(baudrate=9600, bits=8, parity=None, stop=1, \*, ...)

   Initialise the UART bus with the given parameters:

     - *baudrate* is the clock rate.
     - *bits* is the number of bits per character.  Can be 8 or 9.
     - *parity* is the parity, ``None``, 0 (even) or 1 (odd).
     - *stop* is the number of stop bits, 1 or 2.
     - `timeout` is the timeout in milliseconds to wait for the first character.
     - `timeout_char` is the timeout in milliseconds to wait between characters.
     - `flow` is RTS | CTS where RTS == 256, CTS == 512
     - `read_buf_len` is the character length of the read buffer (0 to disable).

.. method:: UART.deinit()

   Turn off the UART bus.

.. method:: UART.any()

   Returns an integer counting the number of characters that can be read without
   blocking.  It will return 0 if there are no characters available and a positive
   number if there are characters.  The method may return 1 even if there is more
   than one character available for reading.

   For more sophisticated querying of available characters use select.poll::

    poll = select.poll()
    poll.register(uart, select.POLLIN)
    poll.poll(timeout)

.. method:: UART.read([nbytes])

   Read characters.  If ``nbytes`` is specified then read at most that many bytes,
   otherwise read as much data as possible.

   Return value: a bytes object containing the bytes read in.  Returns ``None``
   on timeout.

.. method:: UART.readinto(buf[, nbytes])

   Read bytes into the ``buf``.  If ``nbytes`` is specified then read at most
   that many bytes.  Otherwise, read at most ``len(buf)`` bytes.

   Return value: number of bytes read and stored into ``buf`` or ``None`` on
   timeout.

.. method:: UART.readline()

   Read a line, ending in a newline character.

   Return value: the line read or ``None`` on timeout.

.. method:: UART.readchar()

   Receive a single character, and return it as an integer (or -1 on timeout).

.. method:: UART.write(buf)

   Write the buffer of bytes to the bus.

   Return value: number of bytes written or ``None`` on timeout.

.. method:: UART.writechar(char)

   Write a single character to the bus.  ``char`` is the integer to write.
   Returns ``None``.

.. method:: UART.sendbreak()

   Send a break condition on the bus. This drives the bus low for a duration
   longer than required for a normal transmission of a character.

.. method:: UART.irq(trigger=0, hard=False, handler=None)

   Create a callback to be triggered when data is received on the UART.

       - *trigger* can only be ``UART.IRQ_RXIDLE``
       - *hard* seems to specify whether it's a hardware or software interrupt?
       - *handler* an optional function to be called when new characters arrive.

   .. note::

      The handler will be called whenever any of the following two conditions are met:

          - 8 new characters have been received.
          - At least 1 new character is waiting in the Rx buffer and the Rx line has been
            silent for the duration of 1 complete frame.

      This means that when the handler function is called there will be between 1 to 8
      characters waiting.

   Returns an irq object.

Constants
---------

.. data:: UART.RTS = 256

    Flow parameter setting for initialization.

.. data:: UART.CTS = 512

    Flow parameter setting for initialization.

.. data:: UART.IRQ_RXIDLE = 16

    IRQ flag "idle".  (Replaces UART.RX_ANY from the base documentation.)
