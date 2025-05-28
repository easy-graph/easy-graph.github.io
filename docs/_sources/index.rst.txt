.. test documentation master file, created by
   sphinx-quickstart on Thu Jul 30 15:49:04 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to EasyGraph !
====================================

.. image:: https://img.shields.io/pypi/v/Python-EasyGraph.svg?label=PyPI
  :target: https://pypi.org/project/Python-EasyGraph/

.. image:: https://img.shields.io/pypi/pyversions/Python-EasyGraph.svg?label=Python
   :target: https://pypi.org/project/Python-EasyGraph/

.. image:: https://img.shields.io/pypi/l/Python-EasyGraph?label=License
   :target: https://github.com/easy-graph/Easy-Graph/blob/master/LICENSE

.. image:: https://static.pepy.tech/personalized-badge/python-easygraph?period=total&units=international_system&left_color=brightgreen&right_color=yellowgreen&left_text=Downloads
   :target: https://pypi.org/project/Python-EasyGraph/

EasyGraph is an open source network analysis library. It is written in Python and supports analysis for undirected networks and directed networks. 
It covers advanced network analysis methods in structural hole spanners detection, network embedding and several classic methods (centrality calculation, 
connected component discovery and finding the shortest paths). 

EasyGraph integrates state-of-the-art network analysis approaches and implements them using Python. EasyGraph covers a series of advanced network analysis
algorithms include structural hole spanners detection (HIS, MaxD, Common_Greedy, AP_Greedy and HAM), and network representation learning 
(DeepWalk, Node2Vec, LINE and SDNE). Besides, for a number of general network analysis approaches, EasyGraph optimizes them and introduces 
parallel computing and Python/C++ hybrid programming techniques to achieve high efficiency. 

.. toctree::
   :maxdepth: 2
   :caption: Contents:

   install.rst
   example.rst
   hypergraph.rst
   eggpu.rst
   reference.rst
   tutorial.rst
   videos.rst
   contributorGuide.rst
   license.rst
   sourcecode.rst
   honors.rst
   dev.rst

..    :maxdepth: 1
..    egeps.rst
   aboutus.rst

.. toctree::
..    :titlesonly:

..    aboutus.rst


.. Indices and tables
.. ==================

.. * :ref:`genindex`
.. * :ref:`search`
