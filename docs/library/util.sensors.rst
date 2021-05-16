:mod:`util.sensors` -- sensors utility module
==============================================

.. module:: util.sensors
   :synopsis: sensors utility module

???

Functions
---------

.. function:: register_ports(???)

   ???

.. function:: is_type(???)

   ???

.. function:: _is_motor(???)

   ???

.. function:: _type_change_handler(???)

   ???

.. function:: get_sensor_value(???)

   ???

.. function:: update_sensor_data(???)

   ???

.. function:: update_battery_status(???)

   ???

.. function:: reset_to_default_mode(???)

   ???

.. function:: set_display_sync(???)

   ???

.. function:: current_motion(???)

   ???

Variables
---------

.. data:: battery_status

   ???  Observed value: [8.36, 100, True]

.. data:: sensor_data

   ???  Observed value: [[0, ()], [0, ()], [0, ()], [0, ()], [0, ()], [0, ()], (0, -805, 585), (3, 3, 0), (-3, 0, 54), '', 0]

Constants
---------

.. data:: _PORTS
   :value: [Port(A), Port(B), Port(C), Port(D), Port(E), Port(F)]

   List of the six port objects of the six ports on the Hub.  See `hub.Port`.

.. data:: _REVERSE_MODES
   :value: {48: [3, 0, 1, 2], 65: [3, 0, 1, 2], 49: [3, 0, 1, 2], 75: [3, 0, 1, 2], 76: [3, 0, 1, 2], 61: [1, 0, 2, 3, 4], 62: [0], 63: [0, 1, -1, -1, 2]}

   ???

.. data:: _EVENT_MODE
   :value: [[], [], [], [], [], []]

   ???

.. data:: _PORT_INDEX_MAP
   :value: ['A', 'B', 'C', 'D', 'E', 'F', 'ACCELEROMETER', 'GYROSCOPE', 'POSITION', 'ORIENTATION', 'TIMER']

   ???

.. data:: _PORT_TYPE
   :value: [0, 0, 0, 0, 0, 0]

   ???

.. data:: _NO_DATA
   :value: ()

   ???

.. data:: _SYNC_DISPLAY
   :value: False

   ???

.. data:: _DEFAULT_MODE
   :value: {48: [(1, 0), (2, 2), (3, 1), (0, 0)], 65: [(1, 0), (2, 2), (3, 1), (1, 0)], 49: [(1, 0), (2, 2), (3, 1), (0, 0)], 75: [(1, 0), (2, 2), (3, 1), (0, 0)], 76: [(1, 0), (2, 2), (3, 1), (0, 0)], 61: [(1, 0), (0, 0), (5, 0), (5, 1), (5, 2)], 62: [(0, 0)], 63: [(0, 0), (1, 0), (4, 0)]}

   ???

.. data:: _MOTOR_TYPES
   :value: [65, 48, 49, 75, 76]

   List of the LPF2 type IDs that correspond to motors.

Imports
-------
* Module `hub`
* Function `micropython.const`
* Function `util.scratch.orientation_to_number`
* Function `util.time.get_time`
* Constant `util.constants.LPF2_FLIPPER_MOTOR_MEDIUM` = 48
* Constant `util.constants.LPF2_FLIPPER_MOTOR_LARGE` = 49
* Constant `util.constants.LPF2_FLIPPER_COLOR` = 61
* Constant `util.constants.LPF2_FLIPPER_DISTANCE` = 62
* Constant `util.constants.LPF2_FLIPPER_FORCE` = 63
* Constant `util.constants.LPF2_FLIPPER_MOTOR_SMALL` = 65
* Constant `util.constants.LPF2_STONE_GREY_MOTOR_MEDIUM` = 75
* Constant `util.constants.LPF2_STONE_GREY_MOTOR_LARGE` = 76
