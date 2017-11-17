---
layout: post
title: "Benchmarking Geometric Convolutions in TensorFlow"
description: "Benchmarking Geometric Convolutions in TensorFlow"
comments: true
categories: Research
keywords: "dummy content, lorem ipsum"
---

### Benchmarking Geometric Convolutions in TensorFlow

I made a series of benchmark experiments about TensorFlow implementations of Geometric Convolutions [MoNet]. In particular, I tried to exploit sparse matrix computation to speed-up and optimize the memory requirements of [MoNet]. My impression is that TF sparse matrix computations are not yet advanced enough to make this faster than dense computations. It would be a really usefull feature.

I tested the following settings:   

#### *BenchmarkStandardConvolution:* Standard convolutional Neural net
Average Time 0.00098 s. It runs on the GPU such a speed is possible thanks to the regular grid organisation.

#### *BenchmarkGraphLaplacianConvolutionSparse* of [gcn]:   
Average Time 0.00889 s. TensorFlow takes advantage of the *pre-computed* Sparse Laplacian Matrix to perform very efficient GPU operations. However, this model has a limited expressivity as the convolutions are performed by a for of "averaging" of the neighbouring features using Laplacian matrices.

#### *BenchmarkGeometricConvolutionDense* of [MoNet]:   
Average Time 0.27200 s. It corresponds to the dense version as implemented in the public code of [MoNet]. 
TensorFlow uses GPU computation with dense adjacency matrices. The main drawback is the memory requirements which limit the graph size and the number of features.

#### *BenchmarkGeometricConvolutionSparse* of [MoNet]:   
Average Time 1.67996 s. TensorFlow cannot use the GPU to perform some sparse matrix operations which related to the construction of the sparse geometric weight matrix used
in Geometric Convolutions.

The efficiency and speed achieved by sparse matrix multiplications in [gcn], calls for a Sparse GPU implementation of the Geometric Convolutions [MoNet].

## References
[gcn] : Thomas N. Kipf, Max Welling, Semi-Supervised Classification with Graph Convolutional Networks, ICLR 2017
[MoNet] : F. Monti*, D. Boscaini*, J. Masci, E. Rodolà, J. Svoboda, M. M. Bronstein, Geometric deep learning on graphs and manifolds using mixture model CNNs, CVPR 2017 (MoNet framework)

[TF Code on GitHub](https://github.com/pierrebaque/GeometricConvolutionsBench)
