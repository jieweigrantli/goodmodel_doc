Grid Optimized Operation Dispatch (GOOD)
=========================================

.. image:: https://img.shields.io/badge/status-development-orange
    :alt: Project Status

This is a Python-based power grid optimization framework for modeling energy systems with renewable integration and policy constraints.

You're encouraged to use this documentation to get inspiration, explore configurations, and understand the structure and operation of the GOOD model.

📚 `good/ <https://github.com/ucdavis/good_model/tree/1.1.1/good/>`_
    Core source code and optimization framework. This includes handling of network structures, assets, and policy implementations.

📂 **Optimization Modules**

- 📍 `assets/`: Definitions of asset types (plants, storage, loads).
- 📍 `base/`: Base classes for regions and policies.
- 📍 `buses/`: Network bus modeling.
- 📍 `edges/`: Transmission lines and edge definitions.
- 📍 `policies/`: Renewable and other policy implementations.
- 📄 `network.py`: Core network optimization management.
- 📄 `exceptions.py`: Custom exception handling for optimization.

⚙️ `requirements.txt <https://github.com/ucdavis/good_model/tree/1.1.1/good/requirements.txt>`_
    Lists Python dependencies required to run the GOOD model.

📄 `utilities.py`: General utility functions for data handling, statistics, and JSON management.

📄 `graph.py`: Graph utilities extending NetworkX capabilities, including JSON handling, graph serialization/deserialization, subgraph and supergraph construction, and graph operation utilities.

📄 `__init__.py`: Initializes submodules for utilities, graph handling, and optimization framework components.

✅ `tests/ <https://github.com/ucdavis/good_model/tree/1.1.1/tests/>`_
    Test suite for verifying feasibility, edge cases, and optimization logic. Uses `pytest` for structured testing.

🔢 Versioning
    Project versioning follows standard Git tagging. Check releases and tags directly on GitHub.

📜 `README.rst <https://github.com/ucdavis/good_model/tree/1.1.1/README.rst>`_
    This README provides a brief overview and links to key resources.

⁉️ Questions / Comments
    For questions, suggestions, or comments, please open an issue on `GitHub Issues <https://github.com/ucdavis/good_model/issues>`_.


Getting Started
---------------

We recommend setting up the model in a local Python virtual environment:

.. code-block:: console

    git clone <repository-url>
    cd good-model
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    pip install -r requirements.txt


Running the Optimization
------------------------

Edit the `config.py` to define regions, optimization periods, and file paths:

.. code-block:: python

    REGIONS = ['ERC_FRNT', 'ERC_PHDL', 'ERC_REST', 'ERC_WEST']
    START_HOUR = 0
    NUM_HOURS = 24
    INPUT_GRAPH_PATH = 'Examples/WEC.json'

Run the optimization script:

.. code-block:: console

    python run_network.py

Results are saved to `optimization_results.json`, and logs are available in `optimization_output.log`.


Testing the Project
-------------------

Run all tests using `pytest`:

.. code-block:: console

    pytest

Run specific test files:

.. code-block:: console

    pytest tests/test_feasibility.py


Adapting GOOD for Your Project
------------------------------

If you're adapting this project for your specific use:

#. Clone or download the repository.
#. Adjust `config.py` according to your requirements.
#. Customize or add data files within the `Data/` directory.
#. Ensure all dependencies are listed in `requirements.txt`.
#. Run initial tests to ensure basic functionality.
#. Optionally, extend the provided tests to cover new functionality or data scenarios.
