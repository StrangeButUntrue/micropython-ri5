:mod:`util.animations` -- animation utility module
==================================================

.. module:: util.animations
   :synopsis: animation utility module

???

Functions
---------

.. function:: shift_left(???)

   ???

.. function:: shift_right(???)

   ???

.. function:: shift_out_to_top(???)

   Generator function.  ???

.. function:: shift_in_from_right(???)

   Generator function.  ???

.. function:: shift_in_from_bottom_left(???)

   Generator function.  ???

.. function:: shift_out_to_bottom(???)

   Generator function.  ???

.. function:: shift_out_to_left(???)

   Generator function.  ???

.. function:: shift_in_from_left(???)

   Generator function.  ???

.. function:: shift_in_from_bottom(???)

   Generator function.  ???

.. function:: shift_out_to_right(???)

   Generator function.  ???

.. function:: shift_in_from_top_right(???)

   Generator function.  ???

.. function:: shift_in_from_top(???)

   Generator function.  ???

.. function:: streaming_animation(???)

   ???

.. function:: download_animation(???)

   ???

.. function:: bootup_animation(???)

   ???

.. function:: shutdown_animation(???)

   ???

.. function:: bt_animation(???)

   Generator function.  ???

.. function:: led_fade_to(???)

   Generator function.  ???

.. function:: led_fade_in_out(???)

   Generator function.  ???

.. function:: chain_animations(???)

   Generator function.  ???

Constants
---------

.. data:: DISPLAY_WIDTH
   :value: 5
.. data:: DISPLAY_HEIGHT
   :value: 5

   Constants for the display dimensions.

.. data:: BOOTUP_FRAMES
   :value: (Image('00000:00000:09000:00000:00000:'), Image('00000:00000:07000:00000:00000:'), Image('00000:00000:07000:00009:00000:'), Image('00000:00000:07000:00007:00000:'), Image('00000:00000:07000:90007:00000:'), Image('00000:00000:07000:70007:00000:'), Image('00000:90000:07000:70007:00000:'), Image('00000:70000:07000:70007:00000:'), Image('00000:70000:07000:70007:00900:'), Image('00000:70000:07000:70007:00700:'), Image('00000:70900:07000:70007:00700:'), Image('00090:70800:07000:70007:00700:'), Image('00080:70800:07000:79007:00700:'), Image('00080:70700:07090:78007:00700:'), Image('00070:70700:07080:78007:90700:'), Image('09070:70700:07070:77007:80700:'), Image('08070:70700:07070:77007:80709:'), Image('08079:70700:07070:77007:70708:'), Image('07078:70700:07070:77907:70708:'), Image('07078:79700:07070:77707:70707:'), Image('07077:78700:07079:77707:70707:'), Image('07077:78700:07078:77707:79707:'), Image('07977:78700:07078:77707:78707:'), Image('07877:77700:07078:77797:78707:'), Image('07877:77709:07077:77787:78707:'), Image('07877:77708:97077:77787:77707:'), Image('07777:77708:87077:77787:77797:'), Image('07777:77798:87077:77777:77787:'), Image('97777:77787:87077:77777:77787:'), Image('87777:77787:87977:77777:77787:'), Image('99999:99999:99999:99999:99999:'), Image('77777:77777:77777:77777:77777:'), Image('66669:66669:66669:66669:66669:'), Image('55599:55595:55595:55595:55599:'), Image('44999:44949:44949:44949:44999:'), Image('39993:39393:39393:39393:39993:'), Image('09990:09090:09090:09090:09990:'))

   The set of image objects that are displayed on the bootup animation.

.. data:: SHUTDOWN_FRAMES
   :value: (Image('99999:90009:90009:90009:99999:'), Image('55555:57775:57075:57775:55555:'), Image('00000:09990:09090:09990:00000:'), Image('00000:05550:05750:05550:00000:'), Image('00000:00000:00900:00000:00000:'), Image('00000:00000:00500:00000:00000:'), Image('00000:00000:00000:00000:00000:'))

   The set of image objects that are displayed on the shutdown animation.

Imports
-------
* Module `hub`
* Module `utime`
* Class `util.constants.Image`
* Function `util.color.color_percentage`
* Function `util.color.get_color_percentage`
* Constant `util.color.BLACK` = (0, 0, 0)
* Constant `util.color.DIM_WHITE` = (135, 25, 10)
