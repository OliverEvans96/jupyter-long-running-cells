# Long-Running Notebook Tasks

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/OliverEvans96/jupyter-long-running-cells/HEAD?filepath=Long-Running%20Notebook%20Tasks.ipynb)

Assume that you're working on a notebook that contains
1. a long-running computation
2. a visualization.

You run the long computation, get the results, and plot the visualization.
You realize that your parameters weren't quite right, so you want to run the long computation again.
But you also want to tweak some aspects of the visualization while it's running.

Since a notebook can only execute one cell at a time, once you start the long-running computation, you won't be able to re-run the visualization cells to see your updates.

In this notebook, I'll demonstrate one way to address this issue using multi-threading and futures (a.k.a. promises).
