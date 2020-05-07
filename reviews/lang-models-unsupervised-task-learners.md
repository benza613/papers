# Language Models are Unsupervised Multitask Learners.

Alec Radford, Jeffrey Wu, Rewon Child, David Luan, Dario Amodei, Ilya Sutskever


## Summary 

- In “Language Models are Unsupervised Multitask Learners”, Radford et all have presented a novel approach to solving natural language processing tasks that normally require a supervised approach. 

- The authors present their findings on how language models can be trained to solve domain specific tasks without the need for specific training examples. Basically, the idea put forward is generalization of training language models to be able to solve tasks in multiple domains without need for explicit supervision and training. 

- The authors implement this approach by combining two relevant approaches, namely task conditioning & zero shot learning. They also run a series of experiments to show how their model performs against other smaller parameter models & finally evaluated & contrasted their findings for a variety of natural language tasks. 

## Thoughts on Strength / Weaknesses 

- The main strength of this paper is naturally its novel approach that it is putting forward towards building unsupervised multitask learners in order to generalize language modelling. 

- Traditionally ML & NLP systems require training examples to learn correct behavior. The authors have demonstrated several experiments in a zero-shot setting to show that generalization of language model training can be possible. This means that they are able to prime the model using little to none training examples that are task specific to the specific domain. 

- While this paper doesn’t show any significant points of concern, I would be slightly concerned about the 1Billion+ parameters size for their GPT-2 model & the related humongous computing power. Naturally, for implementing a model so huge the compute space requirement would definitely be a challenge in itself. 

## Thoughts on Analysis / Evaluation

- The methodology put forward by this paper realizes language model probability as a representation of output by context given specific task to realize multitask learning. The authors have aimed to build a diverse & rich dataset as big as possible in order to aggregate natural language representations of tasks in as varied domains and contexts possible. 

- While scraping, they kept a focus on content quality that have been curated or filtered by other human readers & in this process created a dataset called WebText, which is basically the subset of over 45 million documents. 

- I find the text encoding approach taken by the authors to be quite novel. By using a byte level encoding they are able to lower their vocabulary size significantly. This approach lets them combine the benefits of word level language modelling with the byte level approach of generality. The authors finally trained multiple variations of the GPT model, which at that time was one of the biggest data models available. 

- They ran a series of experiments on this combination of WebText trained GPT-2 towards evaluating multiple language model benchmarks. A eye-catching observation here was the SOTA accuracy results for models that especially had a larger number of parameters in the language model. The authors have evaluated their GPT-2 model and published their findings for a variety of tasks like random unseen context completions, summary generation, reading comprehensions, English-French translations, etc. 


_Ultimately, I feel that this paper has shown tremendous improvements towards generalization of language models as compared to the few related works that they contrasted against. The authors have presented their claims & findings in a concise and lucid manner & have also provided various results in the appendix from the number of experiments they conducted._



#### Citation 

Paper Citation: Radford, A, Wu, J, Child, R, Luan, D, Amodei, D, and Sutskever, I 2018 Language Models are Unsupervised Multitask Learners. Available at https://d4mucfpksywv.cloudfront.net/better-language-models/language-models.pdf