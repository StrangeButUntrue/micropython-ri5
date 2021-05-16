:mod:`util.storage` -- storage utility module
=============================================

.. module:: util.storage
   :synopsis: storage utility module

???

Functions
---------

.. function:: get_path(???)

   ???

.. function:: get_storage_information(???)

   ???

.. function:: generate_project_id(???)

   ???

.. function:: read_local_name(???)

   ???

.. function:: write_local_name(???)

   ???

.. function:: _ensure_folder_exists(???)

   ???

.. function:: _get_metadata(???)

   ???

.. function:: _set_metadata(???)

   ???

.. function:: get_used_slots(???)

   ???

.. function:: clear_slot(???)

   ???

.. function:: move_slot(???)

   ???

.. function:: _move_slot_lookup(???)

   ???

.. function:: _file_to_slotid(???)

   ???

.. function:: get_program_type(???)

   ???

.. function:: get_program_project_id(???)

   ???

.. function:: open_program(???)

   ???

.. function:: read_program(???)

   ???

.. function:: close_program(???)

   ???

.. function:: set_force_reset(???)

   ???

.. function:: pop_force_reset(???)

   ???

Constants
---------

.. data:: _BT_PREFIX
   :value: LEGO Hub@

   ???

.. data:: __FORCE_RESET_PATH__
   :value: ./reset

   ???

.. data:: __STORAGE_PATH__
   :value: ./projects

   ???

.. data:: __META_PATH__
   :value: ./projects/.slots

   ???

.. data:: __PROGRAM_PATH__
   :value: ./projects/{0}

   ???

.. data:: __PROGRAM_PATH_EXT__
   :value: ./projects/{0}.py

   ???

.. data:: PROGRAM_TYPE_PYTHON
   :value: python

   ???

.. data:: PROGRAM_TYPE_SCRATCH
   :value: scratch

   ???

Imports
-------
* Module `uos`
* Module `urandom`
* Module `ure`
* Constant `uerrno.ENOENT` = 2
* Constant `uerrno.EEXIST` = 17
* Constant `util.constants.LOCAL_NAME` = /local_name.txt
