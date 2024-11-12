---
layout: page
title: Hitting "Probe"rty with Non-Linearity
description: We reformulate the design of nonlinear structural probes introduced by (White et al., 2021) making its design simpler yet effective. We also design a visualization framework that lets us qualitatively assess how strongly two words in a sentence are connected in the predicted dependency tree.
img: assets/img/linear_rbf_12.png
importance: -2
category: masters
---

In human languages, the meaning of a sentence is composed hierarchically - small chunks of words together make successively larger chunks. We refer to this tree-structured hierarchy of a sentence as a dependency tree. Hewitt and Manning (2019), introduces "Structural Probes" that tests a simple hypothesis for how dependency trees may be embedded in the hidden states of a language model. The probe in this context is a model that learns a linear transformation such that two words that are syntactically close to one another should also have less distance between their respective contextual representations.

One of the advantages of these structural probes is simplicity. However, this simple design may not allow for full exploitation of the structure of the encoded information. This motivates us to investigate whether the dependency structure is encoded in a non-linear way. White et al. (2021), introduces three non-linear structural probes - polynomial, radial basis function, and sigmoid. We reformulate these non-linear probe variants. We then apply these probes on contextualized embeddings of BERT and BERT-Large. Since different layers of BERT capture different linguistic properties, can our probing method tell us how dependency information is encoded in every layer? This question (as far as we know) hasn't been answered yet in the existing literature. We answer this question by applying a non-linear probing variant-RBF across the layers of BERT and BERT-Large.

We expect the non-linear variants to perform better than linear probes due to the complex nature of the dependency trees which might be better captured by non-linear probes. We test this hypothesis quantitatively using undirected attachment score (UUAS). Additionally, we test this hypothesis qualitatively by introducing a measure that computes the strength with which the probe predicts dependency between two words.

We find that Radial Basis Function (RBF) probe is more effective than the linear probe for BERT. And we are also able to understand how every layer gradually encodes syntactical information to form a complete dependency tree.

The code implementation of our study is publicly available <a href="https://github.com/madhu221b/probing-lms">here</a>.
Read more <a href="https://arxiv.org/abs/2402.16168v1">here</a>.
