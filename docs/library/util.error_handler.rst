:mod:`util.error_handler` -- error handling utility module
==========================================================

.. module:: util.error_handler
   :synopsis: error handling utility module

???

Constants
---------
.. data:: error_handler
   :value: <Main ErrorHandler object>

.. data:: PROGRAM_EXECUTION_ERROR
   :value: 0

   ???

.. data:: PROGRAM_EXECUTION_MEMORY_ERROR
   :value: 1

   ???

ErrorHandler Class
------------------

.. class:: ErrorHandler(???)

   ???

   .. method:: handle_user_program_error(???)

      ???

   .. method:: handle_notify_error(???)

      ???

   .. method:: handle_runtime_error(???)

      ???

   .. method:: initialize(???)

      ???

   .. method:: _emit_runtime_error(???)

      ???

   .. method:: _handle_error(???)

      ???

Imports
-------
* Module `hub`
* Module `protocol.notifications`
* Module `sys`
* Module `uio`
* Module `ure`
* Module `version`
* Function `event_loop.get_event_loop`
* Function `micropython.const`
* Function `ubinascii.b2a_base64`
* Function `util.log.log_critical_error`
* Constant `util.color.BLACK` = (0, 0, 0)
* Constant `util.color.RED` = (255, 0, 0)
