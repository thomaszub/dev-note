# Data preprocessing

## Label encoder

*Python:*
```python
from sklearn.preprocessing import LabelEncoder
```

## One hot encoder

*Python:*
```python
from sklearn.preprocessing import OneHotEncoder
```

## Column transformer

Scikit-learn contains a class for applying multiple transformations to a dataset including dropping columns:

*Python:*
```python
from sklearn.compose import ColumnTransformer
```

*Note:* Does currently not work with a LabelEncoder.

