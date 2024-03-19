---
layout: page
title: Label-Free XAI 
description: In this work, we evaluate the reproducibility of the paper Label-Free Explainability for Unsupervised Models by Crabbe and van der Schaar. Our goal is to reproduce the paper's four main claims in a label‐free setting and extend it's research to assess robustness.
img: assets/img/label-free-xai.png
importance: -1
category: masters
related_publications: false
---

Deep learning models are getting more and more advanced, making it difficult for humans to understand and retrace how an algorithm arrives at a specific result. To solve this problem, explanation methods were developed.

Post‐Hoc methods separate explanations from models allowing explanation methods to be compatible with a variety of models. They treat these models as "black boxes" due to their increasing complexity. Most of the post‐hoc explanation techniques require labels to explain black‐box outputs and thus they work only in a supervised setting. The paper Label-Free Explainability for Unsupervised Models, by J. Crabbé and M. van der Schaar's goal is to explain black‐box outputs in a label‐free setting. The authors introduce two extensions for the Feature Importance and the Example Importance that highlight influential features and training examples respectively for a black box to construct representations at inference time.

The contribution of our work is summarized as follows:
1. We reproduce the main experiments by Crabbé and Schaar to reproduce their main claims.
2. We conduct additional experiments to assess the robustness of label‐free techniques proposed by the authors. Since they originally experiment on image and time‐series datasets, we extend their techniques to find salient features and training samples for graphs and text datasets respectively.
3. We find that one of the authors' claims is model‐specific when we introduce a penalty term to the loss function of those models.

The code implementation of our study is publicly available <a href="https://github.com/vpariza/Re-Label-Free-XAI">here</a>.
Read more <a href="https://openreview.net/pdf?id=qP34dvJpHd">here</a>.
