:mod:`ui.hubui` -- menu system
==============================

.. module:: ui.hubui
   :synopsis: menu system

Runs the menu system that you see when you boot up the Hub (and between running
programs).  The entire functionality is contained in submodule ui.hubui,
although the main module also aliases the ui.hubui.HubUI class as ui.HubUI.

Functions
---------

.. function:: reset(???)

   ???

.. function:: user_interaction(???)

   ???

Variables
---------

.. data:: _latest_activity

   ???

Constants
---------

.. data:: INACTIVE_SHUTDOWN_BT_MS
   :value: 1200000

   ???

.. data:: INACTIVE_SHUTDOWN_MS
   :value: 300000

   ???

.. data:: DEFAULT_IMAGE
   :value: (Image('09090:99999:99999:09990:00900:'), Image('09000:09900:09990:09900:09000:'))

   ???

.. data:: SLOTS_IMAGE
   :value: (Image('09990:09090:09090:09090:09990:'), Image('00900:09900:00900:00900:09990:'), Image('09990:00090:09990:09000:09990:'), Image('09990:00090:09990:00090:09990:'), Image('09090:09090:09990:00090:00090:'), Image('09990:09000:09990:00090:09990:'), Image('09990:09000:09990:09090:09990:'), Image('09990:00090:00900:09000:09000:'), Image('09990:09090:09990:09090:09990:'), Image('09990:09090:09990:00090:09990:'), Image('90999:90909:90909:90909:90999:'), Image('09009:99099:09009:09009:09009:'), Image('90999:90009:90999:90900:90999:'), Image('90999:90009:90999:90009:90999:'), Image('90909:90909:90999:90009:90009:'), Image('90999:90900:90999:90009:90999:'), Image('90999:90900:90999:90909:90999:'), Image('90999:90009:90090:90900:90900:'), Image('90999:90909:90999:90909:90999:'), Image('90999:90909:90999:90009:90999:'))

   ???

Class HubUI
-----------

.. class:: HubUI(???)

   ???

   **Methods**

   .. method:: __bt_disconnect(???)

      ???

   .. method:: __toggle_program(???)

      ???

   .. method:: __change_slot(???)

      Closure function.  ???

   .. method:: _program_start(???)

      Generator function.  ???

   .. method:: stop_all(???)

      Closure function.  ???

   .. method:: change_execution_mode(???)

      Closure function.  ???

   .. method:: start_program(???)

      Closure function.  ???

   .. method:: __cancel_animations(???)

      ???

   .. method:: __start_autoshutdown(???)

      ???

   .. method:: __on_center_button(???)

      Closure function.  ???

   .. method:: _program_stop(???)

      Generator function.  ???

   .. method:: __get_slot_image(???)

      ???

   .. method:: __on_connect_button(???)

      Closure function.  ???

   .. method:: __bt_connect(???)

      ???

   .. method:: will_stop_restart(???)

      ???

   .. method:: __shutdown_timer(???)

      ???

   .. method:: on_connection(???)

      Closure function.  ???

   *Properties*

   .. property:: idle

      ???

Imports
-------
* Module `hub`
* Module `utime`
* Class `ProgramRunner`
* Class `Sounds`
* Class `system.System`
* Function `event_loop.get_event_loop`
* Function `micropython.const`
* Function `util.animations.bootup_animation`
* Generator function `util.animations.bt_animation`
* Function `util.animations.download_animation`
* Generator function `util.animations.led_fade_to`
* Function `util.animations.shutdown_animation`
* Function `util.animations.streaming_animation`
* Generator function `util.animations.shift_in_from_bottom`
* Generator function `util.animations.shift_out_to_bottom`
* Function `util.storage.get_used_slots`
* Constant `util.color.DIM_WHITE` = (135, 25, 10)
* Constant `util.color.WHITE` = (255, 70, 35)