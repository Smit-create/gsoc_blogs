# Week 4

This blog provides the brief description of the last week i.e week 4 of the Phase 1. Some of the key highlights on the discussions and the implementation during this week are described below:

## Discussions and Updates on Open PRs

* [Open PR-Added Poisson, Wiener and Gamma Process](https://github.com/sympy/sympy/pull/19387)
  * This PR contains the implementation of three processes: Poisson, Wiener and Gamma Process. The previous implementation of the PR failed at few queries and so, it required coming up with a more robust algorithm. I have updated the PR with a new approach and is ready for testing. I will further update the PR as per mentors suggestion to improve the implementation and the scope of the classes.

* [Open PR-Added symbolic Expectation, Variance and CrossCovariance matrix](https://github.com/sympy/sympy/pull/19529)
  * This PR implements the idea of [Francesco Bonazzi](https://github.com/Upabjojr) of adding symbolic classes of Multivariate Expectation, Variance and CrossCovariance Matrices. This PR also completes the Draft shared by [Francesco Bonazzi](https://github.com/Upabjojr) in [#19299](https://github.com/sympy/sympy/pull/19299). I have added all the three classes and their respective tests and is currently tested by the mentors.

* [Merged-Added Sampling of Stochastic Process(DTMC)](https://github.com/sympy/sympy/pull/19500)
  * This PR completes the idea of [Gagandeep Singh](https://github.com/czgdp1807) of adding sampling for the stochastic processes. This is initially implemented for DTMC and will be extended further after adding more of such stochastic processes.

With the end of this week, it completes the official first month of the program. I learnt a lot during this one month and gained many important things from my mentors. I would also be thankful to my mentors for their constant guidance and support. Further, I also plan to complete the left over work of this month as soon as possible before beginning with the second month of the official coding period.
