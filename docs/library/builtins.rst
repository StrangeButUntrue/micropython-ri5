Builtin functions and exceptions
================================

All builtin functions and exceptions are described here. They are also
available via ``builtins`` module.

Functions and types
-------------------

.. function:: abs()

.. function:: all()

.. function:: any()

.. function:: bin()

.. class:: bool()

.. class:: bytearray()

   .. admonition:: Difference for RI5
      :class: attention

      As with the array class, in RI5 this has methods ``append()``, ``extend()``
      and ``decode()`` that isn't in standard Micropython.

.. class:: bytes()

    |see_cpython| `python:bytes`.

    It's missing a lot of the more complicated or specialized functions of that
    class though.

.. function:: callable()

.. function:: chr()

.. function:: classmethod()

.. function:: compile()

.. class:: complex()

.. function:: delattr(obj, name)

   The argument *name* should be a string, and this function deletes the named
   attribute from the object given by *obj*.

.. class:: dict()

.. function:: dir()

.. function:: divmod()

.. function:: enumerate()

.. function:: eval()

.. function:: exec()

.. function:: execfile()

   Not in Python 3, but it does show up in Micropython.

.. function:: filter()

.. class:: float()

   In MicroPython, this class doesn't have any methods.

.. class:: frozenset()

.. function:: getattr()

.. function:: globals()

.. function:: hasattr()

.. function:: hash()

.. function:: help()

.. function:: hex()

.. function:: id()

.. admonition:: Difference for RI5
   :class: attention

   The input() function has been removed in RI5 - not unreasonably!

.. class:: int()

   .. classmethod:: from_bytes(bytes, byteorder)

      In MicroPython, `byteorder` parameter must be positional (this is
      compatible with CPython).

   .. method:: to_bytes(size, byteorder)

      In MicroPython, `byteorder` parameter must be positional (this is
      compatible with CPython).

.. function:: isinstance()

.. function:: issubclass()

.. function:: iter()

.. function:: len()

.. class:: list()

.. function:: locals()

.. function:: map()

.. function:: max()

.. class:: memoryview()

   In MicroPython, this doesn't have any methods and can only be used with
   indices and slicing.

.. function:: min()

.. function:: next()

.. class:: object()

.. function:: oct()

.. function:: open(file, mode='r', buffering=-1, encoding=None)

   On RI5, this allows one to four arguments, so not as many as the corresponding
   CPython function.

.. function:: ord()

.. function:: pow()

.. function:: print()

.. class:: property()

.. function:: range()

.. function:: repr()

.. function:: reversed()

.. function:: round()

.. class:: set()

.. function:: setattr()

.. class:: slice()

   The *slice* builtin is the type that slice objects have.

.. function:: sorted()

.. function:: staticmethod()

.. class:: str()

    |see_cpython| `python:str`.

    It's missing a lot of the more complicated or specialized functions of that
    class though.

.. function:: sum()

.. function:: super()

.. class:: tuple()

.. class:: type()

.. function:: zip()


Exceptions
----------

.. exception:: BaseException

.. exception:: ArithmeticError

.. exception:: AssertionError

.. exception:: AttributeError

.. exception:: EOFError

.. exception:: Exception

.. exception:: GeneratorExit

.. exception:: ImportError

.. exception:: IndentationError

.. exception:: IndexError

.. exception:: KeyboardInterrupt

.. exception:: KeyError

.. exception:: LookupError

.. exception:: MemoryError

.. exception:: NameError

.. exception:: NotImplementedError

.. exception:: OSError

    |see_cpython| `python:OSError`. MicroPython doesn't implement ``errno``
    attribute, instead use the standard way to access exception arguments:
    ``exc.args[0]``.

.. exception:: OverflowError

.. exception:: RuntimeError

.. exception:: StopAsyncIteration

.. exception:: StopIteration

.. exception:: SyntaxError

.. exception:: SystemExit

    |see_cpython| `python:SystemExit`.

.. exception:: TypeError

    |see_cpython| `python:TypeError`.

.. exception:: UnicodeError

.. exception:: ValueError

.. exception:: ZeroDivisionError

Constants
---------

.. data:: Ellipsis

   The same as the ellipsis literal “...”. Special value used mostly in
   conjunction with extended slicing syntax for user-defined container data types.

.. data:: NotImplemented

   Special value which should be returned by the binary special methods (e.g.
   __eq__(), __lt__(), __add__(), __rsub__(), etc.) to indicate that the
   operation is not implemented with respect to the other type; may be returned
   by the in-place binary special methods (e.g. __imul__(), __iand__(), etc.)
   for the same purpose. It should not be evaluated in a boolean context.

   Note: When a binary (or in-place) method returns NotImplemented the
   interpreter will try the reflected operation on the other type (or some
   other fallback, depending on the operator). If all attempts return
   NotImplemented, the interpreter will raise an appropriate exception.
   Incorrectly returning NotImplemented will result in a misleading error
   message or the NotImplemented value being returned to Python code.

   See Implementing the arithmetic operations for examples.

   Note: NotImplementedError and NotImplemented are not interchangeable, even
   though they have similar names and purposes. See NotImplementedError for
   details on when to use it.