Grid Optimized Operation Dispatch (GOOD)
=========================================

.. image:: https://img.shields.io/badge/status-development-orange
    :alt: Project Status

This is a Python-based power grid optimization framework for modeling energy systems with renewable integration and policy constraints.

You're encouraged to use this documentation to get inspiration, explore configurations, and understand the structure and operation of the GOOD model.

📚 `src/ <https://github.com/ucdavis/good_model/tree/main/src/>`_
    Core source code and optimization framework. This includes handling of network structures, assets, and policy implementations.

📚 `Data/ <https://github.com/ucdavis/good_model/tree/main/Data/>`_
    Contains input data files for the model, including network configurations and parameters.

⚙️ `config.py <https://github.com/ucdavis/good_model/blob/main/config.py>`_
    Customize regions, time windows, input/output paths, and debugging settings.

⚙️ `requirements.txt <https://github.com/ucdavis/good_model/blob/main/requirements.txt>`_
    Lists Python dependencies required to run the GOOD model.

🔧 `run_network.py <https://github.com/ucdavis/good_model/blob/main/run_network.py>`_
    Main executable script to run the grid optimization process.

✅ `tests/ <https://github.com/ucdavis/good_model/tree/main/tests/>`_
    Test suite for verifying feasibility, edge cases, and optimization logic. Uses `pytest` for structured testing.

🔢 Versioning
    Project versioning follows standard Git tagging. Check releases and tags directly on GitHub.

📜 `README.rst <https://github.com/ucdavis/good_model/blob/main/README.rst>`_
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
    INPUT_GRAPH_PATH = 'Data/Default/US/graph.json'

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
