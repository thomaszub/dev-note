# Loss functions

This note is about loss functions used in training neural networks.

## Cross entropy

For classification problems the output of the network can be choosen to be a vector of probabilities \( q(y) \) for the different classes \( y \in Y \). With the expected result \( p(y) = \delta_{y,\hat{y}} \) and the correct class \( \hat{y} \), the cross entropy can be used:

\[
  H(p, q) = - \sum_{y \in Y}{p(y) \log(q(y))}
\]
