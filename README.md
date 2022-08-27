# Subgraph-Sampling-Toolbox
A subgraph sampling toolbox using PyG to practice graph partitioning for model train/validation/test split.

## Overview
Data splitting in Graph Neural Network (GNN) training has been a challenge in real-world applications because sometimes we cannot guarantee
that the test set will really be held out. Nodes are not independent and relationships can cross training and validation nodes.

Usually, a data split task in GNN training follows two types of settings:

**Transductive setting**
- The input graph can be observed in all the dataset splits (training, validation and test set). We only split the (node) labels.
  
**Inductive setting**
- We break the edges between splits to get multiple graphs. Now we have training, validation and test graphs that are independent.

## Benchmarking

We use the OGBN-products dataset to compare multiple graph partition methods for data split.

### Vertext Partitioning or Edge-Cut Partitioning

**1. OGBN-products**

Dataset splitting with OGBN-products is designed to use the sales ranking (popularity) to split nodes into training/validation/test sets.

*"Specifically, we sort the products according to their sales ranking and use the top 8% for training, next top 2% for validation, and the rest for testing. This is a more challenging splitting procedure that closely matches the real-world application where labels are first assigned to important nodes in the network and ML models are subsequently used to make predictions on less important ones."*

**2. METIS**
