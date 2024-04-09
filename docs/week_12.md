# Week 12

This is the final blog of the official program highlighting the final week. Some of the key highlights were:

## Open PRs

* [Adding Mixture Distribution](https://github.com/sympy/sympy/pull/19886)
  * The PR allows creating Mixture Distribution in `sympy.stats`. This PR is under discussion regarding the implementation notes and its API.

* [Assumptions of Dependence of Rvs](https://github.com/sympy/sympy/pull/19949)
  * This PR continues the work of [Gagandeep Singh](https://github.com/czgdp1807) for supporting Assumptions of Dependence between the random variables. This has intially been implemented with `Covariance` as the metric for assumptions.

* [Handle Joint Rvs Expectation](https://github.com/sympy/sympy/pull/19957)
  * This PR adds the new algorithm to calculate the `Expectation` of random Variables containing the Joint Random Symbol. The also fixes its `Variance` Computing as it is dependent on the `Expectation`. Moreover, this also adds `doit` method in symbolic `Variance` and `Covariance` classes and links `variance` and `covariance` functions to their respective classes.

## Merged PRs

* [Move external libraries import inside functions](https://github.com/sympy/sympy/pull/19934)
  * This PR moved all the imports of external libraries inside the functions in which they are used.

* [Fix state space of Wiener Process](https://github.com/sympy/sympy/pull/19926)
  * This PR fixed a small bug related to the state space of `WienerProcess`.

By the end of this week, it completes the Google Summer of Code and I am really thankful to the Community and the mentors for always helping and supporting me. Further, as suggested by the mentors, I would now focus on testing ang fixing the issues to make `stats` more robust.
