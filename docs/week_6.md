# Week 6


This blog describes the 6<sup>th</sup> week of the official program and the 2<sup>nd</sup> week of Phase 2. By the end of this week, Compound Distributions framework is ready as targeted and I would now focus on the Joint Distributions in the upcoming weeks of this Phase.

Some of the key highlights on this week's discussions and PRs.

## Discussions

* Adding `doit` method in symbolic `Probability`
  * This discussion was held on gitter and was decided to make the stats more consistent by linking to `P` to `Probability` as it was done with `E` by linking it to `Expectation.doit()`. This will make `stats` module uniform with other modules of sympy.

* Order Statistics and Range Statistics
  * This was the new idea proposed by [Francesco Bonazzi](https://github.com/Upabjojr) on gitter. This will need further discussions on its API and implementation.

## Open PRs

* [Added doit in symbolic Probability](https://github.com/sympy/sympy/pull/19696)
  * This PR is the outcome of the discussion on gitter for adding a `doit` method in symbolic `Probability` and linking it to `P`.

* [Compound Distributions](https://github.com/sympy/sympy/pull/19648)
  * This PR completes the idea of supporting Compound Distributions. This was stalled from 2018 and the current implementation works good in most of the cases. This PR is ready for the review and from the mentors and also fixes some of the old issues related to Compound Distributions.

## Merged PRs

* [Testing and cleaning up Joint Rvs](https://github.com/sympy/sympy/pull/19631)
  * This PR aimed at testing and cleaning `joint_rv_types.py`. The coverage of this file was increased to `98%` by adding new tests and documentation as well as some missing functions.

This week was mostly Compound Distributions focused as it was an important addition. I also looked into many of the past issues related to `stats` to fix them if they were related to Compound Distributions or if I could fix them up. I also closed a few issues that were either fixed or requesting already added feature. The upcoming two weeks will be focused on additions to Joint Distributions as it supports very few distributions at present and needs attention to make it equivalent to other `stats` Distributions.
