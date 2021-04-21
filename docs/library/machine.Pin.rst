.. currentmodule:: machine
.. _machine.Pin:

class Pin -- control I/O pins
=============================

A pin object is used to control I/O pins (also known as GPIO - general-purpose
input/output).  Pin objects are commonly associated with a physical pin that can
drive an output voltage and read input voltages.  The pin class has methods to set the mode of
the pin (IN, OUT, etc) and methods to get and set the digital logic level.
For analog control of a pin, see the :class:`ADC` class.

A pin object is constructed by using an identifier which unambiguously
specifies a certain I/O pin.  The allowed form of the identifier in the RI5 case
is a string that specifies the board-name or cpu-name of the pin.  Pins can also be
selected via the cpu and board convenience classes within Pin.

Usage Model::

    from machine import Pin

    # create an output pin on pin X0
    p0 = Pin('X0', Pin.OUT)

    # set the value low then high
    p0.value(0)
    p0.value(1)

    # create an input pin on pin X1, with a pull up resistor
    p2 = Pin('X1', Pin.IN, Pin.PULL_UP)

    # read and print the pin value
    print(p2.value())

    # reconfigure pin X0 in input mode
    p0.mode(p0.IN)

    # configure an irq callback
    p0.irq(lambda p:print(p))

Constructors
------------

.. class:: Pin(id)
.. class:: Pin(id, mode, pull=None, af=-1, \* value, alt=-1)

   Access the pin peripheral (GPIO pin) associated with the given ``id``.  If
   additional arguments are given in the constructor then they are used to initialise
   the pin.  If no settings are specified they will remain in their previous state.

   The arguments are:

     - ``id`` is mandatory and can be either an existing Pin object or a string
       that identifies one.  String identifiers can be either the cpu-name or the
       board-name of a Pin.

     - ``mode`` specifies the pin mode, which can be one of:

       - ``Pin.IN`` - Pin is configured for input (i.e. for getting values
         from the outside world into the CPU).  If viewed as an output the pin
         is in high-impedance state.

       - ``Pin.OUT`` - Pin is configured for (normal) output (i.e. for letting
         the program set values).

       - ``Pin.OPEN_DRAIN`` - Pin is configured for open-drain output. Open-drain
         output works in the following way: if the output value is set to 0 the pin
         is active at a low level; if the output value is 1 the pin is in a high-impedance
         state.  Some pins may not implement this mode.

       - ``Pin.ALT`` - Pin is configured to perform an alternative function.  Available
         alt-functions are specific to particular pins.  For a pin configured in such a
         way any other Pin methods (except :meth:`Pin.init`) are not necessarily applicable
         (calling them will lead to undefined, or a hardware-specific, result).

       - ``Pin.ALT_OPEN_DRAIN`` - The Same as ``Pin.ALT``, but the pin is configured as
         open-drain.  Not all ports implement this mode.

       - ``Pin.ANALOG`` - The pin is configured as an analog input/output instead
         of digital, and voltages will be read instead of binary 0/1 states.  Use
         the :class:`ADC` class instead of the functions below on pins in this mode.
         Some pins may not implement this mode.

     - ``pull`` specifies if the pin has a (weak) pull resistor attached, and can be
       one of:

       - ``None``/``Pin.PULL_NONE`` - No pull up or down resistor.
       - ``Pin.PULL_UP`` - Pull up resistor enabled.
       - ``Pin.PULL_DOWN`` - Pull down resistor enabled.

     - ``af`` is a legacy (positional) alternative to ``alt`` with exactly the same
       values - the other parameter takes precedence over it.

     - ``value`` is valid only for Pin.OUT and Pin.OPEN_DRAIN modes and specifies initial
       output pin value if given, otherwise the state of the pin peripheral remains
       unchanged.

     - ``alt`` specifies an alternate function for the pin.  The values it can take are
       0-15, although whether these will do anything is pin-dependent.  The alt argument
       is valid only for ``Pin.ALT`` and ``Pin.ALT_OPEN_DRAIN`` modes and must be specified
       for those modes.  For other modes it is ignored.

   As specified above, the Pin class allows to set an alternate function or analog mode
   for a particular pin, but it does not specify any further operations on such a pin.
   Pins configured in alternate-function or analog mode are usually not used as GPIO
   but are instead driven by other hardware peripherals.  Sometimes they may be usable
   with other machine subclasses.  The only Pin operation supported on such a pin is
   re-initialising, by calling the constructor or :meth:`Pin.init` method.  If a pin
   that is configured in alternate-function mode is re-initialised with ``Pin.IN``,
   ``Pin.OUT``, or ``Pin.OPEN_DRAIN``, the alternate function will be removed from the pin.

Methods
-------

.. method:: Pin.init(mode, pull=None, af=-1 \*, value, alt=-1)

   Re-initialise the pin using the given parameters.  If ``value`` is unspecified,
   it will not be set, but the other arguments are always set (to the defaults
   where suitable).

   See the constructor documentation for details of the arguments.

   Returns ``None``.

   Note that since this is modifying hardware state, changing parameters here
   will be reflected in any other objects referencing the same physical pin.

.. method:: Pin.value([x])

   This method allows to set and get the value of the pin, depending on whether
   the argument ``x`` is supplied or not.

   If the argument is omitted then this method gets the digital logic level of
   the pin, returning 0 or 1 corresponding to low and high voltage signals
   respectively.  The behaviour of this method depends on the mode of the pin:

     - ``Pin.IN`` - The method returns the actual input value currently present
       on the pin.
     - ``Pin.OUT`` - The behaviour and return value of the method is undefined.
     - ``Pin.OPEN_DRAIN`` - If the pin is in state '0' then the behaviour and
       return value of the method is undefined.  Otherwise, if the pin is in
       state '1', the method returns the actual input value currently present
       on the pin.

   If the argument is supplied then this method sets the digital logic level of
   the pin.  The argument ``x`` can be anything that converts to a boolean.
   If it converts to ``True``, the pin is set to state '1', otherwise it is set
   to state '0'.  The behaviour of this method depends on the mode of the pin:

     - ``Pin.IN`` - The value is stored in the output buffer for the pin.  The
       pin state does not change, it remains in the high-impedance state.  The
       stored value will become active on the pin as soon as it is changed to
       ``Pin.OUT`` or ``Pin.OPEN_DRAIN`` mode.
     - ``Pin.OUT`` - The output buffer is set to the given value immediately.
     - ``Pin.OPEN_DRAIN`` - If the value is '0' the pin is set to a low voltage
       state.  Otherwise the pin is set to high-impedance state.

   When setting the value this method returns ``None``.

   Behaviour is undefined always for pins in ALT or ANALOG modes.

.. method:: Pin.__call__([x])

   Pin objects are callable.  The call method provides a (fast) shortcut to set
   and get the value of the pin.  It is equivalent to Pin.value([x]).
   See :meth:`Pin.value` for more details.

.. method:: Pin.on()
.. method:: Pin.high()

   Set pin to "1" output level.

.. method:: Pin.off()
.. method:: Pin.low()

   Set pin to "0" output level.

.. method:: Pin.mode()

   Returns the pin mode in numeric form.
   See the constructor documentation for details of the ``mode`` argument.
   Unlike base MicroPython, the STM32 port doesn't let you set mode with this
   method.

.. method:: Pin.pull()

   Returns the pin pull state in numeric form.
   See the constructor documentation for details of the ``pull`` argument.
   Unlike base MicroPython, the STM32 port doesn't let you set pull with this
   method.

.. method:: Pin.irq(handler=None, trigger=(Pin.IRQ_FALLING | Pin.IRQ_RISING), hard=False)

   Configure an interrupt handler to be called when the trigger source of the
   pin is active.  If the pin mode is ``Pin.IN`` then the trigger source is
   the external value on the pin.  If the pin mode is ``Pin.OUT`` then the
   trigger source is the output buffer of the pin.  Otherwise, if the pin mode
   is ``Pin.OPEN_DRAIN`` then the trigger source is the output buffer for
   state '0' and the external pin value for state '1'.

   The arguments (all optional and can be positonal or named) are:

     - ``handler`` is an optional function to be called when the interrupt
       triggers. The handler must take exactly one argument which is the
       ``Pin`` instance.

     - ``trigger`` configures the event which can generate an interrupt.
       Possible values are:

       - ``Pin.IRQ_FALLING`` interrupt on falling edge.
       - ``Pin.IRQ_RISING`` interrupt on rising edge.

       These values can be OR'ed together to trigger on multiple events.

     - ``hard`` if true a hardware interrupt is used. This reduces the delay
       between the pin change and the handler being called. Hard interrupt
       handlers may not allocate memory; see :ref:`isr_rules`.

   This method returns ``None``.  Since it doesn't return any kind of IRQ object,
   there's no way to turn the IRQ off again (presumably even when the program
   exits) so this function will probably be of limited use on the RI5 unless
   you want permanent control of a pin until the system is reset.  And that's
   assuming you can make this work - all my attempts at using this function
   either did nothing (on pins that had constant value) or crashed the system!

.. method:: Pin.name()

   Returns the pin name.  (This will be the CPU-based form.)

.. method:: Pin.names()

   Returns a list containing the cpu- and board-based names for the pin in that
   order.

.. method:: Pin.af_list()

   Returns an array of alternate functions available for this pin, in the form
   of constants like Pin.AF1_TIM1 and Pin.AF5_I2S4.

.. method:: Pin.port()

   Returns the pin port in numeric form.  (A=0 to H=7)

.. method:: Pin.pin()

   Returns the pin number.  (The 0-15 number of the pin that comes after the
   port letter.)

.. method:: Pin.gpio()

   Returns the base address of the GPIO block associated with this pin.

.. method:: Pin.af()

   Returns the currently configured alternate function of the pin in numeric
   form.  This will match one of the allowed constants for the ``af`` argument
   to ``init()``.

Class methods
-------------

.. admonition:: Difference for RI5
   :class: attention

   These three functions define global behaviour which persists past the end
   of a program back into the hub menu, and so could conceivably cause future
   programs to break.

.. method:: Pin.mapper([map_function])

   Given a parameter, stores a global mapping function, which should be a function
   that takes a single string and returns a pin object.  (ValueError is thrown
   if it returns something else.)  Once specified this function takes precedence
   over the default way of mapping strings to Pins.  It may return None, at which
   point other lookup types are attempted.

   With no parameter it returns the current mapper function.

.. method:: Pin.dict(mapping_dict)

   Given a parameter, specifies a global dictionary to be used to map strings
   to pin objects.  If specified, this method of mapping takes precedence over
   the default way of mapping strings to Pins.  But the mapper function takes
   precedence over this.

   Note that nothing checks the output of this mapping to make sure it's
   actually returning a Pin object.

   With no parameter it returns the current mapping dictionary.

.. method:: Pin.debug(debug_info)

   Sets global debug information on/off according to the boolean ``debug_info``.
   Debug information (printed to stsandard output stream) tells you more about
   how a given string is mapped to a Pin object.

Classes
-------

.. class:: board
.. class:: cpu

   Two classes containing constant objects for all the pins on the
   system.  In the cpu class these take the raw form cpu.A0 to cpu.H1.  (Port
   letter plus pin number.)  In the board class most are just named board.PA0 to
   board.PH1, but some have been translated into more meaningful names:
   A1 = ``board.BUTTON3_SW``, A11 = ``board.USB_DM``, A12 = ``board.USB_DP``,
   A14 = ``board.TEST_LED``.

   .. admonition:: Difference for RI5
      :class: attention

      The more meaningful board names here appear to be unique to the RI5, or
      at least I couldn't find other sources for them all online.

Constants
---------

The following constants are used to configure the pin objects.

.. data:: Pin.IN = 0
          Pin.OUT = 1
          Pin.OPEN_DRAIN = 17
          Pin.ALT = 2
          Pin.ALT_OPEN_DRAIN = 18
          Pin.ANALOG = 3

   Selects the pin mode.

.. data:: Pin.PULL_NONE = 0
          Pin.PULL_UP = 1
          Pin.PULL_DOWN = 2

   Selects whether there is a pull up/down resistor.

.. data:: Pin.IRQ_FALLING = 0x10210000
          Pin.IRQ_RISING = 0x10110000

   Selects the IRQ trigger type.

.. data:: Pin.OUT_PP = 1
          Pin.OUT_OD = 17
          Pin.AF_PP = 2
          Pin.AF_OD = 18

   Legacy constants (synonyms for pin modes above).

.. data:: Pin.AFx_*

   Lots of constants describing the possible alternate functions.  These match
   the alternate function numbers described at
   https://github.com/micropython/micropython/blob/master/ports/stm32/boards/stm32f413_af.csv
   or at least the subset that this board supports.
