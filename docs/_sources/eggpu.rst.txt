EGGPU
========

Overview
+++++++++++++

EGGPU is a GPU-accelerated network analysis library that supports essential functions such as betweenness centrality, k-core centrality, and single-source shortest path. Built on top of the **EasyGraph** library, EGGPU delivers a user-friendly Python API while achieving remarkable speedups for large-scale network analysis.

EGGPU is engineered with a three-layer architecture:
- User Interface Layer: Developed in Python, this layer offers intuitive and easy-to-use APIs for end users.
- Middleware Layer: Constructed in C++, this layer shares memory space with the Computation Layer and serves as the binding agent. It also provides a graph container responsible for graph loading, storage, and format conversion.
- Computation Layer: Implemented in CUDA C/C++, this layer primarily executes the GPU-based network analysis functions, including betweenness centrality, k-core centrality, and SSSP.
.. image:: eggpu_architecture.png

Installation
+++++++++++++

On Linux
--------

.. code-block:: bash

   git clone --recursive https://github.com/easy-graph/Easy-Graph
   export EASYGRAPH_ENABLE_GPU="TRUE"
   pip install ./Easy-Graph

On Windows
----------

.. code-block:: none

   % For Windows users who want to enable GPU-based functions,
   % you must execute the commands below in cmd but not PowerShell.
   git clone --recursive https://github.com/easy-graph/Easy-Graph
   set EASYGRAPH_ENABLE_GPU=TRUE
   pip install ./Easy-Graph
