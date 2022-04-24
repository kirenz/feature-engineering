(section-permutation-feature-importance)=
# Permutation feature importance

*The following content is based on tutorials provided by scikit-learn developers.*

Permutation feature importance overcomes limitations of the impurity-based feature importance ([scikit-learn developers](https://scikit-learn.org/stable/auto_examples/ensemble/plot_forest_importances.html)): 
  - they do not have a bias toward high-cardinality features
  - they can be computed on a left-out test set.

The permutation feature importance is defined to be the decrease in a model score when a single feature value is randomly shuffled. This procedure breaks the relationship between the feature and the target, thus the drop in the model score is indicative of how much the model depends on the feature. This technique benefits from being model agnostic and can be calculated many times with different permutations of the feature.

```{note}
Permutation feature importance is a model inspection technique that can be used for any fitted estimator when the data is tabular (see [scikit learn](https://scikit-learn.org/stable/modules/permutation_importance.html#permutation-importance) for more details). 
```

 The permutation importance can be calculated on the training set to show how much the model relies on each feature during training. However, it can also be calculated on the test data to show the ability of a feature to be useful to make predictions that generalize to the test set.

```{admonition} Resources
:class: tip
- [Gradient Tree Boosting with scikit learn](https://kirenz.github.io/regression/docs/gradientboosting.html)

- [Gradient Tree Boosting with XGBoost](https://kirenz.github.io/regression/docs/gradientboosting-xgboost.html#gradient-boosting-with-xgboost)

- [Scikit-learn developers: Permutation feature importance](https://scikit-learn.org/stable/modules/permutation_importance.html)
```