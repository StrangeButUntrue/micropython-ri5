:mod:`util.constants` -- constants module
=========================================

.. module:: util.constants
   :synopsis: constants module

???

Constants
---------

.. data:: LPF2_FLIPPER_MOTOR_MEDIUM
   :value: 48
.. data:: LPF2_FLIPPER_MOTOR_LARGE
   :value: 49
.. data:: LPF2_ACCELERATION
   :value: 57
.. data:: LPF2_GYRO
   :value: 58
.. data:: LPF2_ORIENTATION
   :value: 59
.. data:: LPF2_FLIPPER_COLOR
   :value: 61
.. data:: LPF2_FLIPPER_DISTANCE
   :value: 62
.. data:: LPF2_FLIPPER_FORCE
   :value: 63
.. data:: LPF2_FLIPPER_MOTOR_SMALL
   :value: 65
.. data:: LPF2_STONE_GREY_MOTOR_MEDIUM
   :value: 75
.. data:: LPF2_STONE_GREY_MOTOR_LARGE
   :value: 76

   Constants to represent various types of input device.  They correspond to
   official PoweredUp/SpikePrime Type IDs - see for example
   https://github.com/pybricks/technical-info/blob/master/assigned-numbers.md

.. data:: MOTOR_TYPES
   :value: (65, 48, 49, 75, 76)

   A tuple specifying which of the above types are motors.

.. data:: DEFAULT_IMAGE
   :value: (Image('09090:99999:99999:09990:00900:'), Image('09000:09900:09990:09900:09000:'))

   Two Image objects that are the default initial display screens on the
   Spike Prime and the RI5 firmwares respectively.

.. data:: SLOTS_IMAGE
   :value: (Image('09990:09090:09090:09090:09990:'), Image('00900:09900:00900:00900:09990:'), Image('09990:00090:09990:09000:09990:'), Image('09990:00090:09990:00090:09990:'), Image('09090:09090:09990:00090:00090:'), Image('09990:09000:09990:00090:09990:'), Image('09990:09000:09990:09090:09990:'), Image('09990:00090:00900:09000:09000:'), Image('09990:09090:09990:09090:09990:'), Image('09990:09090:09990:00090:09990:'), Image('90999:90909:90909:90909:90999:'), Image('09009:99099:09009:09009:09009:'), Image('90999:90009:90999:90900:90999:'), Image('90999:90009:90999:90009:90999:'), Image('90909:90909:90999:90009:90009:'), Image('90999:90900:90999:90009:90999:'), Image('90999:90900:90999:90909:90999:'), Image('90999:90009:90090:90900:90900:'), Image('90999:90909:90999:90909:90999:'), Image('90999:90909:90999:90009:90999:'))

   Image objects shown in the menu system when navigating between slots
   (they are the numbers 0 - 19).

.. data:: PORTS
   :value: {'C': Port(C), 'B': Port(B), 'D': Port(D), 'E': Port(E), 'A': Port(A), 'F': Port(F)}

   Dictionary mapping port names to the corresponding Port objects (see
   `hub.Port`).

.. data:: FLOAT
   :value: 0
.. data:: BRAKE
   :value: 1
.. data:: HOLD
   :value: 2

   Modes of operation for stopping a motor.  FLOAT simply removes power and
   allows coasting, while BRAKE reverses power to stop the motor as soon as
   possible, and HOLD mode will deliberately try to return to the braked point
   if it is moved away from it.

.. data:: USB_VCP
   :value: USB_VCP(0)
.. data:: BT_VCP
   :value: BT_VCP(0)

   Aliases for the main USB and Bluetooth objects on the Hub.  See
   `hub.USB_VCP` and `hub.BT_VCP`.

.. data:: NO_KEY
   :value: -1
.. data:: NUMBER
   :value: 0
.. data:: STRING
   :value: 1
.. data:: BOOLEAN
   :value: 2
.. data:: VAR_DEFAULTS
   :value: {0: 0, 1: '', 2: False}

   Imported by `util.scratch`.  Seems to be representing basic scratch data
   types numerically, with a dictionary to look up their default values.

.. data:: TIMER_PACE_LOW
   :value: 48
.. data:: TIMER_PACE_HIGH
   :value: 16

   Imported by `programrunner` and `hub_runtime`.  ???

.. data:: INACTIVE_SHUTDOWN_MS
   :value: 300000
.. data:: INACTIVE_SHUTDOWN_BT_MS
   :value: 1200000

   Imported by `ui.hubui`.  Presumably they represent the length of inactive
   time before the system shuts down.  Perhaps when running alone, and when
   connected to bluetooth?

.. data:: LONG_PRESS_MS
   :value: 3000

   Not obviously used anywhere.  ???

.. data:: SUCCESS
   :value: 0
.. data:: INTERRUPTED
   :value: 1

   Seems to represent return codes of some function somewhere.  Success code
   is imported in various places.  ???

.. data:: STALLED
   :value: 2

   Not obviously used anywhere.  May belong to the previous group?  ???

.. data:: NO_STATUS
   :value: -1

   Imported by various methods submodules in the `commands` module.  ???

.. data:: DATA_DIR
   :value: /data
.. data:: LINEGRAPH_DIR
   :value: /data/linegraph
.. data:: LOCAL_NAME
   :value: /local_name.txt

   Important things in the local filesystem.  ???

Sounds Class
------------

.. class:: Sounds(???)

   ???

   **Constants**

   Looks like filesystem locations of sounds associated with certain system
   operations.

   .. data:: NAVIGATION
      :value: sounds/menu_click

      ???

   .. data:: NAVIGATION_FAST
      :value: sounds/menu_fastback

      ???

   .. data:: STARTUP
      :value: sounds/startup

      ???

   .. data:: SHUTDOWN
      :value: sounds/menu_shutdown

      ???

   .. data:: PROGRAM_STOP
      :value: sounds/menu_program_stop

      ???

   .. data:: PROGRAM_START
      :value: sounds/menu_program_start

      ???

Image Class
-----------

.. class:: Image(???)

   ???  I'm not quite clear whether this class principally lives here or in
   `hub`...

   **Methods**

   .. method:: width(???)

      ???

   .. method:: height(???)

      ???

   .. method:: get_pixel(???)

      ???

   .. method:: set_pixel(???)

      ???

   .. method:: shift_left(???)

      ???

   .. method:: shift_right(???)

      ???

   .. method:: shift_up(???)

      ???

   .. method:: shift_down(???)

      ???

   **Constants**

   .. data:: HEART
      :value: Image('09090:99999:99999:09990:00900:')
   .. data:: HEART_SMALL
      :value: Image('00000:09090:09990:00900:00000:')
   .. data:: HAPPY
      :value: Image('00000:09090:00000:90009:09990:')
   .. data:: SMILE
      :value: Image('00000:00000:00000:90009:09990:')
   .. data:: SAD
      :value: Image('00000:09090:00000:09990:90009:')
   .. data:: CONFUSED
      :value: Image('00000:09090:00000:09090:90909:')
   .. data:: ANGRY
      :value: Image('90009:09090:00000:99999:90909:')
   .. data:: ASLEEP
      :value: Image('00000:99099:00000:09990:00000:')
   .. data:: SURPRISED
      :value: Image('09090:00000:00900:09090:00900:')
   .. data:: SILLY
      :value: Image('90009:00000:99999:00909:00999:')
   .. data:: FABULOUS
      :value: Image('99999:99099:00000:09090:09990:')
   .. data:: MEH
      :value: Image('09090:00000:00090:00900:09000:')
   .. data:: YES
      :value: Image('00000:00009:00090:90900:09000:')
   .. data:: NO
      :value: Image('90009:09090:00900:09090:90009:')
   .. data:: CLOCK12
      :value: Image('00900:00900:00900:00000:00000:')
   .. data:: CLOCK1
      :value: Image('00090:00090:00900:00000:00000:')
   .. data:: CLOCK2
      :value: Image('00000:00099:00900:00000:00000:')
   .. data:: CLOCK3
      :value: Image('00000:00000:00999:00000:00000:')
   .. data:: CLOCK4
      :value: Image('00000:00000:00900:00099:00000:')
   .. data:: CLOCK5
      :value: Image('00000:00000:00900:00090:00090:')
   .. data:: CLOCK6
      :value: Image('00000:00000:00900:00900:00900:')
   .. data:: CLOCK7
      :value: Image('00000:00000:00900:09000:09000:')
   .. data:: CLOCK8
      :value: Image('00000:00000:00900:99000:00000:')
   .. data:: CLOCK9
      :value: Image('00000:00000:99900:00000:00000:')
   .. data:: CLOCK10
      :value: Image('00000:99000:00900:00000:00000:')
   .. data:: CLOCK11
      :value: Image('09000:09000:00900:00000:00000:')
   .. data:: ARROW_N
      :value: Image('00900:09990:90909:00900:00900:')
   .. data:: ARROW_NE
      :value: Image('00999:00099:00909:09000:90000:')
   .. data:: ARROW_E
      :value: Image('00900:00090:99999:00090:00900:')
   .. data:: ARROW_SE
      :value: Image('90000:09000:00909:00099:00999:')
   .. data:: ARROW_S
      :value: Image('00900:00900:90909:09990:00900:')
   .. data:: ARROW_SW
      :value: Image('00009:00090:90900:99000:99900:')
   .. data:: ARROW_W
      :value: Image('00900:09000:99999:09000:00900:')
   .. data:: ARROW_NW
      :value: Image('99900:99000:90900:00090:00009:')
   .. data:: GO_RIGHT
      :value: Image('09000:09900:09990:09900:09000:')
   .. data:: GO_LEFT
      :value: Image('00090:00990:09990:00990:00090:')
   .. data:: GO_UP
      :value: Image('00000:00900:09990:99999:00000:')
   .. data:: GO_DOWN
      :value: Image('00000:99999:09990:00900:00000:')
   .. data:: TRIANGLE
      :value: Image('00000:00900:09090:99999:00000:')
   .. data:: TRIANGLE_LEFT
      :value: Image('90000:99000:90900:90090:99999:')
   .. data:: CHESSBOARD
      :value: Image('09090:90909:09090:90909:09090:')
   .. data:: DIAMOND
      :value: Image('00900:09090:90009:09090:00900:')
   .. data:: DIAMOND_SMALL
      :value: Image('00000:00900:09090:00900:00000:')
   .. data:: SQUARE
      :value: Image('99999:90009:90009:90009:99999:')
   .. data:: SQUARE_SMALL
      :value: Image('00000:09990:09090:09990:00000:')
   .. data:: RABBIT
      :value: Image('90900:90900:99990:99090:99990:')
   .. data:: COW
      :value: Image('90009:90009:99999:09990:00900:')
   .. data:: MUSIC_CROTCHET
      :value: Image('00900:00900:00900:99900:99900:')
   .. data:: MUSIC_QUAVER
      :value: Image('00900:00990:00909:99900:99900:')
   .. data:: MUSIC_QUAVERS
      :value: Image('09999:09009:09009:99099:99099:')
   .. data:: PITCHFORK
      :value: Image('90909:90909:99999:00900:00900:')
   .. data:: XMAS
      :value: Image('00900:09990:00900:09990:99999:')
   .. data:: PACMAN
      :value: Image('09999:99090:99900:99990:09999:')
   .. data:: TARGET
      :value: Image('00900:09990:99099:09990:00900:')
   .. data:: TSHIRT
      :value: Image('99099:99999:09990:09990:09990:')
   .. data:: ROLLERSKATE
      :value: Image('00099:00099:99999:99999:09090:')
   .. data:: DUCK
      :value: Image('09900:99900:09999:09990:00000:')
   .. data:: HOUSE
      :value: Image('00900:09990:99999:09990:09090:')
   .. data:: TORTOISE
      :value: Image('00000:09990:99999:09090:00000:')
   .. data:: BUTTERFLY
      :value: Image('99099:99999:00900:99999:99099:')
   .. data:: STICKFIGURE
      :value: Image('00900:99999:00900:09090:90009:')
   .. data:: GHOST
      :value: Image('99999:90909:99999:99999:90909:')
   .. data:: SWORD
      :value: Image('00900:00900:00900:09990:00900:')
   .. data:: GIRAFFE
      :value: Image('99000:09000:09000:09990:09090:')
   .. data:: SKULL
      :value: Image('09990:90909:99999:09990:09990:')
   .. data:: UMBRELLA
      :value: Image('09990:99999:00900:90900:09900:')
   .. data:: SNAKE
      :value: Image('99000:99099:09090:09990:00000:')

      These are all Image objects containing the pictures suggested by their
      names.

   .. data:: ALL_CLOCKS
      :value: (Image('00900:00900:00900:00000:00000:'), Image('00090:00090:00900:00000:00000:'), Image('00000:00099:00900:00000:00000:'), Image('00000:00000:00999:00000:00000:'), Image('00000:00000:00900:00099:00000:'), Image('00000:00000:00900:00090:00090:'), Image('00000:00000:00900:00900:00900:'), Image('00000:00000:00900:09000:09000:'), Image('00000:00000:00900:99000:00000:'), Image('00000:00000:99900:00000:00000:'), Image('00000:99000:00900:00000:00000:'), Image('09000:09000:00900:00000:00000:'))
   .. data:: ALL_ARROWS
      :value: (Image('00900:09990:90909:00900:00900:'), Image('00999:00099:00909:09000:90000:'), Image('00900:00090:99999:00090:00900:'), Image('90000:09000:00909:00099:00999:'), Image('00900:00900:90909:09990:00900:'), Image('00009:00090:90900:99000:99900:'), Image('00900:09000:99999:09000:00900:'), Image('99900:99000:90900:00090:00009:'))

      A couple of tuples of sets of images you might want to iterate though.

Imports
-------
* Module `hub`
* Function `micropython.const`
