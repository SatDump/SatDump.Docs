Scripting
=========

SatDump supports Lua scripts that can automatically be triggered when a certain action has been performed.

.. warning::
   This module is **NOT** built by default.
   You need to compile SatDump yourself and specify the ``-DPLUGIN_SCRIPTING=ON`` CMake option.

Basics
------

Scripts are simple Lua scripts. They do not have any function that needs to be called, the file will be executed as a normal Lua file by a regular Lua interpreter.

For example, consider a script containing the following:

.. code-block:: Lua

   print("Hello world")

This will be evaluated as a regular Lua script and return ``Hello World`` to standard output.

.. note::
   ``print`` will always return to stdout. It is not currently possible to output in SatDump's logger.

Scripts need to be stored in SatDump's user script directory.

-  Linux: ``~/.config/satdump/scripts``
-  Windows: ``%appdata%\satdump\scripts``
-  MacOS: ``~/.config/satdump/scripts``

Scripts need to have a specific name in order to be called, which is detaied below.

pipeline_done_processing.lua
----------------------------

This script will be executed when the pipeline is done processing (i.e. when the satellite has been decoded and processed).

A typical use case is to archive the frame files such ``.cadu`` or ``.frm`` in a specific directory.

The Lua script supports these variables:

- ``pipeline_id``: the ID of the pipeline that has just finished procesing. See :doc:`pipelines` for a list.
- ``pipeline_output_directory``: the full path of the output directory where the pipeline's results have been saved.

.. note::
   For example, if you offline decoded Meteor-M N°2-3 into a directory called ``/home/user/MeteorM``, ``pipeline_id`` will output ``meteor_hrpt``  and ``pipeline_output_directory`` will output ``/home/user/MeteorM``.