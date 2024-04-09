# Week 1

This blog discribes the first official implementation week of the program. One of the advantage of Community Bonding period, I experienced during this week was that it saves a lot of time of designing new APIs. Since, it was all decided earlier on the APIs in the previous week, it made easy to maintain the timeline and add significant features.

Some key highlights on this week's work are:

* [Added Poisson Process](https://github.com/sympy/sympy/pull/19387)
  * After completely the discussions on Poisson Process, I made a PR for implementing the plan. Initially few errors popped up in the API design, but was backed by another new design which was successfully implemented and satisfied almost all the requirement of the problems on Poisson Process. I made a prototype [PR #19387](https://github.com/sympy/sympy/pull/19387) which shows the plan of implementing Poisson Process. It still requires few methods to be added, but once the PR is approved by the mentors, I will go for adding the documentation and some important methods.

* [Sampling from external libraries](https://github.com/sympy/sympy/pull/19342)
  * This was one of the most important work of this week. Sampling from external libraries was also a GSoC 2019 topic, but was not completed. This PR wraps up the complete sampling of sympy random variables from external libraries with much easier and compact implementation that avoids adding ad-hoc methods to corresponding classes. This PR has been approved by the mentors and is ready to be merged.

## Merged PRs

* [Fixes in Symbolic Expectation](https://github.com/sympy/sympy/pull/19290)
  * This PR was aimed at making `Expectation` equivalent to `Integral` and `E` equivalent to `integrate`. This was the outcome of the discussion in [#19267](https://github.com/sympy/sympy/issues/19267). `doit` method was added to `Expectation`, and made `E` to call this `doit` as similar to `integrate`. This was finally approved and merged by the mentors.
