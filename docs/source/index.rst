
Grid Optimized Operation Dispatch (GOOD)
=========================================

Welcome to the documentation for **GOOD** – Grid Optimized Operation Dispatch – a Python-based power grid optimization framework designed to model energy systems with renewable integration and policy constraints.

Whether you're exploring grid optimization, energy policy simulation, or sustainable power systems, this guide will help you get started with GOOD and adapt it for your project needs.

Overview
--------

- Python-based framework for grid modeling and dispatch optimization.
- Supports renewable integration and custom policy constraints.
- Modular code structure for assets, buses, policies, and networks.
- Includes test suite powered by ``pytest``.
- Designed to be flexible and extensible for academic and practical use cases.

Core Repository
~~~~~~~~~~~~~~~

Explore the GOOD model's core structure including asset definitions, network modeling, and policy implementations.

**GitHub:** https://github.com/ucdavis/good_model

Optimization Modules
~~~~~~~~~~~~~~~~~~~~

Includes ``assets``, ``buses``, ``edges``, ``policies``, and more.

Graph Utilities
~~~~~~~~~~~~~~~

Extend NetworkX for advanced graph manipulation and serialization.

Dependencies
~~~~~~~~~~~~

Python dependencies for running GOOD, managed via ``requirements.txt``.

Learn
-----

Quickstart
~~~~~~~~~~

Getting Started with GOOD::

    git clone <repository-url>
    cd good-model
    python -m venv venv
    source venv/bin/activate
    pip install -r requirements.txt

Clone the repo, set up a virtual environment, and install dependencies to begin modeling with GOOD.

Running the Model
-----------------

Configure and Optimize::

    # Edit config.py
    REGIONS = ['ERC_FRNT', 'ERC_PHDL', 'ERC_REST', 'ERC_WEST']
    START_HOUR = 0
    NUM_HOURS = 24
    INPUT_GRAPH_PATH = 'Examples/WEC.json'

    # Run the script
    python run_network.py

After running, results are saved to ``optimization_results.json`` and logs to ``optimization_output.log``.

Testing
-------

Run Tests with Pytest::

    # Run all tests
    pytest

    # Run a specific test
    pytest tests/test_feasibility.py

Adapting for Your Use
----------------------

Customize for Your Project:

1. Clone repo  
2. Edit ``config.py``  
3. Add new data under ``Data/``  
4. Validate with tests  
5. Extend as needed

Resources
---------

README
~~~~~~

Project-level overview and links to the model structure, usage, and contribution guidelines.

**Link:** https://github.com/ucdavis/good_model/blob/1.1.1/README.rst

Test Suite
~~~~~~~~~~

Automated tests for optimization logic and edge cases using ``pytest``.

**Link:** https://github.com/ucdavis/good_model/tree/1.1.1/tests/

Questions or Feedback?
----------------------

Please open an issue via GitHub if you have suggestions, bugs, or contributions:

**Issues:** https://github.com/ucdavis/good_model/issues

.. note::

   This project is under active development.

Contents
--------
.. toctree::
   :maxdepth: 2
   :caption: Contents:
   formulation
   usage
   api
