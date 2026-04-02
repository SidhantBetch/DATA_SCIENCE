# Probability Distribution
Probabiity distributions describe how the probabilities of different outcomes are distributed over the sample space of a random variable.

## Probability Distribution divided into two parts:
1. Discrete Probability Distributions
   - Deals with countable values (0, 1, 2, 3…)
   - Probabilities are assigned to each value

    Examples:  
        Bernoulli Distribution  
        Binomial Distribution  
        Poisson Distribution  
   
2. Continuous Probability Distributions
   - Deals with continuous values (infinite possibilities)
   - Uses probability density instead of exact probability

    Examples:
        Normal (Gaussian) Distribution  
        Uniform Distribution  
        Exponential Distribution  

# Probability Distribution Functions
A probability distribution is the mathematical function that gives the probabilities of occurrence of different posssible outcomes for an experiment.

## Probability Density Function(PDF)
PDF describes the density of probability at a given point.
(It does NOT give probability directly.)

$𝑓 ( 𝑥 ) $

👉 To find probability, we use area:

$𝑃 (𝑎≤𝑋≤𝑏) = \int_𝑎^𝑏 𝑓(𝑥)\,𝑑x$

## Probability Mass Function(PMF)
PMF gives the probability that a discrete random variable takes a specific value.

$𝑃 ( 𝑋 = 𝑥 ) $

##✅ Example:
If you roll a dice:

$𝑃 ( 𝑋 = 3 ) = \frac{1}{6}$
	​
## Cumulative Density Function(CDF)
CDF gives the probability that a random variable is less than or equal to a value.

$ 𝐹 (𝑥) = 𝑃(𝑋≤𝑥)
