# Week 2

I will be describing the second week of the project in this blog. This week can be considered as one the most important week as it consists of completing one of the important aim of the project.
I will highlight some of the main discussions and the completed work during this week.

Some key highlights on this week's work:

* [Sampling from Stochatic Process-Discussion](https://github.com/sympy/sympy/issues/19454)
  * As the sampling of Continuous, Discrete and Finite random variables was finalized and completed from the external libraries, [Gagandeep Singh](https://github.com/czgdp1807) had a great idea of implementing sampling from the Stochatic Processes and their simulations. So, to finalize its API and the framework of implementation, this issue was opened for the discussion.

* [Random Walks-Discussion](https://github.com/sympy/sympy/issues/19428)
  * After almost completing the discussion on the API of the Poisson and its related processes, we moved on for implementing one of the important Stochatic Process-Random Walk.

* [Error in Sum.doit with Random Indexed Symbol-Issue](https://github.com/sympy/sympy/issues/19456)
  * While trying to design the API of Random Walks, I came a across a bug with the Random Indexed Symbol. The error was due to the method `free_symbols` of class Random Indexed Symbol. I soon investigated into it and opened a PR to fix it.

## PRs during this week

* [Merged- Sampling from external libraries](https://github.com/sympy/sympy/pull/19342)
  * Sampling from external libraries was one of the main aim of this project and I am happy to complete it during this week and getting it merged. This PR also fixed a number of issues related to the sampling which were opened from a long time.

* [Merged- Add a test of an issue](https://github.com/sympy/sympy/pull/19452)
  * While going through all the issues of the `stats`, I found them many of them were already fixed and can be closed, this PR added a test case to close the fixed issue. Also, during this week I closed many of the feature requesting issues of `stats` that were fixed.

* [Open- Fixes RandomIndexedSymbol issue](https://github.com/sympy/sympy/pull/19459)
  * This is the PR to fix [#19456](https://github.com/sympy/sympy/issues/19456). It is almost completed and ready for merging.

* [Open- Adding Poisson Process](https://github.com/sympy/sympy/pull/19387)
  * This is the PR for adding Poisson Process. I had got an approval for its API from the mentors, but to make the framework more generic for the Counting Processes like Poisson, Wiener and Gamma Process, it was suggested by [Gagandeep Singh](https://github.com/czgdp1807) to implement a class of Counting Process similar to current API, and make it a superclass of Poisson, Wiener and Gamma Processes.
