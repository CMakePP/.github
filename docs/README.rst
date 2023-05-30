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



Start a terminal at the root directory of the repository. It is recommended
to create a virtual environment before installing packages:

.. code-block:: bash

   python -m venv venv

Activate the virtual environment with:

On Unix and Linux-based systems:

.. code-block:: bash

   source venv/bin/activate

.. Windows makefile doesn't exist yet
.. On Windows systems:

.. .. code-block:: batch

..    .\venv\Scripts\activate

Install documentation dependencies with:

.. code-block:: bash

   pip install -r docs/requirements.txt

Build the documentation by navigating into the `docs` directory:

.. code-block:: bash

   cd docs

and building the HTML documentation:

.. code-block:: bash

   make html

The documentation can be viewed in a browser using Python's ``http.server``
module at (`http://localhost:8000`__) by running:

.. code-block:: bash

   python -m http.server --directory build/html
