:mod:`_api` -- user API
=======================

.. module:: _api
   :synopsis: user API

This module contains most of the API functions that you're meant to call to
operate the system as a user.  The module itself is actually a backend to
modules `mindstorms` and `spike`, which are nearly identical and seem to exist
mainly in order to correctly brand the Hub in documentation (i.e. so that
Mindstorms docs can tell you to import mindstorms, and Spike Prime docs can
tell you to import spike).

One interesting note is that submodule ``large_technic_hub`` only seems to
appear in this module after you've imported either `mindstorms` or `spike`, so
it's probably better to just use one of those unless you have very odd
requirements.

All of the classes within the submodules (except LargeTechnicHub) are aliased
in the main namespace for convenience.

Submodules
----------

.. toctree::
   :maxdepth: 1

   _api.distancesensor.rst
   _api.forcesensor.rst
   _api.colorsensor.rst
   _api.motionsensor.rst
   _api.statuslight.rst
   _api.motor.rst
   _api.button.rst
   _api.motorpair.rst
   _api.lightmatrix.rst
   _api.util.rst
   _api.speaker.rst
   _api.app.rst
   _api.large_technic_hub.rst
