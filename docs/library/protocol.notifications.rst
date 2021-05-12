:mod:`protocol.notifications` -- ???
====================================

.. module:: protocol.notifications
   :synopsis: ???

???

Functions
---------
.. function:: notify_error_event(???)

   ???

.. function:: notify_sensor_data(???)

   ???

.. function:: notify_storage_status(???)

   ???

.. function:: notify_stack_start(???)

   ???

.. function:: notify_battery_status(???)

   ???

.. function:: notify_program_running(???)

   ???

.. function:: notify_gesture_event(???)

   ???

.. function:: notify_info_status(???)

   ???

.. function:: notify_vm_state(???)

   ???

.. function:: notify_stack_stop(???)

   ???

.. function:: notify_linegraph_timer_reset(???)

   ???

.. function:: notify_debug_event(???)

   ???

.. function:: notify_button_event(???)

   ???

.. function:: notify_gesture_status(???)

   ???


Constants
---------
.. data:: _RQ_LEN
   :value: run_queue_len

   ???

.. data:: _MEM
   :value: mem_alloc

   ???

.. data:: _D
   :value: mem_delta

   ???

.. data:: _DEBUG_PAYLOAD
   :value: {'wait_queue_len': 0, 'mem_delta': 0, 'run_queue_len': 0, 'mem_alloc': 0}

   ???

.. data:: _WQ_LEN
   :value: wait_queue_len

   ???

Imports
-------
* Module `hub`
* Function `gc.mem_alloc`
* Function `micropython.const`
* Function `ubinascii.b2a_base64`
* Function `util.storage.get_storage_information`
* Function `util.storage.read_local_name`
* Variable `util.sensors.battery_status`
* Variable `util.sensors.sensor_data`