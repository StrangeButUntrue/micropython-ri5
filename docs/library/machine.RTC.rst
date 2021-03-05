.. currentmodule:: machine
.. _machine.RTC:

class RTC -- real time clock
============================

The RTC is an independent clock that keeps track of the date
and time.  As noted in the utime module, it defaults to 2015-01-01 00:00:00 UTC
and only seems to start running when it's used (calling any of the functions below
except ``info()`` will start it running.)

Example usage::

    rtc = machine.RTC()
    rtc.datetime((2014, 5, 1, 4, 13, 0, 0, 0))
    print(rtc.datetime())


Constructors
------------

.. class:: machine.RTC()

   Create an RTC object.


Methods
-------

.. method:: RTC.datetime([datetimetuple])

   Get or set the date and time of the RTC.

   With no arguments, this method returns an 8-tuple with the current
   date and time.  With 1 argument (being an 8-tuple) it sets the date
   and time (and ``subseconds`` is reset to 255).

   The 8-tuple has the following format:

       (year, month, day, weekday, hours, minutes, seconds, subseconds)

   ``weekday`` is 1-7 for Monday through Sunday.

   ``subseconds`` counts down from 255 to 0

   Very little error-checking seems to be done on the input values so be
   aware that the RTC will try to work with whatever you give it, with
   potentially undefined results.  It won't successfully set years below 2000
   though.

.. method:: RTC.wakeup(timeout, callback=None)

   Set the RTC wakeup timer to trigger repeatedly at every ``timeout``
   milliseconds.

   If ``timeout`` is ``None`` then the wakeup timer is disabled.

   If ``callback`` is given then it is executed at every trigger of the
   wakeup timer.  ``callback`` must take exactly one argument.  It's not
   clear what this does - it appears to be uninitialised on entry.

.. method:: RTC.info()

   Get information about the startup time and reset source.  If the RTC hasn't
   yet been started, this seems to take value 1056964608 (= 0x3F000000).
   Otherwise, it's not quite clear what the value means - in experiments it
   always seems to have high bit 0x20000000 set, and then some value in the
   lower 0xFFFF.  Base MicroPython docs claim:

    - The lower 0xffff are the number of milliseconds the RTC took to
      start up.
    - Bit 0x10000 is set if a power-on reset occurred.
    - Bit 0x20000 is set if an external reset occurred

   But on the RI5 I've seen lower bit values of 16658 and 27119 which don't
   seem to correspond to a startup time...

.. method:: RTC.calibration(cal)

   Get or set RTC calibration.

   With no arguments, ``calibration()`` returns the current calibration
   value, which is an integer in the range [-511 : 512].  With one
   argument it sets the RTC calibration.

   The RTC Smooth Calibration mechanism adjusts the RTC clock rate by
   adding or subtracting the given number of ticks from the 32768 Hz
   clock over a 32 second period (corresponding to 2^20 clock ticks.)
   Each tick added will speed up the clock by 1 part in 2^20, or 0.954
   ppm; likewise the RTC clock it slowed by negative values. The
   usable calibration range is:
   (-511 * 0.954) ~= -487.5 ppm up to (512 * 0.954) ~= 488.5 ppm

   Default calibration on the RI5 is 0, although it's presumably likely to
   vary by system (and maybe even vary over time?) what value is best to
   make the RTC approximate real time.