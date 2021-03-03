:mod:`uerrno` -- system error codes
===================================

.. module:: uerrno
   :synopsis: system error codes

|see_cpython_module| :mod:`python:errno`.

This module provides access to symbolic error codes for `OSError` exception.
A particular inventory of codes depends on `MicroPython port`.

Constants
---------

.. data:: EEXIST, EAGAIN, etc.

    Error codes, based on ANSI C/POSIX standard. All error codes start with
    "E". As mentioned above, inventory of the codes depends on
    `MicroPython port`. Errors are usually accessible as ``exc.args[0]``
    where ``exc`` is an instance of `OSError`. Usage example::

        try:
            uos.mkdir("my_dir")
        except OSError as exc:
            if exc.args[0] == uerrno.EEXIST:
                print("Directory already exists")

.. data:: EPERM = 1

.. data:: ENOENT = 2

.. data:: EIO = 5

.. data:: EBADF = 9

.. data:: EAGAIN = 11

.. data:: ENOMEM = 12

.. data:: EACCES = 13

.. data:: EEXIST = 17

.. data:: ENODEV = 19

.. data:: EISDIR = 21

.. data:: EINVAL = 22

.. data:: EOPNOTSUPP = 95

.. data:: EADDRINUSE = 98

.. data:: ECONNABORTED = 103

.. data:: ECONNRESET = 104

.. data:: ENOBUFS = 105

.. data:: ENOTCONN = 107

.. data:: ETIMEDOUT = 110

.. data:: ECONNREFUSED = 111

.. data:: EHOSTUNREACH = 113

.. data:: EALREADY = 114

.. data:: EINPROGRESS = 115

.. data:: errorcode

    Dictionary mapping numeric error codes to strings with symbolic error
    code (see above)::

        >>> print(uerrno.errorcode[uerrno.EEXIST])
        EEXIST
