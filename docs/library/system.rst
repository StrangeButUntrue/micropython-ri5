:mod:`system` -- system module
==============================

.. module:: system
   :synopsis: system module

Module containing a lot of high-level concepts, but no obvious theme beyond
that.

Classes `system.callbacks.Callbacks`, `system.display.DisplayWrapper`,
`system.move.Movement`, `system.motors.Motors`, `system.sound.SoundWrapper`
have aliases in the main namespace for convenience.

Constants
---------
.. data:: system

   Reference to the main System object.

System Class
------------

.. class:: System(???)

   ???

   .. method:: reset(???)

      ???

Submodules
----------

.. toctree::
   :maxdepth: 1

   system.callbacks.rst
   system.motors.rst
   system.motorwrapper.rst
   system.sound.rst
   system.move.rst
   system.movewrapper.rst
   system.abstractwrapper.rst
   system.display.rst

Imports
-------
* Module `hub`
* Function `event_loop.get_event_loop`
