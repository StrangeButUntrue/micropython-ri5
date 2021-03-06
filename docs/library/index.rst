.. _micropython_lib:

MicroPython libraries
=====================

.. warning::

   Important summary of this section

   * MicroPython implements a subset of Python functionality for each module.
   * To ease extensibility, MicroPython versions of standard Python modules
     usually have ``u`` ("micro") prefix.
   * Additions/deletions/modifications from the base Micropython version are
     indicated within the document.


This chapter describes modules (function and class libraries) which are built
into MicroPython. There are a few categories of such modules:

* Modules which implement a subset of standard Python functionality and are not
  intended to be extended by the user.
* Modules which implement a subset of Python functionality, with a provision
  for extension by the user (via Python code).
* Modules which implement MicroPython extensions to the Python standard libraries.
* Modules specific to this particular `MicroPython port` and thus not portable.

Note about the availability of the modules and their contents: This documentation
in general aspires to describe all modules and functions/classes which are
implemented in MicroPython project. However, MicroPython is highly configurable, and
each port to a particular board/embedded system makes available only a subset
of MicroPython libraries. For officially supported ports, there is an effort
to either filter out non-applicable items, or mark individual descriptions
with "Availability:" clauses describing which ports provide a given feature.

You are able to discover the available, built-in libraries that can be
imported by entering the following at the REPL::

    help('modules')

Beyond the built-in libraries described in this documentation, many more
modules from the Python standard library, as well as further MicroPython
extensions to it, can be found in `micropython-lib`.

Python standard libraries and micro-libraries
---------------------------------------------

The following standard Python libraries have been "micro-ified" to fit in with
the philosophy of MicroPython.  They provide the core functionality of that
module and are intended to be a drop-in replacement for the standard Python
library.  Some modules below use a standard Python name, but prefixed with "u",
e.g. ``ujson`` instead of ``json``. This is to signify that such a module is
micro-library, i.e. implements only a subset of CPython module functionality.
By naming them differently, a user has a choice to write a Python-level module
to extend functionality for better compatibility with CPython (indeed, this is
what done by the `micropython-lib` project mentioned above).

In the RI5 port, since it may be cumbersome to add Python-level
wrapper modules to achieve naming compatibility with CPython, micro-modules
are available both by their u-name, and also by their non-u-name.  The
non-u-name can be overridden by a file of that name in your library path (``sys.path``).
For example, ``import json`` will first search for a file ``json.py`` (or package
directory ``json``) and load that module if it is found.  If nothing is found,
it will fallback to loading the built-in ``ujson`` module.

.. toctree::
   :maxdepth: 1

   builtins.rst
   array.rst
   cmath.rst
   gc.rst
   math.rst
   sys.rst
   ubinascii.rst
   ucollections.rst
   uerrno.rst
   uhashlib.rst
   uheapq.rst
   uio.rst
   ujson.rst
   uos.rst
   ure.rst
   uselect.rst
   ustruct.rst
   utime.rst
   uzlib.rst

These libraries do exist in MicroPython, but aren't in the base docs.

.. toctree::
   :maxdepth: 1

   urandom.rst

MicroPython-specific libraries
------------------------------

Functionality specific to the MicroPython implementation is available in
the following libraries.

.. toctree::
   :maxdepth: 1

   machine.rst
   micropython.rst
   uctypes.rst

These libraries do exist in MicroPython, but aren't in the base docs.

.. toctree::
   :maxdepth: 1

   utimeq.rst
   _onewire.rst

MicroPython default libraries unavailable
-----------------------------------------

Some default MicroPython functionality is missing from the Hub:

* usocket

* ussl

* _thread

* btree

* framebuf

* network

* ucryptolib

And some undocumented MicroPython modules that aren't in RI5:

* bluetooth

* lwip

* uasyncio (but note that the RI5 does have the async keyword)

* uwebsocket

* webrepl

Libraries specific to the Technic Hub
-------------------------------------

The following libraries are specific to the Technic Hub and are built into its Micropython.

.. toctree::
  :maxdepth: 2

  hub.rst
  firmware.rst

The following libraries are specific to the Technic Hub and are found in its filesystem.

.. toctree::
  :maxdepth: 2

  _api.rst
  commands.rst
  event_loop.rst
  mindstorms.rst
  programrunner.rst
  protocol.rst
  runtime.rst
  spike.rst
  system.rst
  ui.rst
  util.rst
  hub_runtime.rst
  version.rst

File main.py is also found in the filesystem, but do not import it as it will
restart the hub and require a battery removal/reinsert to get the hub working
again!  You can technically "import" boot, projects, sounds, extra_files, but
by default they're empty of Python content so they do nothing.
