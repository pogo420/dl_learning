# dl_learning
Deep learning  concepts and implementation

## AI Tree:
* AI mimics the human behaviour.
* Following are the part of AI:
   * NLP/Regular Expression.
   * Code with flow and condition.
   * Robotics.
   * Statistical ML
   * Deep Learning
      * Neural networks.(RNN, CNN, Transformers)
* NLP + Transformers => LLM or large language models.

## Statistical ML vs Deep learning
|Satistical | Deep|
|--|--|
| Classical algorithms | Neural Networks |
|Results can be explained, as we derive equation. | We can't explain why its making a decision | 
| Low volume | Large Volume |
| Less compute | More compute |

## Neural Networks:
### Intro:
- Mimics the human brain(Simple version)
- Network of neurons.
- Ability to identify pattern once trained.

### Types:
- Feed forward (FNN)
   - Data flows one layer to other. 
   - No feedback involved.
   - Structured data.
- Recurrent (RNN)
   - Output of network will be added to the network again with additional input.
   - Feedback involved.
   - Works in cycles.
   - Machine translation/text
- Convolutional (CNN)
   - Video ,Speech, Anomaly, etc.
- Trasformers (Base of LLM)
   - Text, Q&A, Translation.

### What is a neuron?
- Smallest unit of pattern identifier.
- Logistic regression is simplest form of neural network.
- It has two part:
    - Linear equation: $`y = \sum_{k=1}^n (W_iX_i)+B`$, W are weights, X are inputs and B is bias.
    - Activation function: $`z=sigmoid(y)`$, Binary output, neuron is either on or off.
    - Finally, $`z`$ is the output of neuron.
- Perceptron is a neuron where Activation function is setp function not sigmoid.
- MLP or multi layer percepton is a Feed forward NN.

### Activation functions:
- Sigmoid: $`sigmoid(z)=\frac{1}{1+e^{-z}}`$; Converts values from 0 to 1(Due to Vanishing gradient problem; not used in hidden layes).
- Softmax: Collects all inputs and converts them into probabilites, such that sum of all probabilities is 1.
- Tanh: Convert values from -1 to 1, $`tanh(z)=\frac{e^{z}-e^{-z}}{e^{z}+e^{-z}}`$
- ReLU: $`ReLU(z)=max(0,z)`$; Used in hidden layers(Not sutable when too many -ve values).
- Leaky ReLU: $`ReLU(z)=max(0.1z,z)`$; Used in hidden layers.

## Neural training:
- Setup network with ramdom weights.
- Feed the training data into the network.
- Calculate Error or loss.
- Fine tune weights on the neurons, so final error is less(It's called backward propagation)
- An epoch is called step 2 - step 4.
- Repeat if for epochs till you get a lower error.
- Once error/loss is under desirable level, network is ready for action.

### Backward propagation:
- Write in simple logic.
- Learn gradient descent.

## Gradient desccents
feature | batch gradient descend(GB) | mini batch gradient descend | stochastic gradient descend(SGD)
--|--|--|--
data used per update | entire dataset | small batch | single data point
convergence speed(How quickly we can reach local minima) | slow | medium | fast
compute effeciency | high | balanced | low
memory | high | modetare | low
convergence stability | stable  | balanced | less stable due to frequent updates
Noise in gradient update | low | moderate | High 
Large Data set application | nopes | good | very good
Example use cases | small data set | real world cases | Large dataset
