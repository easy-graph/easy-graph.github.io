Example of Hypergraph
========

This part offers three examples on how to do hypergraph analysis with **EasyGraph**.

Basic Properties and Operation of Hypergraph
-------------------------
>>> import torch
>>> import easygraph as eg
>>> # Create a hypergraph with three nodes and zero hyperedge.
>>> hg = eg.Hypergraph(5, [(0, 1, 2), (2, 3), (0, 4)])
>>> # Calculate five shs(Structural Hole Spanners) in G
>>> hg.e[0]
([(0, 1, 2), (2, 3), (0, 4)], [1.0, 1.0, 1.0])
>>> # print the incidence matrix of the hypergraph
>>> hg.H.to_dense()
>>> # Draw hypergraph with label of each vertex.
>>> hg.draw(v_label = [0,1,2,3,4])

.. image:: hypergraph1.png


Add hyperedges and you can find the weight of the last hyperedge is 1.0 and 2.0, if you set the merge_op to mean and sum, respectively.

>>> hg = dhg.Hypergraph(5, [(0, 1, 2), (2, 3), (2, 3), (0, 4)], merge_op="mean")
>>> hg.e
([(0, 1, 2), (2, 3), (0, 4)], [1.0, 1.0, 1.0])
>>> hg = dhg.Hypergraph(5, [(0, 1, 2), (2, 3), (2, 3), (0, 4)], merge_op="sum")
>>> hg.e
([(0, 1, 2), (2, 3), (0, 4)], [1.0, 2.0, 1.0])
>>> hg.add_hyperedges([(0, 2, 1), (0, 4)], merge_op="mean")
>>> hg.e
([(0, 1, 2), (2, 3), (0, 4)], [1.0, 2.0, 1.0])
>>> hg.add_hyperedges([(0, 2, 1), (0, 4)], merge_op="sum")
>>> hg.e
([(0, 1, 2), (2, 3), (0, 4)], [2.0, 2.0, 2.0])


Use the eg.Hypergraph.from_feature_kNN() function to construct a hypergraph based on the k-nearest neighbors of the features

>>> X = torch.tensor([[0.0658, 0.3191, 0.0204, 0.6955],
                      [0.1144, 0.7131, 0.3643, 0.4707],
                      [0.2250, 0.0620, 0.0379, 0.2848],
                      [0.0619, 0.4898, 0.9368, 0.7433],
                      [0.5380, 0.3119, 0.6462, 0.4311],
                      [0.2514, 0.9237, 0.8502, 0.7592],
                      [0.9482, 0.6812, 0.0503, 0.4596],
                      [0.2652, 0.3859, 0.8645, 0.7619],
                      [0.4683, 0.8260, 0.9798, 0.2933],
                      [0.6308, 0.1469, 0.0304, 0.2073]])
>>> hg = eg.Hypergraph.from_feature_kNN(X, k=3)
>>> hg
Hypergraph(num_v=10, num_e=9)
>>> hg.e
([(0, 1, 2), (0, 1, 5), (0, 2, 9), (3, 5, 7), (4, 7, 8), (4, 6, 9), (3, 4, 7), (4, 5, 8), (2, 6, 9)], [1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0, 1.0])
>>> hg.H.to_dense()
tensor([[1., 1., 1., 0., 0., 0., 0., 0., 0.],
        [1., 1., 0., 0., 0., 0., 0., 0., 0.],
        [1., 0., 1., 0., 0., 0., 0., 0., 1.],
        [0., 0., 0., 1., 0., 0., 1., 0., 0.],
        [0., 0., 0., 0., 1., 1., 1., 1., 0.],
        [0., 1., 0., 1., 0., 0., 0., 1., 0.],
        [0., 0., 0., 0., 0., 1., 0., 0., 1.],
        [0., 0., 0., 1., 1., 0., 1., 0., 0.],
        [0., 0., 0., 0., 1., 0., 0., 1., 0.],
        [0., 0., 1., 0., 0., 1., 0., 0., 1.]])
>>> hg.draw(v_label=list(range(0,10)))

.. image:: hypergraph2.png

Construct a hypergraph from a graph using the eg.Hypergraph.from_graph() function

>>> g = eg.Graph()
>>> g.add_edges([(0, 1), (1, 2), (2, 3), (1, 4)])
>>> hg = eg.Hypergraph.from_graph(g)
>>> hg.e
([(0, 1), (1, 2), (1, 4), (2, 3)], [1.0, 1.0, 1.0, 1.0])
>>> hg.H.to_dense()
tensor([[1., 0., 0., 0.],
        [1., 1., 1., 0.],
        [0., 1., 0., 1.],
        [0., 0., 0., 1.],
        [0., 0., 1., 0.]])
