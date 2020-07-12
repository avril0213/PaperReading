# PaperReading

* 05/31/2020 [Deep Sets](https://arxiv.org/pdf/1703.06114.pdf)
```
A function f(X) is invariant to the permutation of instances in X iff it can be decomposed in the form of 
- a neural net \rho(.) on top of summation of the transform \phi(x) applied to each component in a set
```
* 06/28/2020 [MA-DNN](https://arxiv.org/pdf/1907.04667.pdf)
```
we create two external memory vectors for each user, memorizing high-level abstractions of what a user possibly likes and dislikes. 
The proposed MA-DNN achieves a good compromise between DNN and RNN. It is as simple as DNN, but has certain ability to exploit useful information contained in users’ historical behaviors as RNN.
Learn two user-level embeddings for label 0/1 separately, feed into dense together with other groups' embedding vectors. Pose an additional L2 loss to force the two embeddings close to last layer of DNN. This loss only updates the two embeddings(last layer only updated in cross-entropy loss).
```
* 07/06/2020 [MoSE](https://research.google/pubs/pub49274/)
```
Recently, using neural sequence models to effectively represent users’ activity streams has become popular in web applications.
The work in [3](https://research.google/pubs/pub46488/) studies how to effectively use context features(such as device) for recommending videos in Youtube. It uses LSTM to represent a user’s video watch history. 
[30](https://www.ismll.uni-hildesheim.de/pub/pdfs/RendleFreudenthaler2010-FPMC.pdf) is a personalized sequential recommendation model based on Markov chains. 
[39] applies a Recurrent Neural Network (RNN) for next basket recommendation.(https://cseweb.ucsd.edu/classes/fa17/cse291-b/reading/A%20Dynamic%20Recurrent%20Model%20for%20Next%20Basket%20Recommendation.pdf)
[33](https://arxiv.org/abs/1902.08588) uses RNN and Attention to model both short and long range dependencies in user sequences. 
[17](https://arxiv.org/abs/1808.09781) proposes a self-attention based sequential model for next item recommendation[13] shows that RNN can learn multiple user dynamics patterns in individual recommendation sessions.
```
* 07/06/2020 [Deep Learning for Sequential Recommendation](https://arxiv.org/pdf/1905.01997.pdf)

* 07/09/2020 [SimGNN](https://arxiv.org/pdf/1808.05689.pdf)
```
Use GCN + global context-aware attention (learn an adaptable/learnable context vector) to learn the graph embedding(hi, hj).
To calculate similarity of two embedding, it uses a "neural tensor network" which is like Factorization Machine.
The second strategy is a pairwise interaction between nodes and the histogram provides information for learning the first part. The second part id not differentiable.
```

Queue:
[MOE](https://arxiv.org/abs/1701.06538)

[ExplorationStrategiesInDL](https://lilianweng.github.io/lil-log/2020/06/07/exploration-strategies-in-deep-reinforcement-learning.html)

[RoBERTa](https://arxiv.org/abs/1907.11692)

[FaceNet](https://arxiv.org/abs/1503.03832)

[IntegratedGradient](https://arxiv.org/abs/1703.01365)

[VideoBERT](https://arxiv.org/abs/1904.01766)
