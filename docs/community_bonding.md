# Community Bonding Period

This is the first official blog associated with GSoC 2020. I will be sharing the experience of the Community Bonding Period and work during this period after selection.

After the results were announced one of the key learning was to set-up my blog where I will provide the weekly reports on the progress of the project.

Considering this period as the key time for having discussions on the project with the mentors, I discussed my ideas further with [Gagandeep Singh](https://github.com/czgdp1807), [Francesco Bonazzi](https://github.com/Upabjojr) and [Jogi Miglani](https://github.com/jmig5776). This was the first time I met [Francesco Bonazzi](https://github.com/Upabjojr) on gitter, and was wonderful learning from him.

Some key work on the project during this period was the issues I opened for discussions of the API and the examples of the Stochatic Processes, `doit` method in Symbolic Probability, Compound Distributions and Mixture Distributions.

Some highlights on the discussions are:
* [Compound Distributions](https://github.com/sympy/sympy/issues/19332)
  * Integrate doesn't evaluate completely for complicated expressions and might be unreliable if we add Compound Distributions by definiton.
* [Stochatic Processes](https://github.com/sympy/sympy/issues/19274)
  * This followed a nice pattern of designing API for Poisson Process, first discuss the examples using fake API, observe the pattern from fake APIs and then propose a strong API covering most of the examples. This was the key learning in this discussion from [Gagandeep Singh](https://github.com/czgdp1807)
* [doit method in Symbolic Expectation](https://github.com/sympy/sympy/issues/19267)
  * The discussion is still in the progress. It aims at making Symbolic stats classes equivalent to `Integrate` and their respective functions equivalent to `integrate`. The intial outcome is to rename the present `doit` method to `expand` as it performed expansion of expression rather than evaluating.

Few Pull requests during the period are:
* [Renaming doit to expand](https://github.com/sympy/sympy/pull/19295)
  * The `doit` method of Symbolic stats was renamed to `expand`.
* [Lomax and Bounded Pareto Distributions](https://github.com/sympy/sympy/pull/19273)
  * Added two continuous distributions.
* [Sampling of CRV](https://github.com/sympy/sympy/pull/18754)
  * One of the main aim of the project was to design a sampling API for sampling of random variables from external libraries.

In the conclusion, it can be said that the Community Bonding Period was one the peak time of the project discussion on designing the interface. This saves time during the implementation period. And I personally had gained many things from the mentors [Gagandeep Singh](https://github.com/czgdp1807), [Francesco Bonazzi](https://github.com/Upabjojr) and [Jogi Miglani](https://github.com/jmig5776).
Thanks and let's move to the implementation of this existing project.
