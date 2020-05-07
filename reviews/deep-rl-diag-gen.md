# Deep Reinforcement Learning for Dialogue Generation

Jiwei Li, Will Monroe, Alan Ritter, Michel Galley, Jianfeng Gao, Dan Jurafsky. 


## Summary 

- In “Deep Reinforcement Learning for Dialogue Generation”, Li, Monroe et all have presented an approach to building conversational agents that focus on more sustained & interactive dialogue generation. The authors present their findings on how their approach basically aims to minimize repetitive & generic responses in conversational flow. 

- The approach put forward builds upon the sequence to sequence attention model with policies that aim to optimize conversational quality through reinforcement. The authors implement this approach by using what they call policy gradients in the reinforcement loop that reward specific dialogue properties. 

- They also develop a number of metrics to evaluate the models & conduct qualitative analysis. Finally, the authors evaluated & contrasted their results with existing dialogue generation approaches. 

## Thoughts on Strength / Weaknesses 

- Naturally one of the main strengths of this paper is the novel approach it takes towards defining & evaluating optimal policies that maximize conversational quality. 

- The authors implement a policy here in the form of an encoder-decoder LSTM architecture that represents itself as a probability distribution over choice of output responses. The authors have also used a reinforcement learning approach here by implementing an Alpha-Go style approach wherein they simulate conversation between two virtual agents to learn desirable policies that are maximizing dialogue quality. 

- While I do not see any major issue with this paper, it would be interesting to see some follow up on more objective evaluation metrics for developed models here. Of course, evaluation of dialogue agents is harder than other NLP tasks and it is made even harder by one of the proposed goals being long term dialogue quality.

## Thoughts on Analysis / Evaluation

- The methodology put forward by this paper describes how policy reinforcement approach aims to improve conversational flow & quality. The authors build upon a sequence to sequence attention model by pretraining with the usual supervised approach and then they fine tune it using a policy network. 

- The interesting aspects that these policies focus on maximizing are are ease of answering, information flow & semantic coherence. The authors feel that this process helps in keeping the conversation moving, improves potential dialog history & long-term engagement. 

- The authors also trained the model using the OpenSubtitles dataset. The authors finally spoke about the numerous difficulties in evaluating these type of dialogue systems objectively using established metrics like Bleu & perplexity scores & how they cannot really evaluate conversational black holes. 

- They finally evaluated these models using parameters like dialogue length, n-gram frequency & human response evaluations. I feel these methods would be justified as the conventional metrics might not accurately measure long term context or quality well, as pointed out by the authors too. 


_Overall, I feel that this paper has shown significant improvements as compared to the previous traditional approaches to dialogue generation in related works. The authors have presented their approach in a concise and well laid out manner. I do believe that the authors have put forward several good points & feel that their results towards a neural dialogue model based on long term contextuality seems quite encouraging._



#### Citation 

Jiwei Li, Will Monroe, Alan Ritter, Michel Galley, Jianfeng Gao, Dan Jurafsky. Proceedings of the 2016 Conference on Empirical Methods in Natural Language Processing. “Deep Reinforcement Learning for Dialogue Generation”. 2016. https://www.aclweb.org/anthology/D16-1127