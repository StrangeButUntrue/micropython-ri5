:mod:`protocol` -- RI5 communication protocol
=============================================

.. module:: protocol
   :synopsis: RI5 communication protocol

This module handles the communication protocol that the RI5 uses when talking
over USB/Bluetooth to a controller app.  The protocol uses a specific json
format.  The base module has three submodules, and aliases
protocol.rpc_protocol.RPCProtocol as protocol.RPCProtocol for convenience.

Submodules
----------

.. toctree::
   :maxdepth: 1

   protocol.notifications.rst
   protocol.rpc_protocol.rst
   protocol.ujsonrpc.rst
