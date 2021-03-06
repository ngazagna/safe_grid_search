# Safe Grid Search with Optimal Complexity.

This package implements a safe grid search strategy for hyperparameter tunning. We use a coordinate descent algorithm to solve the optimization algorithms (though the choice of coordinate descent is "arbitrary" here: indeed any other optimization solver can be used as soon as it can output a duality gap). The approximation path algorithms and their complexity are based only on the duality gap computation to quantify the optimality of a vector at a given regularization parameter.

See the paper https://arxiv.org/abs/1810.05471 for more details.

## Installation & Requirements

We first need to install the optimization solvers ``safegridoptim`` and the compilation proceed as follows:

```
$ pip install -e .
```

This package has the following requirements:

- [numpy](http://numpy.org)
- [scipy](http://scipy.org)
- [scikit-learn](http://scikit-learn.org)
- [cython](http://cython.org/)

We recommend to install or update anaconda (at least version 0.16.1).


## Reproducibility

- Figure 1 is generated by plot_lars.py (time<1s.)
- Figure 2 is generated by plot_bounds.py (time<1s.)
- Figure 3 (a) is generated by bench_safe_enet_path.py (time<3s. - ``make_regression``(100, 500))
- Figure 3 (b) is generated by bench_safe_logreg_path.py (time<60s. - ``make_classification``(100, 500))
- Figure 4 (a) and (b) are generated by plot_confidence_validation.py (time<2s. for a; time<2mn. for b;)
- Figure 5 (appendix) is generated by plot_autoconcordance.py


