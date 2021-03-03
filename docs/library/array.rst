:mod:`array` -- arrays of numeric data
======================================

.. module:: array
   :synopsis: efficient arrays of numeric data

|see_cpython_module| :mod:`python:array`.

Supported format codes: ``b``, ``B``, ``h``, ``H``, ``i``, ``I``, ``l``,
``L``, ``q``, ``Q``, ``f``, ``d`` (the latter 2 depending on the
floating-point support).

Classes
-------

.. class:: array.array(typecode, [iterable])

    Create array with elements of given type. Initial contents of the
    array are given by *iterable*. If it is not provided, an empty
    array is created.

    .. method:: append(val)

        Append new element *val* to the end of array, growing it.

    .. method:: extend(iterable)

        Append new elements as contained in *iterable* to the end of
        array, growing it.

    .. method:: decode()

        Outputs a string of the decoded array.  Seems to treat each element
        as a byte and use ASCII encoding only?

        .. admonition:: Difference for RI5
           :class: attention

           This function is an extension from the base MicroPython version.