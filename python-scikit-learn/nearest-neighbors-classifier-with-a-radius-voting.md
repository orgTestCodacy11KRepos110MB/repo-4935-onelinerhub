# Nearest neighbors classifier with a radius voting

```python
from sklearn import datasets, neighbors, model_selection

X, y = datasets.load_iris(return_X_y=True)
X_train, X_test, y_train, y_test = model_selection.train_test_split(X, y)

model = neighbors.RadiusNeighborsClassifier(0.75)
model.fit(X_train, y_train)
y_pred = model.predict(X_test)
```

- `from sklearn import` - import module from [lib:scikit-learn](https://onelinerhub.com/python-scikit-learn/how-to-install-scikit-learn-using-pip)
- `load_iris` - loads [Iris](https://scikit-learn.org/stable/auto_examples/datasets/plot_iris_dataset.html) dataset
- `model_selection.train_test_split` - splits given `X` and `y` datasets to test (25% of values by default) and train (75% of values by default) subsets
- `.RadiusNeighborsClassifier(` - K neighbors classification model with a given radius neighbors voting
- `0.75` - radius to vote within
- `.fit(` - train model with a given features and target variable dataset
- `.predict(` - predict target variable based on given features dataset

group: nn

## Example: 
```python
from sklearn import datasets, neighbors, model_selection

X, y = datasets.load_iris(return_X_y=True)
X_train, X_test, y_train, y_test = model_selection.train_test_split(X, y)

model = neighbors.RadiusNeighborsClassifier(0.75)
model.fit(X_train, y_train)
y_pred = model.predict(X_test)

print(y_pred)
```
```
[1 0 1 2 1 0 2 2 2 2 0 0 2 1 1 1 1 0 0 2 1 2 2 0 2 0 2 1 2 1 2 1 2 1 1 1 0
 1]

```

