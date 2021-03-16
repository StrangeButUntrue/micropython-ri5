:mod:`machine` --- functions related to the hardware
====================================================

.. module:: machine
   :synopsis: functions related to the hardware

The ``machine`` module contains specific functions related to the hardware
on a particular board. Most functions in this module allow to achieve direct
and unrestricted access to and control of hardware blocks on a system
(like CPU, timers, buses, etc.). Used incorrectly, this can lead to
malfunction, lockups, crashes of your board, and in extreme cases, hardware
damage.

The RI5 version of this module seems to be a lot like the STM32 port of
Micropython, as you might expect given that the RI5 runs on a STM32F413.  A lot
of the RI5 specifics here line up with the code for that port.

.. _machine_callbacks:

A note of callbacks used by functions and class methods of :mod:`machine` module:
all these callbacks should be considered as executing in an interrupt context.
This is true for both physical devices with IDs >= 0 and "virtual" devices
with negative IDs like -1 (these "virtual" devices are still thin shims on
top of real hardware and real hardware interrupts). See :ref:`isr_rules`.

Reset related functions
-----------------------

.. function:: reset()

   Resets the device in a manner similar to pushing the external RESET
   button.

.. function:: soft_reset()

   On RI5, resets to menu with a SystemExit, as though calling ``sys.exit()``.
   Doesn't seem to change the reset_cause() below.

   .. admonition:: Difference for RI5
      :class: attention

      This function isn't in the base MicroPython, at least not the version
      RI5 was branched from.  It's also not clear it does precisely the same
      thing as the soft_reset function in the latest base MicroPython version.

.. function:: reset_cause()

   Get the reset cause. See :ref:`constants <machine_constants>` for the
   possible return values.  On RI5 it doesn't seem to report SOFT_RESET, and
   PWRON_RESET is only reported when the Hub has been both powered off and
   unplugged and then powered up.  But the others all seem to work as you'd
   expect.

Interrupt related functions
---------------------------

.. function:: disable_irq()

   Disable interrupt requests.
   Returns the previous IRQ state which should be considered an opaque value.
   This return value should be passed to the `enable_irq()` function to restore
   interrupts to their original state, before `disable_irq()` was called.

   On the RI5, the return value seems to be True if interrupt requests were
   successfully disabled, and False if they weren't (which you get for example
   if you try to disable twice without enabling in between).

.. function:: enable_irq(state)

   Re-enable interrupt requests.
   The *state* parameter should be the value that was returned from the most
   recent call to the `disable_irq()` function.

   On the RI5, the parameter seems to determine whether the system actually tries
   to enable interrupts or not - i.e. if False it does nothing.  This allows
   the user to nest calls to disable/enable, but to overlap them in other ways
   you would have to keep track of how many disable calls there have been
   yourself.  Note that trying to enable twice with True parameters in succession
   seems to crash the system.

Power related functions
-----------------------

.. function:: freq()

    With no parameters, returns CPU frequency in hertz, or sets it with a parameter.

   .. admonition:: Difference for RI5
      :class: attention

      See below for RI5-specifics.

   In RI5 this actually returns a tuple (S, H, P1, P2) of the various clock
   speed frequencies of the board.  These can be set by passing one to four
   parameters to the function.  Any unsupplied parameters are set in proportion
   to their default relationship to S, so setting freq(S/2) will divide
   everything by 2.

   See STM32F413 board documentation for full details on the four clocks here,
   but in terms of RI5 observations:

   * S = System Clock frequency.  On my system, it seems to default to 96000000.
     Presumably this dictates how fast the CPU runs.

   * H = AHB (Advanced High-Performance Bus) Clock frequency.  On my system,
     it seems to default to 96000000.  Possibly controls some aspect of USB,
     because setting this too low (e.g. 24MHz) seems to break the connection
     between RI5 and the app and lead to debug logs showing json messages with
     characters doubled or missing.  And potentially other dangers - set at
     your peril!

   * P1 = APB1 (Advanced Peripheral Bus 1) Clock frequency.  On my system, it
     seems to default to 24000000.  This seems to control most of the output
     systems - halving it causes the LED to flicker, and lights and sound go
     half as fast.  It also has some impact on USB though and maybe some quite
     key systems too as a further reduction broke the app connection and had me
     nervous I'd broken things more seriously for a while.  Set at your peril!

   * P2 = APB2 (Advanced Peripheral Bus 2) Clock frequency.  On my system, it
     seems to default to 48000000.  No obvious effect discovered yet.

   Frequency changes persist between programs, but go back to defaults on a
   hard reset.

.. function:: idle()

   Gates the clock to the CPU, useful to reduce power consumption at any time during
   short or long periods. Peripherals continue working and execution resumes as soon
   as any interrupt is triggered (on many ports this includes system timer
   interrupt occurring at regular intervals on the order of millisecond).

   Similar to other low-power functions, it's not clear how much use this is on
   the RI5.  It doesn't turn off lights etc.

.. function:: sleep([time_ms])

   .. note:: This function is deprecated, use `lightsleep()` instead.

.. function:: lightsleep([time_ms])
              deepsleep([time_ms])

   Stops execution in an attempt to enter a low power state.

   If *time_ms* is specified then this will be the maximum time in milliseconds that
   the sleep will last for.  Otherwise the sleep can last indefinitely.

   With or without a timout, execution may resume at any time if there are events
   that require processing.  Such events, or wake sources, should be configured before
   sleeping, like `Pin` change or `RTC` timeout.

   The precise behaviour and power-saving capabilities of lightsleep and deepsleep is
   highly dependent on the underlying hardware, but the general properties are:

   * A lightsleep has full RAM and state retention.  Upon wake execution is resumed
     from the point where the sleep was requested, with all subsystems operational.

   * A deepsleep may not retain RAM or any other state of the system (for example
     peripherals or network interfaces).  Upon wake execution is resumed from the main
     script, similar to a hard or power-on reset. The `reset_cause()` function will
     return `machine.DEEPSLEEP` and this can be used to distinguish a deepsleep wake
     from other resets.

   .. admonition:: Difference for RI5
      :class: attention

      See below for the specifics of how this works in practice for RI5.

   On the RI5, it's not clear that these are going to be particularly useful.

   * Lightsleep seems to potentially cut off the USB connection if you're running
     via the Mindstorms app, requiring you to restart the Hub and then the app
     to regain connection between the two.  It's possible this is just a bug.

   * Deepsleep obviously restarts the Hub from its startup script which will
     put you back in the menu unless you've done extensive customization.
     Although when you run a program after that it is then possible to check
     for the DEEPSLEEP reset cause.

   * It's not clear exactly how power-saving these modes are on the RI5.  In
     tests, both seemed to turn the Hub LED red (or on one weird and memorable
     occasion, green) for the duration of the sleep.

.. admonition:: Difference for RI5
   :class: attention

   Function ``wake_reason()`` is not implemented for the RI5.

Miscellaneous functions
-----------------------

.. function:: info([verbose])

   .. admonition:: Difference for RI5
      :class: attention

      A function specific to the RI5.

   Prints various information, including:

   * ID = The hex of the ``unique_id()``

   * S = System Clock frequency.  See ``freq()`` above.

   * H = AHB (Advanced High-Performance Bus) Clock frequency.  See ``freq()`` above.

   * P1 = APB1 (Advanced Peripheral Bus 1) Clock frequency.  See ``freq()`` above.

   * P2 = APB2 (Advanced Peripheral Bus 2) Clock frequency.  See ``freq()`` above.

   * "qstr" section with similar information to ``micropython.qstr_info()``

   * "GC" section with similar information to ``micropython.mem_info()``

   * If the ``verbose`` parameter is defined then it also prints the GC memory
     layout that you get from ``mem_info()``'s verbose mode.

.. function:: unique_id()

   Returns a byte string with a unique identifier of a board/SoC. It will vary
   from a board/SoC instance to another, if underlying hardware allows. Length
   varies by hardware (so use substring of a full value if you expect a short
   ID). In some MicroPython ports, ID corresponds to the network MAC address.

.. function:: time_pulse_us(pin, pulse_level, timeout_us=1000000)

   Time a pulse on the given *pin*, and return the duration of the pulse in
   microseconds.  The *pulse_level* argument should be 0 to time a low pulse
   or 1 to time a high pulse.

   If the current input value of the pin is different to *pulse_level*,
   the function first (*) waits until the pin input becomes equal to *pulse_level*,
   then (**) times the duration that the pin is equal to *pulse_level*.
   If the pin is already equal to *pulse_level* then timing starts straight away.

   The function will return -2 if there was timeout waiting for condition marked
   (*) above, and -1 if there was timeout during the main measurement, marked (**)
   above. The timeout is the same for both cases and given by *timeout_us* (which
   is in microseconds).

.. admonition:: Difference for RI5
   :class: attention

   Function ``rng()`` is not implemented for the RI5.

Memory Access
-------------

.. data:: mem8
          mem16
          mem32

   Supports machine memory access in 1-byte, 2-byte or 4-byte chunks.  Access
   is via indexing, where the index is the memory address of the beginning of
   the chunk.  (Attempts to use a wrongly aligned address for the chunk size
   cause a ValueError.)

   Beware that slicing doesn't work properly and may cause a system failure!

   On the RI5, be aware that 0 is a valid address: addressable memory goes from
   0 to 1572863 (=0x17FFFF) inclusive, representing 1.5 MiB.  Attempting to reference
   addresses outside of this causes a system restart.  Addresses from 0x08a670
   seem to all return 0xFF values though so I'm not sure how useful anything
   above this is...

   The system lets you attempt to set address contents with ``memX[index] = value``,
   but it doesn't seem to be effective - subsequent reads just show the old value
   again.

.. _machine_constants:

Constants
---------

.. admonition:: Difference for RI5
   :class: attention

   IRQ wake value constants and wake-up reason constants are not present on the RI5.

.. data:: machine.PWRON_RESET
          machine.HARD_RESET
          machine.WDT_RESET
          machine.DEEPSLEEP_RESET
          machine.SOFT_RESET

    Reset causes.

Classes
-------

.. toctree::
   :maxdepth: 1

   machine.Pin.rst
   machine.Signal.rst
   machine.ADC.rst
   machine.UART.rst
   machine.SPI.rst
   machine.I2C.rst
   machine.RTC.rst
   machine.Timer.rst
   machine.WDT.rst


Classes from default Micropython not present on the Hub
-------------------------------------------------------

* class ADCChannel - read analog values from internal or external sources

* class SD - secure digital memory card
