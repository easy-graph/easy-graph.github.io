EGGPU
=====

Overview
+++++++++++++

EGGPU is a GPU-accelerated network analysis library that supports essential functions such as betweenness centrality, k-core centrality, and single-source shortest path. Built on top of the **EasyGraph** library, EGGPU delivers a user-friendly Python API while achieving remarkable speedups for large-scale network analysis.

EGGPU is engineered with a three-layer architecture:

* **User Interface Layer**: Developed in Python, this layer offers intuitive and easy-to-use APIs for end users.

* **Middleware Layer**: Constructed in C++, this layer shares memory space with the Computation Layer and serves as the binding agent. It also provides a graph container responsible for graph loading, storage, and format conversion.

* **Computation Layer**: Implemented in CUDA C/C++, this layer primarily executes the GPU-based network analysis functions, including betweenness centrality, k-core centrality, and SSSP.

.. image:: eggpu_architecture.png
   :align: center


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

Benchmarking and Performance Evaluation
+++++++++++++

Our experiments were conducted on a machine equipped with a 12th Gen Intel Core i9-12900K CPU (16 cores, 24 logical processors) and an NVIDIA GeForce RTX 4090 GPU (114 SMs, 1536 max threads per SM, GPU clock speed: 2520.0 MHz, memory clock speed: 10501.0 MHz). The CUDA-based implementations demonstrated **significant acceleration**, as shown in the benchmark results below.

.. list-table::
   :widths: 50 50
   :header-rows: 0

   * - .. image:: res_clusterings.png
          :align: center
     - .. image:: res_constraint.png
          :align: center



Examples
+++++++++++++

We provide a comprehensive guide to EGGPU's GPU-accelerated functions within the **EasyGraph** ecosystem, demonstrating both native NVCC compilation of CUDA kernels and seamless invocation via our Python API.


.. code-block:: python

   import easygraph as eg

   def add_weighted(G):
   G.add_edges(
   [(0,1),(0,2),(0,3),(1,2),(1,3),(1,5),(2,3),(2,4),(3,5),
   (5,6),(5,8),(6,7),(6,8),(7,8)],
   edges_attr=[
   {'weight': 1},{'weight': 3},{'weight': 2},{'weight': 1},
   {'weight': 2},{'weight': 4},{'weight': 2},{'weight': 1},
   {'weight': 2},{'weight': 1},{'weight': 2},{'weight': 4},
   {'weight': 3},{'weight': 3},
   ]
   )
   G_gpu = eg.GraphC()
   add_weighted(G_gpu)

   print(eg.constraint(G_gpu, weight="weight"))
   """
   [0.73650971 0.62929697 0.58577806 0.64878836 0.4685571  1.
   0.83901931 0.78530837 0.94929847]
   """
   print(eg.effective_size(G_gpu, weight="weight"))
   """
   [1.76388889 2.54166667 2.94047619 2.70833333 3.16666667 1.
   1.94791667 2.09375    1.10714286]
   """