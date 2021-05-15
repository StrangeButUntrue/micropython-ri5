:mod:`system.callbacks` -- ???
==============================

.. module:: system.callbacks
   :synopsis: ???

???

The main namespace contains an alias for
`system.callbacks.customcallbacks.CustomSensorCallbackManager` for convenience.

Submodules
----------

.. toctree::
   :maxdepth: 1

   system.callbacks.customcallbacks.rst

Classes
-------

.. class:: Callbacks(???)

   ???

   .. method:: reset(???)

      ???

   .. method:: hard_reset(???)

      ???

.. class:: ButtonCallbacks(???)

   ???

   .. method:: reset(???)

      ???

   .. method:: hard_reset(???)

      ???

   .. method:: register_rpc_handlers(???)

      ???

   .. method:: __getitem__(???)

      ???

.. class:: PortCallbacks(???)

   ???

   .. method:: reset(???)

      ???

   .. method:: hard_reset(???)

      ???

   .. method:: init_attach(???)

      ???

   .. method:: __getitem__(???)

      ???

.. class:: CallbackHandler(???)

   ???

   .. method:: reset(???)

      ???

   .. method:: hard_reset(???)

      ???

   .. method:: callback(???)

      ???

   .. method:: register(???)

      ???

   .. method:: register_single(???)

      ???

   .. method:: register_persistent(???)

      ???

.. class:: ConnectionCallbacks(???)

   ???

   .. method:: __uch(???)

      ???

   .. method:: check_state(???)

      ???

Imports
-------
* Module `hub`
* Function `protocol.notifications.notify_button_event`
* Function `util.schedule.mp_schedule`
* Constant `util.constants.BT_VCP` = BT_VCP(0) <Bluetooth connection object>
* Constant `util.constants.USB_VCP` = USB_VCP(0) <USB connection object>
* Constant `util.error_handler.error_handler` = <Main ErrorHandler object>
