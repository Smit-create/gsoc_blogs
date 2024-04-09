# Phase 1 (Highlights)

With this blog it completes the awesome month of statistical learning and coding, and the official Phase 1 of the Google Summer of Code-2020.

I will try to highlight some notable additions to `stats` during this month.

## Merged PRs

* [#18754](https://github.com/sympy/sympy/pull/18754)
   * Added Sampling methods of Continuous Random Variables from external libraries.

* [#19273](https://github.com/sympy/sympy/pull/19273)
   * Added Lomax and Bounded Pareto Distributions(CRV types).

* [#19290](https://github.com/sympy/sympy/pull/19290)
   * Fixes Symbolic `Expectation` and its `doit` method.

* [#19295](https://github.com/sympy/sympy/pull/19295)
   * Rename `doit` to `expand` in Symbolic `stats`.

* [#19304](https://github.com/sympy/sympy/pull/19304)
   * Added `is_random` to check for random expressions.

* [#19342](https://github.com/sympy/sympy/pull/19342)
   * Completes sampling from external libraries for CRV, FRV and DRV.

* [#19452](https://github.com/sympy/sympy/pull/19452)
   * Added a test for a fixed issue of `stats`.

* [#19459](https://github.com/sympy/sympy/pull/19459)
   * Fixes `Sum.doit()` for `RandomIndexedSymbol`.

* [#19500](https://github.com/sympy/sympy/pull/19500)
   * Added support for Sampling from Stochatic Processes.

* [#19529](https://github.com/sympy/sympy/pull/19529)
   * Added Expectation, Variance and CrossCovariance Matrices.

## Open PRs

* [#19387](https://github.com/sympy/sympy/pull/19387)
   * Added Poisson, Wiener and Gamma Process.

With the end of the official Phase 1, I would like to thank my mentors for their constant support and guidance and look forward for significant additions to `stats` during the upcoming month and begin with the Phase 2 of program.
