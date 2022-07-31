Graph Classes
=============

EasyGraph provides four types of graph classes, `Graph`、 `DiGraph`、 `MultiGraph`、 `MultiDiGraph`.

Which graph class should I use?
===============================

+----------------+------------+--------------------+------------------------+
| Networkx Class | Type       | Self-loops allowed | Parallel edges allowed |
+================+============+====================+========================+
| Graph          | undirected | Yes                | No                     |
+----------------+------------+--------------------+------------------------+
| DiGraph        | directed   | Yes                | No                     |
+----------------+------------+--------------------+------------------------+
| MultiGraph     | undirected | Yes                | Yes                    |
+----------------+------------+--------------------+------------------------+
| MultiDiGraph   | directed   | Yes                | Yes                    |
+----------------+------------+--------------------+------------------------+

.. toctree::
    :maxdepth: 2
    :caption: Contents

    classes/graph.rst
    classes/digraph.rst
    classes/MultiDiGraph.rst
    classes/MultiGraph.rst
    
