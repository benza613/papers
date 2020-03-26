# Distributed representations of words and phrases and their compositionality.

Tomas Mikolov, Ilya Sutskever, Kai Chen, Greg Corrado, and Jeffrey Dean


## Summary 

In “Distributed Representations of Words and Phrases and their Compositionality”, Mikolov et al. present several extensions to improve the skip-gram model that was used to learn high quality vector representations of words from a large text corpus.

- The aim of these authors was to improve the quality of the vectors as well as the training times for these embeddings. They also describe & implement Negative Sampling, which is a simplified version of Noise Contrastive Estimation (NCE) for training the model.

- Word vector representations have varied downstream applications in tasks like Sentiment classification, machine learning & computational linguistics among others. In this paper, a few limitations of these representations are described and how the skip gram model can help overcome those limitations. The authors then evaluated various techniques to train & learn word representations & contrasted the accuracies of each method.

## Thoughts on Strength / Weaknesses 

- One of the key strengths of this paper is the improvements it puts forward over then existing skip-gram model resulting in models that are computationally efficient & can be trained using more larger data than previous published models. This in turns results in improving the quality of the word and phrase embeddings which the model learns. 

- Another key point that they have demonstrated is that these high-quality embeddings also help make analogical reasoning tasks much simpler and more accurate. 

- An issue with their work could be taken with respect to accuracy in prediction. While they did report a marginal increase in accuracy over previous published models ~60-70%, I would still not consider it significant enough to be groundbreaking. They also manually experimented with a variety of hyperparameter values to observe accuracy & training times. In a particular case, they ended up using a unigram distribution raised to the 3/4th power for negative sampling, that outperformed other distribution patterns for prediction tasks. The correlation of any of the classification algorithms used or hyperparameter values on a type of prediction task, if any, has not be reported.

## Thoughts on Analysis / Evaluation

- The methodology put forward by this paper retains the unsupervised learning nature of the earlier skip-gram model. The authors’ methodology has implemented techniques like hierarchical softmax, negative sampling & subsampling of frequent words while training the model on various news articles from a Google Dataset of 1 billion words. 

- I think an interesting direction for future work could involve study with dataset from a different domain like finance or real estate, wherein context would not be as readily available as compared to news articles or if training times or embedding quality would suffer or not. 

- The authors finally trained models using these various techniques and evaluated them using an analogical reasoning task & showed considerable improvements in training times over a larger order of data. This task handled phrase analogy & similarity quite well apparently by demonstrating the embeddings’ linear structures. 


_Overall, I think that the authors have put forward several good points & feel that their claims that they have concluded with to be reasonably justified. They have made efforts to improve the skip-gram models training times & accuracy and even demonstrate the learned representations’ additive compositionality, which is basically addition of two word-vectors._



#### Citation 

Tomas Mikolov, Ilya Sutskever, Kai Chen, Greg Corrado, and Jeffrey Dean. 2013. Distributed representations of words and phrases and their compositionality. In Proceedings of the 26th International Conference on Neural Information Processing Systems - Volume 2 (NIPS’13). Curran Associates Inc., Red Hook, NY, USA, 3111–3119.