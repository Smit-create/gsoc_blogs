# Week 7
This blog describes the 7<sup>th</sup> week of the program and the 3<sup>rd</sup> week of Phase 2. Some of the key highlights on the discussions and the implementations during this week are:

## Discussions

* [Matrix Distributions](https://github.com/sympy/sympy/issues/19723)
  * This issues contains the discussions for adding the matrix distributions which are not possible to implement along with the joint distributions.

## Open PRs

* [MatrixGamma Distribution](https://github.com/sympy/sympy/pull/19734)
  * This is a prototype PR for showing the Matrix Distribution additions. However, this needs to be changed and will be implemented in a new file as suggested by [Gagandeep Singh](https://github.com/czgdp1807).

* [Add symbolic Moment and CentralMoment](https://github.com/sympy/sympy/pull/19724)
  * This PR fixes one of the old issue for adding symbolic classes for `Moment` and `CentralMoment`. This PR also links `moment` with `Moment.doit()` and `cmoment` with `CentralMoment.doit()`.

## Merged PRs

* [Compound Distributions](https://github.com/sympy/sympy/pull/19648)
  * Adding support for Compound Distributions was one of the main aim of the project as well as of the Phase 2 as it was stalled from 2018. It now has its own Probability Space and is implemented in a new file which was previously mixed up with Joint Rvs.

* [Add doit in symbolic Probability](https://github.com/sympy/sympy/pull/19696)
  * This PR adds `doit` method in symbolic Probability. This also links `P` or `probability` with `Probability.doit()`. Hence, this forms the uniformity with `P` linked to `Probability.doit()` and `E` linked to `Expectation.doit()`.
