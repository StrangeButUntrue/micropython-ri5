:mod:`urandom` -- random number generation
==========================================

.. module:: urandom
   :synopsis: random number generation

|see_cpython_module| :mod:`python:random

.. admonition:: Difference to CPython
   :class: attention

   The pseudorandom algorithm used in Micropython is the Yasmarang algorithm
   (<http://www.literatecode.com/yasmarang>), instead of the Mersenne Twister
   used in CPython.

This module allows generation of pseudo-random numbers, including setting of a
seed.  (These are probably not suitable for cryptographic purposes.)

On the RI5, the random generators do work without calling ``seed()``.  It's not
immediately clear what seed is used by the module in this case, but there's no
obvious repetition in outputs.  If you want an explicit seed whose value is
relatively difficult to predict, consider something like ``utime.ticks_cpu()``.

Functions
---------

.. function:: seed(a)

   Initialize the pseudorandom number generator with integer a.

.. function:: randrange(stop)

.. function:: randrange(start, stop[, step])

   Return a randomly selected element from range(stop) or range(start, stop, step).

.. function:: randint(a, b)

   Return a random integer N between a and b (inclusive).

.. function:: getrandbits(n)

   Return an integer with n random bits.

.. function:: choice(seq)

   Return a random element of the given sequence.

.. function:: random()

   Return a float between 0 and 1 (not including 1).

.. function:: uniform(a, b)

   Return a float between a and b (b may or may not be included depending on
   floating-point rounding).
