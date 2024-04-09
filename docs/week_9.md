# Week 9

This blogs describes the week 9, the beginning week of the final phase. This week, I continued to work on the extension of Compound Distributions as well as completing the Matrix Distributions. Some of the highlights of this week are:

## Open PRs

* [Change return type of `P` and `E` with evaluate=False](https://github.com/sympy/sympy/pull/19819)
  * This PR aims at changing the return type of `P`, `E` and `density` with `evaluate=False`. Currently, they return unevaluated `Integral` or `Sum` but this needs be changed to return their respective symbolic classes.

* [Allowing more than one RV in Compound Distributions](https://github.com/sympy/sympy/pull/19808)
  * This PR is an extension of [PR#19648](https://github.com/sympy/sympy/pull/19648) to change the marginalisation algorithm and handle more than one random variables in Compound Distributions.

* [Added Wishart and MatrixNormal Distributions](https://github.com/sympy/sympy/pull/19795)
  * This PR was completed last week but was stalled because SymPy didn't have any `Set` class to represent the set of matrices. However, I opened a new PR which added the required `Set` and this is now ready for merging.

## Merged PRs

* [Added MatrixSet](https://github.com/sympy/sympy/pull/19826)
  * This PR added a new set class to represent the set of matrices over a given set. This was added as a result of [PR#19795](https://github.com/sympy/sympy/pull/19795)
