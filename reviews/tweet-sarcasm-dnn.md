# Tweet Sarcasm Detection using Deep Neural Networks

Meishan Zhang, Yue Zhang and Guohong Fu


## Summary 

In “Tweet Sarcasm Detection using Deep Neural Networks”, Zhang et al have presented an approach to sarcasm detection using a recurrent neural network architecture. 

- Sarcasm detection on online social media is actually a growing area of interest in present day. It is basically the task of detecting if a given text is sarcastic. They present this paper as a contrast of the traditional methods by which feature extraction normally takes place using lexical methods. 

- The authors have designed & implemented a bi-directional gated recurrent neural network for this very purpose. They also run a series of experiments to show how deep learning can help improve accuracy rates in the task of sarcasm detection. The authors have also evaluated the neural induced features against manual discrete features & contrasted their findings. 

## Thoughts on Strength / Weaknesses 

- One of the main strengths of this paper is the novel approach it takes towards learning features automatically via a deep learning approach. They have elaborated on previous works wherein features have to be extracted manually using a combination of natural language processing techniques like POS tags, lexical n-grams, word sentiments, etc. The authors have used deep learning approach to induce these features automatically which results in much more long-range semantic meaning. 

- A key point of concern for this paper maybe could be the aspect of using the limited history of tweets as a contextual reference in capturing semantic information. Basically, while the accuracy of detection by the neural model is at acceptable levels without context, it is actually much higher when the history of that tweets’ author is present. This indicates a significant dependency on context of tweets from similar authors for the model to be really successful.

## Thoughts on Analysis / Evaluation

- The methodology put forward by this paper describes the architecture as two components: the local and contextual components. The local component is a bi-directional gated recurrent neural network that models the input tweet & extracts semantic features from the whole tweet. Whereas the contextual component is just using the contextual words extracted from previous history tweet & does not require a RNN here. 

- The authors have used a dataset previously collected & annotated by Rajadesingan et al. They are feeding the tweets as an input to the neural network model using Glove embeddings. They also developed baselines to test their model with & without the contextual input to see the effect context from a particular author has on sarcasm detection. I find the results of this experiment quite interesting. 

- The authors finally trained gated RNN models using both balanced and unbalanced datasets that had higher number of not sarcastic tweets & evaluated these models using 10-fold cross validation as a major metric. I think they handled the issues of unbalanced data well by also computing averaged F-scores as well. I find it rather pleasing that their experiments showed a much higher accuracy over the traditional baseline approach & showed considerable improvements in sarcasm detection when contextual input was applied too.


_Ultimately, I feel that this paper has shown significant improvements as compared to the previous traditional approaches to sarcasm detection. The authors have presented their claims in a concise and lucid manner & have made considerable efforts to justify them in the number of experiments they conducted._



#### Citation 

Meishan Zhang, Yue Zhang and Guohong Fu. Proceedings of COLING 2016, the 26th International Conference on Computational Linguistics: Technical Papers, pages 2449–2460, Osaka, Japan, December 11-17-2016. Tweet Sarcasm Detection Using Deep Neural Network. https://www.aclweb.org/anthology/C16-1231.pdf