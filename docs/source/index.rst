---
orphan: true
---

<style>
/* Cards with links */
.sd-hide-link-text {
  height: 0;
}
</style>

# Grid Optimized Operation Dispatch (GOOD)

Welcome to the documentation for **GOOD** – Grid Optimized Operation Dispatch – a Python-based power grid optimization framework designed to model energy systems with renewable integration and policy constraints.

Whether you're exploring grid optimization, energy policy simulation, or sustainable power systems, this guide will help you get started with GOOD and adapt it for your project needs.

:::{rubric} Overview
:::
* Python-based framework for grid modeling and dispatch optimization.
* Supports renewable integration and custom policy constraints.
* Modular code structure for assets, buses, policies, and networks.
* Includes test suite powered by `pytest`.
* Designed to be flexible and extensible for academic and practical use cases.

::::::{grid} 1
:margin: 1
:padding: 2

:::{grid-item-card} {material-outlined}`bolt;1.7em` Core Repository
:link: https://github.com/ucdavis/good_model/tree/1.1.1/good/
:link-alt: GOOD Core Codebase
:padding: 2
:class-title: sd-fs-5

Explore the GOOD model's core structure including asset definitions, network modeling, and policy implementations.
+++
```{button-link} https://github.com/ucdavis/good_model
:color: primary
:expand:
**View on GitHub**
```
:::

::::::{grid-item}
:margin: 0
:padding: 2

::::{grid} 2
:margin: 0
:padding: 0

:::{grid-item-card} {material-outlined}`category;1.7em` Optimization Modules
:link: https://github.com/ucdavis/good_model/tree/1.1.1/good/
:link-alt: GOOD Modules Overview
:class-title: sd-fs-5

Includes `assets`, `buses`, `edges`, `policies`, and more.
:::

:::{grid-item-card} {material-outlined}`science;1.7em` Graph Utilities
:link: https://github.com/ucdavis/good_model/blob/1.1.1/good/graph.py
:link-alt: Graph Utilities
:class-title: sd-fs-5

Extend NetworkX for advanced graph manipulation and serialization.
:::

::::
:::::

:::{grid-item-card} {material-outlined}`build_circle;1.7em` Dependencies
:link: https://github.com/ucdavis/good_model/blob/1.1.1/good/requirements.txt
:link-alt: Requirements File
:padding: 2
:class-title: sd-fs-5

Python dependencies for running GOOD, managed via `requirements.txt`.
:::

::::::


## Learn

:::{rubric} Quickstart
:::

::::{card} Getting Started with GOOD
:class-title: sd-fs-4
:class-body: sd-text-center
:class-footer: sd-fs-6

+++
```console
git clone <repository-url>
cd good-model
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

:::{div} text-smaller
Clone the repo, set up a virtual environment, and install dependencies to begin modeling with GOOD.
:::
::::


:::{rubric} Running the Model
:::
::::{card} Configure and Optimize
:class-title: sd-fs-4
:class-body: sd-text-center
:class-footer: sd-fs-6

+++
Edit `config.py`:

```python
REGIONS = ['ERC_FRNT', 'ERC_PHDL', 'ERC_REST', 'ERC_WEST']
START_HOUR = 0
NUM_HOURS = 24
INPUT_GRAPH_PATH = 'Examples/WEC.json'
```

Run:

```console
python run_network.py
```

:::{div} text-smaller
After running, results are saved to `optimization_results.json` and logs to `optimization_output.log`.
:::
::::


:::{rubric} Testing
:::

::::{card} Run Tests with Pytest
:class-footer: text-smaller

Run all tests:

```console
pytest
```

Or a specific file:

```console
pytest tests/test_feasibility.py
```
::::


:::{rubric} Adapting for Your Use
:::

::::{grid} 1 1 2 2
:padding: 0

:::{grid-item-card}
:padding: 3
:class-header: sd-text-center sd-fs-5 sd-font-weight-bold sd-text-capitalize
:class-body: sd-text-center sd-fs-5
:class-footer: text-smaller
Customize for Your Project
^^^
{material-outlined}`construction;3.5em`
+++
1. Clone repo  
2. Edit `config.py`  
3. Add new data under `Data/`  
4. Validate with tests  
5. Extend as needed
:::
::::


## Resources

::::{grid} 2 3 3 3
:padding: 0

:::{grid-item-card} README
:link: https://github.com/ucdavis/good_model/blob/1.1.1/README.rst
:link-alt: Project README
:padding: 3
:class-card: sd-pt-3
:class-title: sd-fs-5
:class-body: sd-text-center
:class-footer: text-smaller
{material-outlined}`description;3.5em`
+++
Overview and links to the model structure, usage, and contribution guidelines.
:::

:::{grid-item-card} Test Suite
:link: https://github.com/ucdavis/good_model/tree/1.1.1/tests/
:link-alt: GOOD Test Suite
:padding: 3
:class-card: sd-pt-3
:class-title: sd-fs-5
:class-body: sd-text-center
:class-footer: text-smaller
{material-outlined}`bug_report;3.5em`
+++
Automated tests for optimization logic and edge cases using `pytest`.
:::

::::


:::{rubric} Questions or Feedback?
:::
Please open an issue via [GitHub Issues](https://github.com/ucdavis/good_model/issues) if you have suggestions, bugs, or contributions.

.. note::

   This project is under active development.

Contents
--------

.. toctree::
   :maxdepth: 2
   ../home/index
