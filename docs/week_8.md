# Week 8


This blog provides the brief description of last week of the second Phase i.e. week 8.
Some of the key highlights of this week are:

## Open PRs

* [Added Matrix Normal and Wishart Distribution](https://github.com/sympy/sympy/pull/19795)
  * This PR adds the two matrix distributions. Framework for Matrix Distributions was added to `sympy.stats` during this week. There was an attempt in last year's GSoC by [Kumar Ritesh](https://github.com/ritesh99rakesh) to add Wishart Distribution in his [PR#17204](https://github.com/sympy/sympy/pull/17204) but was not completed. This PR also closes it and completes his left over work.

## Merged PRs

* [Add symbolic Moment and CentralMoment](https://github.com/sympy/sympy/pull/19724)
  * This PR added symbolic classes of `Moment` and `CentralMoment` in `sympy.stats`.

* [Add MatrixGamma Distribution](https://github.com/sympy/sympy/pull/19734)
  * This PR introduces Matrix Distributions support in `sympy.stats`. It added the framework for adding more distributions without changing the existing API of `stats`. It also allows for adding and extending more matrix distributions similar to other distributions.

With the end of this week, it completes the official two months of the program. This month successfully completes the targeted aims of the Phase 2 within the time bounds. I would also thank [Gagandeep Singh](https://github.com/czgdp1807) and [Francesco Bonazzi](https://github.com/Upabjojr) for their support and the quick responses on the discussions and PRs, and helping me out with new things to learn.
