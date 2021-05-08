:mod:`programrunner` -- run user programs
=========================================

.. module:: programrunner
   :synopsis: run user programs

This module handles the running of user programs (i.e. the Scratch/Python
programs that live in the program slots on the system).

Functions
---------

.. function:: wait_until_ready_after_restart(???)

   ???

.. function:: rotate_hub_display_to_orientation(???)

   ???

.. function:: get_path(???)

   ???

.. function:: filter_dict_len(???)

   ???

.. function:: set_force_reset(???)

   ???

.. function:: reset_time(???)

   ???

.. function:: get_program_project_id(???)

   ???

.. function:: stop_time(???)

   ???

.. function:: get_program_type(???)

   ???

.. function:: get_event_loop(???)

   ???

.. function:: map_dirty(???)

   ???

.. function:: filter_vm_vars(???)

   ???

.. function:: sum_list_len(???)

   ???

.. function:: filter_vm_lists(???)

   ???

.. function:: setup_vm(???)

   Generator function.  ???

.. function:: untuple_vm_vars(???)

   Generator function.  ???

Constants
---------

.. data:: _EMPTY_DICT = {}

   ???

.. data:: LPF2_FLIPPER_DISTANCE = 62

   ???

.. data:: PROGRAM_TYPE_PYTHON = python

   ???

.. data:: PROGRAM_TYPE_SCRATCH = scratch

   ???

.. data:: PROGRAM_EXECUTION_ERROR = 0

   ???

.. data:: PROGRAM_EXECUTION_MEMORY_ERROR = 1

   ???

.. data:: TIMER_PACE_LOW = 48

   ???

.. data:: TIMER_PACE_HIGH = 16

   ???

.. data:: error_handler

   Reference to the main error handler object (type
   :class:util.error_handler.ErrorHandler).

Imports
-------

* Module :mod:util.sensors
* Module :mod:sys
* Module :mod:hub
* Module :mod:gc
* Module :mod:protocol.notifications
* Class :class:VirtualMachine from :mod:runtime.virtualmachine
* Function :func:const from :mod:micropython

Class ProgramRunner
-------------------

.. class:: ProgramRunner(???)

   ???

   Methods
   ~~~~~~~

   .. method:: __init__(???)

      ???

   .. method:: vm_has_extension(???)

      ???

   .. method:: start_program(???)

      ???

   .. method:: is_running(???)

      ???

   .. method:: start_notify_loop(???)

      Generator function.  ???

   .. method:: notify_all_state(???)

      ???

   .. method:: stop_all(???)

      ???

   Constants
   ~~~~~~~~~

   .. data:: IDLE = 0

      ???

   .. data:: RUNNING_NONBLOCKING = 1

      ???

   .. data:: RUNNING_BLOCKING = 2

      ???
