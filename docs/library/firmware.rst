:mod:`firmware` -- Firmware information and loading
===================================================

.. module:: firmware
   :synopsis: access and control system firmware

.. warning::

   By definition, a lot of the functions in here are probably quite dangerous to
   run as they can rewrite firmware.  I haven't experimented with all of them
   so I can't even tell you which will cause system crashes, and which will be worse...
   Presumably this is the sort of thing you'll be wanting to run only if you want
   to load on a custom firmware.  If you're doing that, feel free to add details
   on the functions and the exact dangers of using them!

   See https://github.com/gpdaniels/spike-prime/issues/7 for some more (but
   currently still quite limited) details.

Functions
---------

.. function:: info()

   Returns a dictionary containing various details about the firmware.  For
   the version in this branch with no changes, it returns:

   {'appl_checksum': 1231192444, 'new_appl_image_stored_checksum': 0,
   'appl_calc_checksum': 1231192444, 'new_appl_valid': False,
   'new_appl_image_calc_checksum': 0, 'new_image_size': 0,
   'currently_stored_bytes': 0, 'upload_finished': True,
   'spi_flash_size': '32 MBytes', 'valid': 0}

.. function:: appl_checksum()

   Returns a checksum of the firmware.  For the version in this branch with no
   changes, that's 1231192444.

.. function:: appl_image_initialise(???params???)

   (Unknown - I wasn't confident I could run it safely.  I suspect this might
   potentially be quite dangerous, at least if you've stored something in
   the image store at any point beforehand.  Seems to take up to 1 positional
   argument.)

.. function:: appl_image_store(???params???)

   (Unknown - I wasn't confident I could run it safely.  Seems to take up to 1
   positional argument.)

.. function:: appl_image_read(start_pos?)

   Returns a bytearray - seems to return empty ones by default for all integer
   inputs.  My hypothesis is that you're supposed to store an image in here with
   the appl_image_store() function and then appl_image_initialise() it to start
   running with it, but is this the whole firmware or just some particular
   necessary part of it that's different to what you might write with flash_write()?

   I'm also hypothesising based on flash_read that the parameter is probably
   the byte to start reading at, and it returns empty bytearrays when there's
   no bytes stored to read.

.. function:: flash_read(start_pos)

   Returns a bytearray of 32 bytes of the flash memory, starting at the given
   byte.

.. function:: flash_write(???)

   (Unknown - I wasn't confident I could run it safely.  Some internet
   research suggests this is the particularly dangerous one, so maybe don't
   try this at home unless you've got the cash for another hub!  Seems to take
   2 positional arguments - perhaps position to write and data to write in
   some order?)

.. function:: ext_flash_read_length()

   Seems to crash the hub or at least make it unresponsive until after a battery
   pull or two.  Not sure what it was trying to do!

.. function:: ext_flash_erase()

   (Unknown - I wasn't confident I could run it safely.  Probably another
   quite dangerous one?)

.. function:: erase_superblock()

   (Unknown - I wasn't confident I could run it safely.  The link at the top says
   that this erases the filesystem from the hub.)

.. function:: bootloader_version()

   Returns a string specifying bootloader version.  For the version in this
   branch with no changes, that's 'v0.5.01.0002-f75d82d'.