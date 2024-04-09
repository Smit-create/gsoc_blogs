# Week 3

This blog provides the brief overview of the week 3 of the Phase 1. Some of the key highlights on the discussions and the implementation during this week are described below.

## Discussions

* [Sampling from Stochatic Process-Discussion](https://github.com/sympy/sympy/issues/19454)
  * This issue includes the examples of rough implementation with the plots to help visualizing the stochastic processes. The API for the same is almost finalized and ready to be implemented.

## PRs during this week

* [Open-Sampling of Stochastic Process](https://github.com/sympy/sympy/pull/19500)
  * This PR implements the idea of sampling from the stochastic processes as discussed in [#19454](https://github.com/sympy/sympy/issues/19454)

* [Draft-Random walks Prototype](https://github.com/sympy/sympy/pull/19482)
  * This is a Draft PR to show how the Random Walks can be implemented. The work is in progress and the final implementation will be done in a new PR once the Draft gets the approval from the mentors.

* [Open-Added Poisson, Wiener and Gamma Process](https://github.com/sympy/sympy/pull/19387)
  * This PR is almost completed and currently it is being tested by the mentors. It PR contains the implementation of Counting Process, Poisson Process, Wiener Process and Gamma Process along with their tests.

* [Merged-Fixes Sum.doit() with Randomindexed symbol](https://github.com/sympy/sympy/pull/19459)
  * This PR fixed the issue of `free_symbols` method in the class `RandomIndexedSymbol`.
