# How to disable cross validation in grid search CV

```python
from sklearn import svm, datasets, model_selection

iris = datasets.load_iris()
parameters = {'kernel':('linear', 'rbf'), 'C':[1, 10]}

clf = model_selection.GridSearchCV(svm.SVC(), parameters, cv=[(slice(None), slice(None))])
clf.fit(iris.data, iris.target)
```

- `from sklearn import` - import module from [lib:scikit-learn](https://onelinerhub.com/python-scikit-learn/how-to-install-scikit-learn-using-pip)
- `load_iris` - loads [Iris](https://scikit-learn.org/stable/auto_examples/datasets/plot_iris_dataset.html) dataset
- `parameters` - parameters dictionary to run grid search accross
- `.GridSearchCV(` - creates GridSearchCV model
- `svm.SVC()` - use [SVC](https://onelinerhub.com/python-scikit-learn/svc-classifier-example) model as an estimator
- `.fit(` - train transformation model
- `[(slice(None), slice(None))]` - will disable cross validation

group: grid-search

## Example: 
```python
from sklearn import svm, datasets, model_selection

iris = datasets.load_iris()
parameters = {'kernel':('linear', 'rbf'), 'C':[1, 10]}

clf = model_selection.GridSearchCV(svm.SVC(), parameters, cv=[(slice(None), slice(None))])
clf.fit(iris.data, iris.target)

print(clf.best_estimator_)
```
```
SVC(C=1, kernel='linear')

```

