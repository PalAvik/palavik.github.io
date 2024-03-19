---
layout: page
title: PIF for NBR
description: We conducted a thorough examination of fairness for Next Basket Recommendation (NBR) task by considering user characteristics. We introduced novel β-VAE architecture to model NBR. The findings highlight the challenges posed by smaller basket sizes and suggest avenues for future research to improve NBR performance.
img: assets/img/PIF_VAE.png
importance: -4
category: masters
---

Applications of Recommender Systems have been widespread recently as organizations look to promote and sell their products using state-of-the-art tools and algorithms. Next-basket recommendation (NBR) is a problem within this field that aims to predict a subsequent set of items for a user and is prevalent in the e-commerce and retail industries. Hu et al. showed that the user's item purchase frequency information modeled as Personalized Item Frequency (PIF) vectors provide two useful signals for the NBR task - repeated and collaborative purchase patterns. They propose a method to capture the two patterns along with the temporal dynamics of previous baskets using a simple k-nearest neighbors (kNN) approach called temporal-item-frequency-based user-KNN (TIFU-KNN). They demonstrate its effectiveness on four real-world datasets using recall and NDCG evaluation metrics.

In this work, we verify the reproducibility of the proposed TIFU-KNN model by reproducing the results on the four datasets. We also keep the Personalized Top Frequency method as our baseline because it's rarely beaten as repeated purchase patterns dominate in most real-world instances. It's also observed that the datasets used are all related to grocery shopping and might not provide a broad view of the method covering the task of NBR. Hence, we test the TIFU-KNN method on additional NBR datasets to examine its robustness. To further characterize the method in comparison to the baseline frequency method, we also evaluate the method on other NBR metrics - MRR, and PHR. Additionally, we observe a lack but a definite need for fairness metrics in the literature for NBR. Hence, we also introduce metrics to validate and visualize the amount of fairness the NBR methods exhibit towards both users and items. 

Finally, we also try to model the sparse user representations in a latent space with a deep model using a Variational Autoencoder (VAE) architecture to capture intrinsic patterns of the user PIF vectors. We also experiment with kNN approach on these dense vectors produced by VAE to inspect the importance of collaborative purchase patterns for NBR.

Thus, we ask the following research questions in our study:
1. Are the results for TIFU-KNN from the original paper \cite{modeling-pif-hu} reproducible?
2. Is TIFU-KNN robust enough to perform well on other NBR datasets? 
3. Is TIFU-KNN performance consistent on metrics beyond recall and NDCG?
4. Is the TIFU-KNN method fair towards users and items?
5. Can a deep model like VAE better capture the purchase patterns?

In summary, our experiments show that the results of TIFU-KNN in the original paper are reproducible with little variations. The model again outperforms plain frequency methods on new datasets which is also verified using additional metrics. Our fairness analysis proves that model performance is dependent on the dataset and user characteristics. Lastly, NBR with VAE architecture remains challenging but still provides some useful trends, and future work in better representation learning could further provide gainful insights into recommender systems.

The code implementation of our study is publicly available <a href="https://github.com/madhu221b/probing-lms">here</a>.
Read more <a href="https://arxiv.org/abs/2402.16168v1">here</a>.
