# Final Report

**Author**: [Smit Lunagariya](https://smit-create.github.io/intro.html)

## GSoC 2020 Report: Improving and Extending stats module

This is the final report of the entire GSoC 2020 for the project titled as **Improving and Extending stats module** with [SymPy](https://sympy.org) as the organization. My mentors were [Gagandeep Singh](https://github.com/czgdp1807), [Francesco Bonazzi](https://github.com/Upabjojr) and [Jogi Miglani](https://github.com/jmig5776). The complete description of the project implementation and discussions of the entire program is available at [smit-create.github.io/gsoc_blogs](https://smit-create.github.io/gsoc_blogs/intro.html).

### About Me

I am Smit Lunagariya, a third-year undergraduate student majoring in Mathematics and Computing Engineering from the Indian Institute of Technology - BHU, Varanasi.


### Project Overview: Phase-wise short description

I divided the four phases to work on the specific topics of the Statistics that were supposed to be implemented during the GSoC.

1. **Community Bonding** - This phase included one of the easiest parts of adding the distributions such as Lomax and Bounded Pareto to `crv_types.py`. I also completed one of my open PR for sampling the Continuous Random Variables from external libraries.

2. **Phase 1** - This phase was majorly oriented towards completing the sampling for most of the SymPy random variables from the external libraries as well as focused on adding the stochastic processes such as Poisson, Wiener, and Gamma Processes.

3. **Phase 2** - This phase was focused on completing the support of Compound Distributions which we introduced in 2018 but were not supported completely. Also, many new symbolic classes were introduced during this phase which includes `ExpectationMatrix`, `VarianceMatrix`, `CrossCovarianceMatrix`, `Moment` and `CentralMoment`.

4. **Phase 3** - This phase continued some of the work from Phase 2 like extending the algorithm of Compound Distributions to handle more complex queries as well as added Matrix Distributions to `sympy.stats`. This phase also was focused on fixing some of the basic issues of `stats` as well as completing the sampling of `stats` from external libraries for all the random variables supported in `sympy.stats`.

### Pull Requests

This section describes the actual work done during the coding period in terms of merged pull requests.

#### Community Bonding

- [#18754](https://github.com/sympy/sympy/pull/18754): This PR completed the sampling of Continuous Random Variables of SymPy from external libraries such as `numpy`, `scipy` and `pymc3`.

- [#19273](https://github.com/sympy/sympy/pull/19273) : This PR added `BoundedPareto` and `Lomax` distributions under `crv_types.py`.

- [#19295](https://github.com/sympy/sympy/pull/19295) : This PR renamed the `doit` method in symbolic stats classes to `expand` in order to maintain the uniformity with the other sympy symbolic classes.

#### Phase 1

- [#19304](https://github.com/sympy/sympy/pull/19304) : This PR added a function `is_random`, which helps in checking whether the expression is random or not.

- [#19290](https://github.com/sympy/sympy/pull/19290) : This PR added the `doit` method in `Expectation` class as well as linked `E` or `expectation` with `Expectation.doit()`

- [#19342](https://github.com/sympy/sympy/pull/19342) : This PR completed one of the major aims of the project of sampling from external libraries. Sampling methods for Discrete and Finite random variables were completed in this PR.

- [#19387](https://github.com/sympy/sympy/pull/19387) : This PR added the stochastic processes which includes `PoissonProcess`, `WienerProcess` and `GammaProcess`. This was one of the challenging PR as designing and handling various queries was a difficult task.

- [#19500](https://github.com/sympy/sympy/pull/19500) : This PR introduced sampling from stochastic processes. The API was designed and implemented for sampling from the Discrete Markov chain which can be now easily extended for further processes.

- [#19459](https://github.com/sympy/sympy/pull/19459) : This PR fixes the issue of the incorrect results produced by `Sum.doit()` when used with the expressions containing Random Indexed Symbol.


#### Phase 2

- [#19529](https://github.com/sympy/sympy/pull/19529) : This PR added new symbolic classes of `ExpectationMatrix`, `VarianceMatrix` and `CrossCovarianceMatrix` for symbolic multivariate probability.

- [#19631](https://github.com/sympy/sympy/pull/19631) : This PR cleans up the code for Joint Random Variables and adds more tests to increase the code coverage of `joint_rv_types.py`. Moreover, it also adds `MultivariateNormal` and `MultivariateLaplace` Joint random variables which previously were not linked to their distribution class.

- [#19648](https://github.com/sympy/sympy/pull/19648): This PR added the support for Compound Distributions in `sympy.stats` and completes one of the major aim of the project. It also fixed a few of the old issues that were related to Compound Distributions.

- [#19724](https://github.com/sympy/sympy/pull/19724) : This PR added new symbolic classes of `Moment` and `CentralMoment`. This was added as a consequence of the discussion on one of the old issues for linking `moment` with `Moment` and `cmoment` with `CentralMoment`.

#### Phase 3

- [#19734](https://github.com/sympy/sympy/pull/19734) : In this PR, Matrix Distribution support was added to `sympy.stats` along with `MatrixGamma` Distribution.

- [#19795](https://github.com/sympy/sympy/pull/19795) : This PR adds more distributions to the Matrix Distribution and completes one of the stalled PR as it adds `MatrixNormal` and `Wishart` Distribution

- [#19808](https://github.com/sympy/sympy/pull/19808): This PR continues the Compound Distributions from the 2nd Phase by changing the algorithm of marginalization and solving the queries using recursion.

- [#19819](https://github.com/sympy/sympy/pull/19819) : This PR changes the return type of `P` and `E` with `evaluate=False`. This was done to maintain the uniform results across other modules of sympy and it was made to return its own symbolic object instead of unevaluated `Integral`.

- [#19848](https://github.com/sympy/sympy/pull/19848) : This PR was a result of one of the old issues for sampling from Joint random variables. The sampling framework for Joint Random variables was added in this PR.

- [#19857](https://github.com/sympy/sympy/pull/19857) : I got this idea to complete the sampling for newly added Matrix Distributions as with this PR, I completed the sampling framework for each sympy random variables type for sampling from the external libraries.

### Miscellaneous Work

This section contains some of my PRs related to miscellaneous issues like workflow improvement, or PRs for some other modules apart from `stats`.

- [#19826](https://github.com/sympy/sympy/pull/19826) : This PR adds a new type of Set under `matrices` and it was a result of the discussions on [#19795](https://github.com/sympy/sympy/pull/19795)

- [#19934](https://github.com/sympy/sympy/pull/19934) : This PR moved all the imports from the external libraries inside the functions where they were used instead of importing them at the top of the file.

- [#19975](https://github.com/sympy/sympy/pull/19975) : This PR updates the documentation of `stats` on the main website and also adds documentation for newly added classes and functions during the GSoC.

### Work In Progress

The following PRs are under the discussions and I am still updating it according to the discussions with the mentors.

- [#19957](https://github.com/sympy/sympy/pull/19957) : This PR changes the algorithm of `expectation` of Joint random variables. This is one of the important PR which adds support for `expectation` and `variance` for Joint random variables along with fixes in symbolic classes of `Variance` and `Covariance`.

- [#19886](https://github.com/sympy/sympy/pull/19886) : This PR adds the support of Mixture Distributions in `sympy.stats`. Currently, I have added the new framework for its support but it is still under the discussion if we can add its support with the help of existing classes

### Examples

This section consists of some of the examples for newly added and fixed features in `sympy.stats` during the GSoC.

#### Compound Distributions
The Compound Distributions became more robust and were able to handle the queries of `P`, `E`, `density`, etc.

```py
>>> from sympy import symbols
>>> from sympy.stats import density, E, Gamma, Poisson, Beta, Bernoulli, variance, cdf
>>> k, t, y = symbols('k t y', positive=True, real=True)
>>> G = Gamma('G', k, t)
>>> D = Poisson('P', G) # This forms a Negative Binomial Distribution
>>> density(D)(y).simplify()
t**y*(t + 1)**(-k - y)*gamma(k + y)/(gamma(k)*gamma(y + 1))
>>> E(D).simplify()
k*t

>>> X = Beta('X', 1, 2)
>>> Y = Bernoulli('Y', X)
>>> density(Y).dict
{0: 2/3, 1: 1/3}
>>> E(Y)
1/3
>>> variance(Y)
2/9
>>> cdf(Y)
{0: 2/3, 1: 1}
```

#### Stochatic Process: Poisson, Wiener and Gamma

The stochastic process framework was introduced in last year's GSoC by [Gagandeep Singh](https://github.com/czgdp1807). I have extended it further by adding few more processes to it. Some of the examples related to them are:

```py
>>> from sympy import Eq, symbols
>>> from sympy.stats import PoissonProcess, WienerProcess, GammaProcess, P, E, variance
>>> t, g, l = symbols('t g l', positive=True)
>>> X = PoissonProcess('X', 10)
>>> P(X(t) < 1)
exp(-10*t)
>>> X = PoissonProcess('X', 2)
>>> P(X(t) < 1)
exp(-2*t)
>>> P(X(3) < 1, Eq(X(1), 0))
exp(-4)
>>> X.state_space
Naturals0

>>> X = WienerProcess("X")
>>> P(X(t) < 3).simplify()
erf(3*sqrt(2)/(2*sqrt(t)))/2 + 1/2
>>> X.state_space
Reals

>>> X = GammaProcess("X", l, g)
>>> E(X(t))
g*t/l
>>> variance(X(t)).simplify()
g*t/l**2
>>> X.state_space
Interval(0, oo)
```

#### Extension of Symbolic classes of stats

The symbolic classes of `Expectation`, `Variance` and `Covariance` were supported intially but had a few issues. I have fixed them and added new symbolic classes for multivariate probability like `ExpectationMatrix`, `VarianceMatrix`, `CrossCovarianceMatrix` and also symbolic classes of `Moment`  and `CentralMoment`. Some examples related these classes are:

```py
>>> from sympy import symbols
>>> from sympy.stats import Expectation, Variance, Covariance, Normal, Moment, CentralMoment
>>> w, z = symbols('w, z')
>>> X = Normal('X', 2, 3)
>>> Y = Normal('Y', 3, 4)
>>> Expectation((X + Y)*(X - Y))
Expectation((X - Y)*(X + Y))
>>> Expectation((X + Y)*(X - Y)).expand()
Expectation(X**2) - Expectation(Y**2)
>>> Expectation((X + Y)*(X - Y)).expand().doit()
-12

>>> Variance(X + Y)
Variance(X + Y)
>>> Variance(X + Y).expand()
2*Covariance(X, Y) + Variance(X) + Variance(Y)

>>> Covariance(z*X + 3, w*Y + 4)
Covariance(w*Y + 4, z*X + 3)
>>> Covariance(z*X + 3, w*Y + 4).expand()
w*z*Covariance(X, Y)

>>> mu = symbols('mu', real=True)
>>> sigma = symbols('sigma', real=True, positive=True)
>>> X = Normal('X', mu, sigma)

>>> M = Moment(X, 4, 2)
>>> M.rewrite(Expectation)
Expectation((X - 2)**4)
>>> M.doit()
mu**4 - 8*mu**3 + 6*mu**2*sigma**2 + 24*mu**2 - 24*mu*sigma**2 - 32*mu + 3*sigma**4 + 24*sigma**2 + 16

>>> CM = CentralMoment(X, 6)
>>> CM.rewrite(Expectation)
Expectation((X - Expectation(X))**6)
>>> CM.doit().simplify()
15*sigma**6
```

Few examples of the symbolic multivariate probability classes:

```py
>>> from sympy.stats.rv import RandomMatrixSymbol
>>> from sympy.stats import Expectation, Variance, Covariance
>>> from sympy import MatrixSymbol, symbols
>>> j, k = symbols("j,k")
>>> A = MatrixSymbol("A", k, k)
>>> B = MatrixSymbol("B", k, k)
>>> X = RandomMatrixSymbol("X", k, 1)
>>> Y = RandomMatrixSymbol("Y", k, 1)
>>> Expectation(A*X + B*Y)
ExpectationMatrix(A*X + B*Y)
>>> Expectation(A*X + B*Y).expand()
A*ExpectationMatrix(X) + B*ExpectationMatrix(Y)

>>> Variance(A*B*X)
VarianceMatrix(A*B*X)
>>> Variance(A*B*X).expand()
A*B*VarianceMatrix(X)*B.T*A.T

>>> a = MatrixSymbol("a", k, 1)
>>> b = MatrixSymbol("b", k, 1)
>>> Covariance(A*X + a, B.T*Y + b)
CrossCovarianceMatrix(A*X + a, b + B.T*Y)
>>> Covariance(A*X + a, B.T*Y + b).expand()
A*CrossCovarianceMatrix(X, Y)*B
```

#### Matrix Distributions

Matrix Distributions were added during this GSoC following the same API as other `stats` distribution classes.

```py
>>> from sympy import MatrixSymbol
>>> from sympy.stats import Wishart, density
>>> W = Wishart('W', 5, [[1, 0], [0, 1]])
>>> X = MatrixSymbol('X', 2, 2)
>>> density(W)(X).doit()
exp(Trace(Matrix([
[-1/2,    0],
[   0, -1/2]])*X))*Determinant(X)/(24*pi)
>>> density(W)([[2, 1], [1, 2]]).doit()
exp(-2)/(8*pi)
```

#### Sampling from external libraries for all types of random variables

One of the important aims was to project to design and implement the sampling of SymPy random variables from external libraries like `scipy`, `numpy` and `pymc3`. This was completed during the GSoC resulting in fixing some of the old issues related to sampling.

```py
>>> from sympy.stats import *
>>> G = Gamma("G", 2, 7) # Continuous Random Variable
>>> next(sample(G, size=3)) # Samples by default from scipy
array([25.02851478,  9.28851461, 12.49382385])

>>> X = Poisson('P', 5) # Discrete Random Variable
>>> next(sample(X, size=4, library='pymc3')) # Samples from pymc3
array([3, 5, 5, 3])

>>> B = Binomial("B", 5, 0.4) # Finite Random Variable
>>> next(sample(B, size=(2, 2), library='numpy')) # Samples from numpy
array([[3, 3],
       [4, 2]])

>>> B = MultivariateBeta("B", [0.4, 5, 15]) # Joint Random Variable
>>> next(sample(B, size=5))
array([[1.58692726e-01, 2.30501631e-01, 6.10805643e-01],
      [1.07837386e-07, 2.74477711e-01, 7.25522181e-01],
      [2.47942734e-02, 3.82168743e-01, 5.93036984e-01],
      [1.29554971e-03, 3.35327136e-01, 6.63377315e-01],
      [2.70403663e-02, 1.82990118e-01, 7.89969516e-01]])

>>> W = Wishart('W', 5, [[1, 0], [0, 1]]) # Matrix Random Variable
>>> next(sample(W, size=2))
array([[[ 5.92473317, -3.78988114],
        [-3.78988114,  5.72223869]],

       [[ 1.04877709,  1.2991145 ],
        [ 1.2991145 ,  4.52413691]]])

```

### Future Work

The following PRs are open and are in their last stages for merging. Any interested student can take a look at them to extend my work in his/her GSoC project.

- [#19482](https://github.com/sympy/sympy/pull/19482) : This PR adds one of the important stochastic processes, Random Walks. This PR requires generalizing the queries for the `probability` and designing an algorithm to handle multiple queries. One can also refer to this [comment](https://github.com/sympy/sympy/pull/19482#issuecomment-654492258).

- [#19949](https://github.com/sympy/sympy/pull/19949) : This PR continues the work from last year's GSoC of [Gagandeep Singh](https://github.com/czgdp1807). This PR is added with the support of `Covariance` as a metric of assumption. This can be extended on the current framework by adding an algorithm for other dependence metrics.

### Conclusion

This Summer has been a great learning experience. I am grateful to my mentors, [Gagandeep Singh](https://github.com/czgdp1807), [Francesco Bonazzi](https://github.com/Upabjojr) and [Jogi Miglani](https://github.com/jmig5776) for always helping me with the new concepts, reviewing my PRs and providing quick responses.
