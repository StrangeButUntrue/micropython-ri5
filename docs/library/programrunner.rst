:mod:`programrunner` -- run user programs
=========================================

.. module:: programrunner
   :synopsis: run user programs

This module handles the running of user programs (i.e. the Scratch/Python
programs that live in the program slots on the system).

Functions
---------

.. function:: filter_dict_len(???)

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

.. data:: _EMPTY_DICT
   :value: {}

   ???

Class ProgramRunner
-------------------

.. class:: ProgramRunner(???)

   ???

   **Methods**

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

   **Constants**

   .. data:: IDLE
      :value: 0

      ???

   .. data:: RUNNING_NONBLOCKING
      :value: 1

      ???

   .. data:: RUNNING_BLOCKING
      :value: 2

      ???

Imports
-------

* Module `util.sensors`
* Module `sys`
* Module `hub`
* Module `gc`
* Module `protocol.notifications`
* Class `runtime.virtualmachine.VirtualMachine`
* Function `micropython.const`
* Function `event_loop.get_event_loop`
* Function `util.resetter.wait_until_ready_after_restart`
* Function `util.rotation.rotate_hub_display_to_orientation`
* Function `util.storage.get_path`
* Function `util.storage.set_force_reset`
* Function `util.storage.get_program_project_id`
* Function `util.storage.get_program_type`
* Function `util.time.reset_time`
* Function `util.time.stop_time`
* Constant `util.constants.LPF2_FLIPPER_DISTANCE` = 62
* Constant `util.constants.TIMER_PACE_LOW` = 48
* Constant `util.constants.TIMER_PACE_HIGH` = 16
* Constant `util.storage.PROGRAM_TYPE_PYTHON` = python
* Constant `util.storage.PROGRAM_TYPE_SCRATCH` = scratch
* Constant `util.error_handler.PROGRAM_EXECUTION_ERROR` = 0
* Constant `util.error_handler.PROGRAM_EXECUTION_MEMORY_ERROR` = 1
* Constant `util.error_handler.error_handler` = <Main ErrorHandler object>
