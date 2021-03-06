# pathnet

Tensorflow Implementation of Pathnet from Google Deepmind.

https://arxiv.org/pdf/1701.08734.pdf

"Agents are pathways (views) through the network which determine the subset of parameters that are used and updated by the forwards and backwards passes of the backpropogation algorithm. During learning, a tournament selection genetic algorithm is used to select pathways through the neural network for replication and mutation. Pathway fitness is the performance of that pathway measured according to a cost function. We demonstrate successful transfer learning; fixing the parameters along a path learned on task A and re-evolving a new population of paths for task B, allows task B to be learned faster than it could be learned from scratch or after fine-tuning."
Form Paper

![alt tag](https://github.com/jaesik817/pathnet/blob/master/figures/pathnet.PNG)

Implementation is on Tensorflow 1.0

[Binary MNIST classification tasks]

python binary_mnist_pathnet.py

Basically, almost parameters are used same to paper, however, I used AdamOptimizer with learning_rate=0.001.

Task1 is classification between "5" and "6", and task2 is classification between "8" and "9".

When two candidates are learned & evaluated, learned parameters from each candidates are saved, and winner parameters are updated to model.

Learning_rate is reset after finishing task1.
