.. Copyright 2023 CMakePP
..
.. Licensed under the Apache License, Version 2.0 (the "License");
.. you may not use this file except in compliance with the License.
.. You may obtain a copy of the License at
..
.. http://www.apache.org/licenses/LICENSE-2.0
..
.. Unless required by applicable law or agreed to in writing, software
.. distributed under the License is distributed on an "AS IS" BASIS,
.. WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
.. See the License for the specific language governing permissions and
.. limitations under the License.

********************
Best CMake Practices
********************

Unit Testing
============

Use ``include(CTest)`` not ``enable_testing()``
-----------------------------------------------

CMake provides CTest for unit testing your project. While it is common to see:

.. code-block:: cmake

   enable_testing()
   add_subdirectory(tests)

(or something similar) in a project's top-level ``CMakeLists.txt`` file you are
actually supposed to do:

.. code-block:: cmake

   include(CTest)
   add_subdirectory(tests)

The ``CTest`` CMake module automatically invokes the ``enable_testing()``
command for you. Furthermore, it does it in an intelligent manner that allows
users of your library to disable unit testing if they don't want it (they simply
need to set ``BUILD_TESTING=OFF``).
