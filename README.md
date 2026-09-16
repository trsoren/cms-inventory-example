# CMS inventory calculation example

This repository provides a short, self-contained example of how interval-level
outputs from a continuous methane monitoring system can be converted into
source- and site-level emissions inventories with uncertainty.

The notebook starts from the basic outputs expected from a CMS inference
method:

- emission-rate estimates for intervals with sufficient information;
- associated variance estimates;
- identification of information/no-information intervals.

Using two synthetic sources, it demonstrates mean imputation for
no-information intervals, the working inventory variance formula, construction
of 95% uncertainty intervals, and aggregation from source to site totals.
Exact-zero estimates are retained as information intervals.

The example does not run a methane inversion model, use proprietary data, tune
an uncertainty adjustment, or evaluate confidence-interval coverage. Its
purpose is simply to provide an accessible implementation of the inventory
calculation described in:

*Enabling Facility-Level Methane Emissions Reporting with Continuous
Monitoring Systems.* [doi pending]

## Running the example

Open [`cms_inventory_example.ipynb`](cms_inventory_example.ipynb) in Jupyter
Notebook, JupyterLab, or Google Colab and run all cells. The example uses
NumPy, pandas, and Matplotlib.

The editable parameters near the top of the notebook can be used to explore
different emission characteristics and information fractions while retaining
the same synthetic reporting period.
