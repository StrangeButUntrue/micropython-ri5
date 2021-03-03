:mod:`uhashlib` -- hashing algorithms
=====================================

.. module:: uhashlib
   :synopsis: hashing algorithms

|see_cpython_module| :mod:`python:hashlib`.

This module implements binary data hashing algorithms. The exact inventory
of available algorithms depends on a board. RI5 implements:

* SHA256 - The current generation, modern hashing algorithm (of SHA2 series).
  It is suitable for cryptographically-secure purposes.

Constructors
------------

.. class:: uhashlib.sha256([data])

    Create an SHA256 hasher object and optionally feed ``data`` into it.

.. admonition:: Difference for RI5
   :class: attention

   Classes sha1 and md5 from the base MicroPython version are not implemented
   on the RI5.


Methods
-------

.. method:: hash.update(data)

   Feed more binary data into hash.

.. method:: hash.digest()

   Return hash for all data passed through hash, as a bytes object. After this
   method is called, more data cannot be fed into the hash any longer.

.. method:: hash.hexdigest()

   This method is NOT implemented. Use ``ubinascii.hexlify(hash.digest())``
   to achieve a similar effect.
