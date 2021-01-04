# Activation functions

## Sigmoid / Logistic

The Sigmoid activation function is defined by

\[
  \sigma(x) = \frac{1}{1 + e^{-x}}
\]

As the Sigmoid function has the bounds [0, 1], it is suited for multi-label classification as the element results can be trained as probabilities for a certain label to be true or not.

## Softmax

The Softmax activation function is defined by

\[
  \sigma_j(x) = \frac{e^{x_j}}{\sum_j{e^{x_j}}}
\]

In comparison to most activation functions, the sum of all element-wise results is constrained, precisely speaking:

\[
  \sum_j \sigma_j(x) = 1
\]

Therefore the Softmax function is suited for multi-class classification as the element results can be trained as probabilities for a certain class in one category to be true or not.
