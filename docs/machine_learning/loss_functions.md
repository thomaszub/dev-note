# Loss functions

This note is about loss functions used in training neural networks.

## Extensions

The folowing extension can be added to induce effects in minimizing the loss function.

### Regularization

Regularization penalizes high values of the parameters in a neural network and helps against overfitting.
The corresponding loss extension term has the form

\[
L_p(\Theta) = \lambda \|\Theta\|^p
\]

with \( \lambda \) the regularization factor, \( \Theta \) the training parameters and \( p \in \mathbb{N} \), typically with \( p = 2 \) (L2-Norm).
### Momentum

To mitigate oscillations in the training of the parameters, a momentum extension can be used.
This term is added to the update of the parameters in gradient descent


\[
  \Theta^{(t+1)} = \Theta^{(t)} + \Delta \Theta_{GD}^{(t)} + \nu \Delta \Theta^{(t-1)} = \Theta^{(t)} + \Delta \Theta^{(t)}
\]

with \( t \) the update step, \( \Theta \) the training parameters and \( \nu \) the momentum factor.
## Cross entropy

For classification problems the output of the network can be choosen to be a vector of probabilities \( q(y) \) for the different classes \( y \in Y \). With the expected result \( p(y) = \delta_{y,\hat{y}} \) and the correct class \( \hat{y} \), the cross entropy can be used:

\[
  H(p, q) = - \sum_{y \in Y}{p(y) \log(q(y))}
\]
