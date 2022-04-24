(section-feature-selection-overview)=
# Overview

Content: importance based feature selection; Forward selection and backward selection.

```{note}
Feature selection  is the process of selecting a subset of relevant features (variables, predictors) for our model. 
```

Supervised feature selection (also known as variable selection, attribute selection, variable subset selection and model subset selection) methods fall into three general classes {cite:p}`Kuhn2019`: 

1. Embedded (or implicit) methods
1. Filter methods
1. Wrapper methods

**Embedded methods** perform feature selection during the modeling process (like regularization models or tree based models). 

**Filter methods** conduct an analysis of the predictors to determine which are important and then only provide these to the model. E.g. based on statistical significance, correlation coefficent scores or feature importance based on magnitude of coefficients.

**Wrapper methods** use iterative search procedures that repeatedly supply predictor subsets to the model and then use the resulting model performance estimate to guide the selection of the next subset to evaluate. Typical performance measures are mean squared error, Mallow's $C_P$, Akaike information criterion (AIC), Bayesian information criterion (BIC) (also called Schwarz information criterion SIC, SBC, SBIC) and adjusted $R^2$.

An example of [greedy](https://en.wikipedia.org/wiki/Greedy_algorithm) wrapper methods are forward and backward selection:

- Forward selection: That is, we start with 0 features and choose the best single feature with the highest score. The procedure is repeated until we reach the desired number of selected features.

- Backward selection: start with all the features and choose features to remove one by one. 

Examples of non-greedy wrapper methods are [genetic algorithms (GA)](http://www.feat.engineering/genetic-algorithms.html) and [simulated annealing (SA)](http://www.feat.engineering/simulated-annealing.html). 

---

In the following Python notebook, we cover these methods to select features for a model:

- Embedded method: Lasso regression (L1 regularization)

- Filter method: Based on coefficient importance.

- Wrapper methods: Forward and backward selection.

```{admonition} Resources
:class: tip
- [Python notebook: feature selection methods](https://kirenz.github.io/regression/docs/feature-selection.html)
- [Download slides](https://drive.google.com/file/d/154JFUOqukNgZThS_ql-ptATY4KEP3edR/view?usp=sharing)

- Literature: [Kuhn, M. & Johnson, K. (2019): Feature Engineering and Selection: A Practical Approach for Predictive Models.](http://www.feat.engineering/selection.html)
```