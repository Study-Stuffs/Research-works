## Introduction to Meta Reinforcement Learning

### Meta-learning: Learning to learn fast:

We expect a good meta-learning model capable of well adapting or generalizing to new tasks and new environments that have never been encountered during training time.  
The adaptation process, essentially a mini learning session, happens during test but with a limited exposure to new tasks configuration.

A good meta-learning model should be trained over a variety of learning tasks and optimized for the best performance on a distribution of tasks, including potentially unseen tasks.

### Common Approaches:

common approaches include: metric-based, model-based and optimization-based methods.

**Metric-based:**
The core idea in metric-based meta-learning is similar to nearest neighbors algorithms and kernel density estimation. To learn a good kernel is crucial to the success of a metric-based meta-learning model. Metric learning is well aligned with this intention, as it aims to learn a metric or distance function over objects.
Some models are:

- Convolutional Siamese Neural Network: The Siamese neural network is composed of two twin networks and their outputs are jointly trained on top with a function to learn the relationship between pairs of input data samples.
- Matching networks: the task of matching networks is to learn a classifier for any given support set. This classifier defines a probability distribution over output labels for any given query sample. 
- Relation network: the relation network is similar to siamese network but with a few differences:
    - the relationship is not captured by a simple L1 distance in the feature space, but predicted by a CNN classifier.
    - The objective function is MSE loss instead of cross-entropy, because conceptually RN focuses more on predicting relation scores.
- Prototypical networks: prototypical networks use an embedding function to encode each input into M-dimensional feature vector.A prototype feature vector is defined for every class as the mean vector of the embedded support data samples in this class.

**Model-based:** 
model-based meta-learning models make no assumption on the form. Rather it depends on a model designed specifically for fast learning.
Some models are:
- Memory-Augmented neural networks: A family of model architectures use external memory storage to facilitate the learning process of neural networks, including neural turing machines and memory networks. With an explicit storage buffer, it is easier for the network to rapidly incorporate new information and not to forget in the future.
- Meta networks: it is a meta-learning model with architecture and training process designed for rapid generalization across tasks.

**Optimization-based:** Deep learning models learn through backpropagation of gradients. However, the gradient-based optimization is neither designed to cope with a small number of training samples, nor to converge within a small number of optimization steps.Some models are:
- LSTM meta-learner: the optimization can be explicitly modeled. There is a similarity between the gradient-based update in backpropagation and the cell-state update in LSTM.
- MAML: Model-agnostic meta-learning is a fairly general optimization algorithm, compatible with any model that learns through gradient descent.
- Reptile: Reptile is a remarkably simple meta-learning optimization algorithm.It is similar to MAML in many ways, given that both rely on meta-optimization through gradient descent and both are model-agnostic.