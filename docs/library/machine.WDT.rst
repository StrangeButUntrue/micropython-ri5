.. currentmodule:: machine
.. _machine.WDT:

class WDT -- watchdog timer
===========================

The WDT is used to restart the system when the application crashes and ends
up into a non recoverable state. Once started it cannot be stopped or
reconfigured in any way. After enabling, the application must "feed" the
watchdog periodically to prevent it from expiring and resetting the system.

Note that on the RI5, the WDT will continue running after a program ends, and
it will still reset the system if it expires during another program or in the
menu system.  A hard reset will get rid of it though.

Example usage::

    from machine import WDT
    wdt = WDT(timeout=2000)  # enable it with a timeout of 2s
    wdt.feed()

Constructors
------------

.. class:: WDT(id=0, timeout=5000)

   Create a WDT object and start it. The timeout must be given in seconds and
   the minimum value that is accepted is 1 second. Once it is running the timeout
   cannot be changed and the WDT cannot be stopped either.

Methods
-------

.. method:: wdt.feed()

   Feed the WDT to prevent it from resetting the system. The application
   should place this call in a sensible place ensuring that the WDT is
   only fed after verifying that everything is functioning correctly.

   On the RI5, note that if you've used a particular WDT before ever, feeding
   it starts it running, even if it wasn't running after a reset!  The system
   seems to remember that a WDT has been used even after a full power off,
   although it may reset to the default timeout.
