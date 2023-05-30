

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
