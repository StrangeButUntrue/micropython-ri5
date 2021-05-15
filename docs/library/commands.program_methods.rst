:mod:`commands.program_methods` -- ???
======================================

.. module:: commands.program_methods
   :synopsis: ???

???

Constants
---------

.. data:: _PRINT_OVERRIDE
   :value: "from util.print_override import spikeprint;print = spikeprint\n"

   Code to override the regular print statement with the special RI5 one.

.. data:: _TRANSFER_HANDLE
   :value: {}

   ???

ProgramMethods Class
------------------
.. class:: ProgramMethods(???)

   ???

   **Methods**

   .. method:: __init__(???)

      Closure function.  ???

   .. method:: get_methods(???)

      ???

   .. method:: handle_write_package(???)

      ???

   .. method:: handle_program_reset_time(???)

      ???

   .. method:: handle_program_start_time(???)

      ???

   .. method:: handle_soft_reset(???)

      ???

   .. method:: _handle_write_print_override(???)

      ???

   .. method:: handle_program_execute(???)

      ???

   .. method:: handle_start_write_program(???)

      ???

   .. method:: handle_remove_project(???)

      ???

   .. method:: handle_program_terminate(???)

      ???

   .. method:: handle_program_modechange(???)

      ???

   .. method:: handle_program_get_time(???)

      ???

   .. method:: handle_storage_status(???)

      ???

   .. method:: handle_move_project(???)

      ???

Imports
-------
* Module `commands.abstract_handler.AbstractHandler`
* Module `protocol.notifications`
* Module `sys`
* Module `urandom`
* Module `util.storage`
* Module `utime`
* Function `micropython.const`
* Function `ubinascii.a2b_base64`
* Function `util.time.get_time`
* Function `util.time.reset_time`
* Function `util.time.start_time`
