# Recurrent neural networks

This note is about recurrent neural networks (RNN). These networks belong to supervised learning and are used in the analysis and prediction of time series or series like data.

There are three general types of RNNs describing the series relation in input and output:

| Type         | Example                   |
| ------------ | ------------------------- |
| One to many  | Sentence describing image |
| Many to one  | Sentiment analysis        |
| Many to many | Sentence translation      |

## Vanishing / exploding gradient problem

RNNs can inhibit the vanishing / exploding gradient problem.
One popular solution ist the use of long short-term memory (LSTM) nodes.

## Further readings:

* Diplomarbeit Josef Hochreiter, 1991: <http://people.idsia.ch/~juergen/SeppHochreiter1991ThesisAdvisorSchmidhuber.pdf>
