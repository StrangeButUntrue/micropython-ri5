:mod:`runtime` -- runtime module
================================

.. module:: runtime
   :synopsis: runtime module

Contains mainly stack and virtual machine details needed to run programs on the
hub.

Classes `runtime.stack.Stack`, `runtime.virtualmachine.VirtualMachine` and
`runtime.multimotor.MultiMotor` have shortcut aliases in the main namespace.

Submodules
----------

.. toctree::
   :maxdepth: 1

   runtime.dirty_dict.rst
   runtime.multimotor.rst
   runtime.stack.rst
   runtime.timer.rst
   runtime.virtualmachine.rst
   runtime.vm_store.rst
