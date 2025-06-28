# bayesian-ab-test-calculator
Simple Bayesian AB/n Test Calculator

It's a pleasure to introduce this calculator, which allows you to easily calculate results from your AB tests using a Bayesian approach.

I am taking into account two different approaches related to the way we count the number of conversions:

1. **Bernoulli‑Beta** &nbsp;→ Binary: a user converts (1) or no (0).
2. **Poisson‑Gamma** &nbsp;→ Event count (A user can interact many times with the same event).

You'll find:
* Comments and explanation.
* Code and visualizations
* An interactive calculator

**Why Monte Carlo?** Monte Carlo simulation is typically used because computing $P(\theta_B > \theta_A)$ analytically involves integrating the product of two Beta distributions. Monte Carlo sidesteps this by sampling from the posterior distributions and estimating the probability empirically, which has become the standard practice in Bayesian A/B testing.

**Warning:**

**Monte Carlo simulation uses random sampling**, so results naturally vary slightly each run. This demonstrates the implementation is working correctly. To reduce variance: increase sample size to 1M or set `np.random.seed(42)` for reproducibility.
