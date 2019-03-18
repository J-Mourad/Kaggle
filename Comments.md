##  1x1 convolutions

- control the depth of the input volume as it is passed to the next layer, either decrease it, or increase it, or just add a non-linearity when it doesn’t alter the depth. This control is achieved by the choosing the appropriate number of filters. We can control the other two dimensions - width and height by the filter sizes and padding parameters, or use pooling to reduce width and height.

- In the case when it is reduces the dimensions, it is a means to reduce computations
![img](https://qph.fs.quoracdn.net/main-qimg-7df9c28f92d879d9f9e6d25f6f991a1e)

### Ensembling of Neural Networks[.](https://towardsdatascience.com/stochastic-weight-averaging-a-new-way-to-get-state-of-the-art-results-in-deep-learning-c639ccf36a)

- Usually it is a good idea to use neural networks of different architectures in an ensemble, because they will likely make mistakes on different training samples and therefore the benefit of ensembling will be larger.

- Ridge regression is one particular way of combining several predictions which is used by [Kaggle-winning machine learning practitioners](http://blog.kaggle.com/2017/10/17/planet-understanding-the-amazon-from-space-1st-place-winners-interview/).

- SWA is not an ensemble in its classical understanding. At the end of training you get one model, but it’s performance beats snapshot ensembles and approaches FGE.



## Learning rate :

is a [hyperparameter](https://en.wikipedia.org/wiki/Hyperparameter) that controls how much you are adjusting the weights of our network with respect to the loss gradient.

- The goal of gradient descent is to find the minima of the loss function your neural network is trying to optimize.

- There is no fixed learning rate for a neural network. It depends on the kind of problem you are working on, the type of data you are feeding to your network, and most importantly the structure of the network which varies from problem to problem

- The most common practice is to set the learning rate to a constant value and decrease it by order of magnitude once the accuracy has plateaued.

- CLR gives an approach for setting the global learning rates for training neural networks that eliminate the need to perform tons of experiments to find the best values with no additional computation.

  ![img](https://cdn-images-1.medium.com/freeze/max/1000/1*VAmbyfpR0_-gP0oIla0Vjw.png?q=20)

## Stochastic Gradient Descent with Restarts (SGDR):

- A variant of learning rate annealing, which gradually decreases the learning rate through training.

- SGDR uses *cosine annealing*, which decreases learning rate in the form of half a cosine curve

  ![img](https://cdn-images-1.medium.com/max/1000/1*2NAuh6DbcrrMv4Voq5yG9A.png)

  ![img](https://cdn-images-1.medium.com/max/1000/1*kbP1fkMFrcjwBO3NVP9OfQ.png)


