# Scikit-Learn

## Design Principles

### Estimator

e.g. `SimpleImputer`

**Estimator** objects have a method`fit()`which takes a dataset as a parameter \(to learn\). Other parameters are **hyperparameters** passed in via a constructor.

All the estimator's **hyperparameters** are accessible via public instance variable \(e.g. `imputer.strategy` and all **learned parameters** are accessible via public instance with an underscore suffix \(e.g. `imputer.statistics_`\). 

###  Transformer

e.g. `OneHotEncoder`

Some **estimators** can also **transform** dataset hence also **transformers**.

A `transform()` method takes a dataset as a parameter and returns the transformed dataset. This process depends on the learned parameters. 

Transformers also have a convenient method`fit_transform()`with optimisations. 

### Predictor

e.g. `LinearRegression`

Some **estimators** can also **predict** hence also **predictors**.

A `predict()` method takes a new dataset and returns a dataset of corresponding predictions. 

A `score` method can measure the quality of prediction, given a test set.

