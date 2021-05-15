:mod:`runtime.stack` -- ???
===========================

.. module:: runtime.stack
   :synopsis: ???

Contains the Stack class.  ???

Stack Class
-----------

.. class:: Stack(???)

   ???

   **Methods**
   .. method:: is_active(???)

      ???

   .. method:: should_start(???)

      ???

   .. method:: _check_condition(???)

      Generator function.  ???

   .. method:: stop(???)

      ???

   .. method:: restart(???)

      ???

   .. method:: start(???)

      ???

   **Constants**
   .. data:: STATUS_RUNNING
      :value: 10

      ???

   .. data:: STATUS_IDLE
      :value: 20

      ???

   .. data:: STATUS_WAITING
      :value: 30

      ???

   .. data:: ON_START
      :value: 0

      ???

   .. data:: ON_BROADCAST
      :value: 1

      ???

   .. data:: ON_BUTTON
      :value: 2

      ???

   .. data:: ON_GESTURE
      :value: 3

      ???

   .. data:: ON_CONDITION
      :value: 4

      ???

Imports
-------
* Function `micropython.const`
* Function `protocol.notifications.notify_stack_start`
* Function `protocol.notifications.notify_stack_stop`