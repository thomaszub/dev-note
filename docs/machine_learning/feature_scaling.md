# Feature scaling

Feature scaling is a data preprocessing step to ease training of neural networks by reducing the numeric scale of different features to a uniform scale.

## Standardisation

Standardisation transforms the feature distribution of data to zero mean and unit variance:

\[
z = \frac{x - \operatorname{mean}(x)}{\operatorname{std}(x)}
\]

*Python:*
```python
from sklearn.preprocessing import StandardScaler
```

## Normalisation

Normalisation transforms the feature distribution to the interval \([0,1]\):

\[
z = \frac{x - \min(x)}{\max(x) - \min(x)}
\]

*Python:*
```python
from sklearn.preprocessing import MinMaxScaler
```
