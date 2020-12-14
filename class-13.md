# Explore the Tech!

## Linear Regression:


`Scikit-learn` is a powerful Python module for machine learning. It contains function for `regression`, `classification`, `clustering`, `model selection` and `dimensionality reduction`. 

#### Linear regression in python: implementing linear regression in Python using Scikit-learn.

Ordinary least squares Linear Regression.

LinearRegression fits a linear model with coefficients w = (w1, …, wp) to minimize the residual sum of squares between the observed targets in the dataset, and the targets predicted by the linear approximation.

##### Parameters
* `fit_interceptbool, default=True`
Whether to calculate the intercept for this model. If set to `False`, no intercept will be used in calculations (i.e. data is expected to be centered).

* `normalizebool, default=False`
This parameter is ignored when `fit_intercept` is set to `False`. If `True`, the regressors `X` will be normalized before regression by subtracting the mean and dividing by the l2-norm. 
If you wish to standardize, please use `sklearn.preprocessing.StandardScaler` before calling fit on an estimator with `normalize=False`.

* `copy_Xbool, default=True`
If `True`, `X` will be copied; else, it may be overwritten.

* `n_jobsint, default=None`
The number of jobs to use for the computation. This will only provide speedup for `n_targets > 1` and sufficient large problems. 
None means 1 unless in a `joblib.parallel_backend` context. -1 means using all processors. See Glossary for more details.


##### Attributes
* `coef_array of shape (n_features, ) or (n_targets, n_features)`
Estimated coefficients for the linear regression problem. If multiple targets are passed during the fit `(y 2D)`, this is a 2D array of shape `(n_targets, n_features)`,
while if only one target is passed, this is a 1D array of length `n_features`.

* `rank_int`
Rank of matrix `X`. Only available when `X` is dense.

* `singular_array of shape (min(X, y),)`
Singular values of `X`. Only available when `X` is dense.

* `intercept_float or array of shape (n_targets,)`
Independent term in the linear model. Set to 0.0 if `fit_intercept = False.`


##### Examples
```
>>>
>>> import numpy as np
>>> from sklearn.linear_model import LinearRegression
>>> X = np.array([[1, 1], [1, 2], [2, 2], [2, 3]])
>>> # y = 1 * x_0 + 2 * x_1 + 3
>>> y = np.dot(X, np.array([1, 2])) + 3
>>> reg = LinearRegression().fit(X, y)
>>> reg.score(X, y)
1.0
>>> reg.coef_
array([1., 2.])
>>> reg.intercept_
3.0000...
>>> reg.predict(np.array([[3, 5]]))
array([16.])
```


##### Methods

* `fit(X, y[, sample_weight])`: Fit linear model.

* `get_params([deep])`: Get parameters for this estimator.

* `predict(X)`: Predict using the linear model.

* `score(X, y[, sample_weight])`: Return the coefficient of determination `R^2` of the prediction.

* `set_params(**params)`: Set the parameters of this estimator.
