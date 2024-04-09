# Week 5


This blogs describes the week 5, the beginning week of the Phase 2. Phase 2 will be mostly focused on Compound Distributions which were stalled from 2018, and additions to Joint Distributions.

Some key highlights of this week are

## Discussions

* [Compound Distributions](https://github.com/sympy/sympy/issues/19332)
  * This issue comprises of the discussions on the implementation design and API for the Compound Distributions.

## PRs during this week

### Open PRs

* [WIP-Compound Distributions](https://github.com/sympy/sympy/pull/19648)
  * This PR is a prototype of the discussions in [#19332](https://github.com/sympy/sympy/issues/19332). This builds basic framework and I will add tests and documentation so that it becomes ready for review from the mentors.

* [Testing and cleaning up Joint Rvs](https://github.com/sympy/sympy/pull/19631)
  * This PR aims at cleaning Joint RVs and increasing the coverage of `joint_rv_types.py`. It also contains corrections in documentations, adding missing functions for `MultivariateNormalDistribution` and `MultivariateLaplaceDistribution` and few clean ups in `test_joint_rv.py`. The coverage has been increased to `98%`.

### Merged PRs

* [Added Poisson, Wiener and Gamma Process](https://github.com/sympy/sympy/pull/19387)
  * This was one of the most important aim of the project which added `Poisson Process`, `Wiener Process` and `Gamma Process` and makes me feel so happy to see it getting merged as this was the important pending work of the Phase 1. I hope to complete my project aims in the upcoming Phases too.
