# Week 10

This blogs describes the 10<sup>th</sup> week of the program. Some of the highlights of this week are:

## Merged PRs

* [Added sampling from Matrix Distributions](https://github.com/sympy/sympy/pull/19857)
  * This PR adds the support of sampling for newly added matrix distributions from external libraries.

* [Added sampling for Joint Random Variables](https://github.com/sympy/sympy/pull/19848)
  * This PR closes one of the issue of sampling from Joint Distributions. Also, adding sampling support from few frequently used Joint Distributions.

* [Change return type of `P` and `E` with `evaluate=False`](https://github.com/sympy/sympy/pull/19819)
  * This PR changes the return type of `P` and `E` with `evaluate=False`. They are made to return their respective classes with `evaluate=False` instead of unevaluated `Integral` or `Sum`.

* [Allow more than one RV in compound distribution](https://github.com/sympy/sympy/pull/19808)
  * This PR changes the marginalisation algorithm of the Compound Distributions and allows to handle more than one Random Variables as parameters.

* [Added Matrix Normal and Wishart Distribution](https://github.com/sympy/sympy/pull/19795)
  * This PR adds Matrix Normal Distribution and Wishart Distributions and closes one of the stalled PR of [Kumar Ritesh](https://github.com/ritesh99rakesh).

This week I am working to add the support for Mixture distributions. I would try to complete it by this week and start to work on the Assumptions of random variables.
