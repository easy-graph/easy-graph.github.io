---
layout: post
title:  "EasyGraph Usage Notes: Computation of Classic Structural Hole Indicators"
date:   2023-10-19 10:18:43 +0800
categories: jekyll update
---
## Introduction：
EasyGraph is an open-source toolbox for network analysis based on the Python language, developed by DataNet team at Fudan University. It is the first open-source library that includes a comprehensive set of methods for detecting structural hole spanners, while also covering network embedding and various traditional network analysis techniques. EasyGraph supports multiple types of network data with excellent compatibility. Additionally, it leverages hybrid programming and parallel computing to enhance the efficiency of most classic network analysis algorithms.



This article will introduce the process of measuring classic indicators of structural holes, such as effective size, efficiency, constraint, and hierarchy through EasyGraph.

[EasyGraph source code](https://github.com/easy-graph/Easy-Graph)

install:```pip install Python-EasyGraph```

## effective size

[source code](https://github.com/easy-graph/Easy-Graph/blob/60f1152bb195d0bbe4fa39e4e8f24f861bbc7146/easygraph/functions/structural_holes/evaluation.py#L85)

A node’s ego network(the one-hop network of a central node) has redundancy to the extent that its contacts are connected to each other. The effective size of a node is an indicator to measure the nonredundant
connections of a node.

![img](https://cdn-images-1.medium.com/max/800/1*YWG2j4f22wmdchKCVrwD_g.png)

 p(u,w) is the normalized mutual weight of the (directed or undirected) edges
joining u and w, while m(v,w) is calculated by dividing the normalized mutual weight between v and w by the maximal normalized mutual weight between v and its neighbors.

```javascript
from easygraph.datasets import get_graph_karateclub
import easygraph as eg
G = get_graph_karateclub()
```
```javascript
sz=effective_size(G)
for node,val in sz.items():
	print(node,val)
```
## efficiency

[source code](https://github.com/easy-graph/Easy-Graph/blob/60f1152bb195d0bbe4fa39e4e8f24f861bbc7146/easygraph/functions/structural_holes/evaluation.py#L176)

Efficiency is calculated by dividing a node's effective size by its degree, measuring the nonredundant connections of a node in a normalized manner.

```javascript
ef=efficiency(G)
for node,val in ef.items():
	print(node,val)
```
## constraint

Constraint is a measure of the extent to which a node is constrained within the ego network. A node with higher constraint implies higher network density and a lower number of structural holes in its neighborhood.

![img](https://cdn-images-1.medium.com/max/800/1*2cjGh62aKoRIphR2wQiClQ.png)

The constraint of a node is the sum of its local_constraints with all neighboring nodes.

[source code](https://github.com/easy-graph/Easy-Graph/blob/60f1152bb195d0bbe4fa39e4e8f24f861bbc7146/easygraph/functions/structural_holes/evaluation.py#L220)

![img](https://cdn-images-1.medium.com/max/800/1*IViRt1b0AhdCO8IrXMMQWA.png)

```javascript
cons=constraint(G)
for node,val in cons.items():
	print(node,val)
```
## hierarchy

Hierarchy is an indicator that measures the extent to which the aggregate constraint on ego is concentrated in a single contact. while h(i) that equals 1.0 indicates that all the constraint is concentrated in a single contact.

[source code](https://github.com/easy-graph/Easy-Graph/blob/8f85a16ae374a8bddf70567321337dab603a65b9/easygraph/functions/structural_holes/evaluation.py#L337)

```javascript
hier=hierarchy(G)
for node,val in hier.items():
	print(node,val)
```
Effective size, constraint, and hierarchy, these three indicators all imply the presence of structural holes. Below is an example using the Karate Club dataset.

![img](https://cdn-images-1.medium.com/max/800/0*n6olVLNYSH48Ti5x.png)

In this image, the red color indicates the top 5 nodes with the maximum effective size, the yellow color marks the 5 nodes with the minimum constraint, and the blue color represents the 5 nodes with the minimum hierarchy.

 It can be observed that four out of the top 5 nodes with the maximum effective size overlap with the minimum constraint nodes, highlighting a strong association between these classic indicators and structural holes, providing direction for maximizing information dissemination.