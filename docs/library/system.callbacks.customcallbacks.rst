:mod:`system.callbacks.customcallbacks` -- ???
==============================================

.. module:: system.callbacks.customcallbacks
   :synopsis: ???

???



Classes
-------

.. class:: CustomSensorCallbackManager(???)

   ???

   **Methods**

   .. staticmethod:: is_less_than(???)

      ???

   .. staticmethod:: did_bump(???)

      ???

   .. staticmethod:: did_change(???)

      ???

   .. method:: until(???)

      Generator function.  ???

   .. method:: until_less_than(???)

      Generator function.  ???

   .. method:: until_force_bumped(???)

      Generator function.  ???

   .. method:: until_changed(???)

      Generator function.  ???

   .. method:: wait_until_less_than(???)

      ???

   .. method:: wait_until_force_bumped(???)

      ???

   .. method:: wait_until_changed(???)

      ???

   .. method:: _start_test_task(???)

      ???

   .. method:: remove_task(???)

      ???

   .. method:: clear_tasks(???)

      ???

   **Variables**

   .. data:: _active_tasks

      ???  Observed value: []

Imports
-------
* Module `utime`
* Function `event_loop.get_event_loop`
* Function `micropython.const`
* Function `util.sensors.get_sensor_value`
* Constant `util.constants.LPF2_FLIPPER_FORCE` = 63
