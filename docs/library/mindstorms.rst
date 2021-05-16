:mod:`mindstorms` -- Mindstorms branding of the user API
========================================================

.. module:: mindstorms
   :synopsis: Mindstorms branding of the user API

This module seems to be purely designed as a frontend for the `_api` module,
so that Robot Inventor Mindstorms documentation can tell its users to import a
module with a related name.

See `_api` for the majority of submodules and classes, all of which can also
be called from the mindstorms module by using it as a synonym for "_api".

Classes
-------
.. class:: MSHub()

    The actual class appears to have no methods or functions of its own, but it
    seems to be a superclass of `_api.large_technic_hub.LargeTechnicHub` so
    inherits everything from there.

    The API expects most access to the central Technic Hub and its functions to
    use an instance of this class.
