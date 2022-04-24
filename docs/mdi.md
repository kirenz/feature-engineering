(section-mean-decrease)=
# Mean decrease in impurity (MDI)

*The following content is based on tutorials provided by the scikit-learn developers.*

Mean decrease in impurity (MDI) is a measure of feature importance for decision tree models. They are computed as the mean and standard deviation of accumulation of the impurity decrease within each tree.

Note that impurity-based importances are computed on training set statistics and therefore do not reflect the ability of feature to be useful to make predictions that generalize to the test set (when the model has enough capacity). Also note that impurity-based importances are biased towards high cardinality features (i.e., features with many unique values). 

As an alternative to MDI, you may want to use ![](permutation-feature-importance.md), which can be computed on a held out test set. 

```{admonition} Resources
:class: tip
- [Gradient Tree Boosting with scikit learn](https://kirenz.github.io/regression/docs/gradientboosting.html)

- [Gradient Tree Boosting with XGBoost](https://kirenz.github.io/regression/docs/gradientboosting-xgboost.html#gradient-boosting-with-xgboost)

- [Scikit-learn developers: Permutation Importance vs Random Forest Feature Importance (MDI)](https://scikit-learn.org/stable/auto_examples/inspection/plot_permutation_importance.html#)
```
