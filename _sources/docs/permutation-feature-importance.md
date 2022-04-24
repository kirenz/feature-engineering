(section-permutation-feature-importance)=
# Permutation feature importance

Permutation feature importance overcomes limitations of the impurity-based feature importance ([scikit learn](https://scikit-learn.org/stable/auto_examples/ensemble/plot_forest_importances.html)): 
  - they do not have a bias toward high-cardinality features
  - they can be computed on a left-out test set.

```{note}
It is a model inspection technique that can be used for any fitted estimator when the data is tabular (see [scikit learn](https://scikit-learn.org/stable/modules/permutation_importance.html#permutation-importance) for more details). 
```

The permutation feature importance is defined to be the decrease in a model score when a single feature value is randomly shuffled. This procedure breaks the relationship between the feature and the target, thus the drop in the model score is indicative of how much the model depends on the feature. 

This technique benefits from being model agnostic and can be calculated many times with different permutations of the feature. The permutation importance is calculated on the training set to show how much the model relies on each feature during training.


```{admonition} Resources
:class: tip
- [Gradient Boosting with scikit learn](https://kirenz.github.io/regression/docs/gradientboosting.html)

- [Gradient Boosting with XGBoost]()

- [Scikit-learn developers: Permutation feature importance](https://scikit-learn.org/stable/modules/permutation_importance.html)
```