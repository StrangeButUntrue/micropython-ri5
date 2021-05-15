:mod:`commands` -- commands module
==================================

.. module:: commands
   :synopsis: commands module

Module containing a lot of high-level concepts, but no obvious theme beyond
that.  Mostly organised into submodules *_methods containing *Methods classes,
which are all also aliased in the main module for convenience and seem to
implement the `commands.abstract_handler.AbstractHandler` class.

Submodules
----------

.. toctree::
   :maxdepth: 1

   commands.abstract_handler.rst
   commands.linegraphmonitor_methods.rst
   commands.sound_methods.rst
   commands.light_methods.rst
   commands.program_methods.rst
   commands.motor_methods.rst
   commands.hub_methods.rst
   commands.wait_methods.rst
   commands.move_methods.rst
