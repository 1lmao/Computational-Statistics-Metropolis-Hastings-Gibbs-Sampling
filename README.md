# Statistical Simulation & MCMC Assignment

### 1. Extreme Value Distribution

Consider the following probability distribution function:

> *f*(*x*) = (1 / *b*) exp[−(*x* − *a*) / *b*] exp{−exp[−(*x* − *a*) / *b*]},    *b* > 0.

This distribution is called Extreme Value distribution (EV(*a*, *b*)) with the location parameter *a* and the scale parameter *b*. This distribution has been used widely to model extreme events, for example, annual maximum rainfall. We are interested in generating random sample from the density with *a* = 2 and *b* = 1.

- **(a)** Use any method of your choice to generate a random sample of size 100 from the density. Plot the density histogram of the random sample with the true density superimposed. Also provide the empirical and the theoretical CDF and compare.
- **(b)** Using the random sample in (a), construct a MC for the location parameter *a* assuming the scale parameter *b* is known as 1. Plot the MC and the density histogram after burn-in. Give the mean, standard deviation, and 95% percentile interval for *a*. Discuss your findings.

---

### 2. Poisson Process Simulation

It is known that the distribution of waiting times between events in a Poisson process with intensity λ are Exp(λ). We would like to use this fact to generate random numbers from Poisson(λ). Generate events *X*<sub>*i*</sub> = ∑<sub>*j*=1</sub><sup>*i*</sup> *Y*<sub>*j*</sub>, *Y*<sub>*j*</sub> ~ Exp(λ) and then take *Z* = #{*X*<sub>*i*</sub> : *X*<sub>*i*</sub> ∈ [*l* − 1, *l*)}, *l* ≥ 1, as Poisson(λ) pseudo-rv's. Write a function to generate *N* such random numbers. Using your function generate *N* = 1000 such random numbers with λ = 1. Count the outcomes in the categories 0, 1, 2, ..., 10, 10+. Provide the density histogram and compare with the theoretical density. Discuss your findings.

- **(a)** Describe how you might do this using a resampling method.
- **(b)** Describe how you might do this using a kernel density estimation method.

For each method you used, describe your procedure in detail, write a MATLAB function, and provide results. Compare the results both graphically and numerically.

---

### 3. Gibbs Sampling

Consider random variables *X* and *Y* having the following conditional distributions:

> *f*(*x* | *y*) = *y* *e*<sup>−*xy*</sup>,    0 < *x* < 10
>
> *f*(*y* | *x*) = *x* *e*<sup>−*xy*</sup>,    0 < *y* < 10

Use Gibbs sampler to generate MC of size 1000 from the marginal distribution *f*(*x*). Use your own starting values and burn-in period. Estimate mean, variance, skewness, and kurtosis of the marginal distribution. After burn-in plot the MC and give the density histogram of the chain. Estimate the marginal pdf *f̂*(*x*) at *x* = 0.1, 1.8, 3.5, 9.2.

Repeat with different starting values and compare the results.
