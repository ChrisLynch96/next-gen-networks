# M/M/1 queue

Poisson assumptions for the arrival of customers to a queue make the analysis easily managed.

M/M/1 is also called Kendall's notation

* M: Poisson arrivals
* M: Exponential service times
* 1: one server

## Little's law

Little's law: The expected number in the system (queue) is the product of the arrival rate and the average time spent in the system.

$E[n] = \lambda{}E[\gamma{}]$

## M/M/1 model

* single server system
* Arrival according to Poisson process of rate $\lambda{}$
* Inter-arrival times exponential RVs
* Service times are exponential RVs with mean 1/$\mu$
* infinite buffers

![](markdown-files/images/MM1-model.png)

## Markov Chain

A Markov chain is a mathematical system that experiences transitions from one state to another according to certain probabilistic rules.

Due to the memoryless property of exponential RVs, Number of customers in the system can be expressed as a continuous Markov chain.

* States represent the number of customers in the queuing system.

### probability mass function

Let $p = \lambda{}/\mu < 1$ called utilization

To determine the pmf for the number if customers currently in the system

* Let $p_n$ denote the probability that customers are currently in the system.

$p_0 = (1-p)$

$p_n = p^np_0 = p^n(1-p)$

## Averages

Average number of customers in the system

$E[n] = \sum_{j = 0}^{\infty} jp_j = \frac{p}{1-p}$

Average delay in the system (Use Little's law)

$E[\gamma] = \frac{1}{\lambda}\frac{p}{1-p} = \frac{1}{\mu{} - \lambda{}}$

Average waiting time in the system

$E[\gamma_Q] = E[\gamma] - E[s] = E[\gamma] - \frac{1}{\mu} = \frac{1}{\mu}\frac{p}{1 - p}$

Average number of customers in the queue (use Little's law)

$E[n_q] = \lambda{}E[\gamma_Q] = \frac{p^2}{1 - p}$

## Acronyms

RV: Random Variable
pmf: probability mass function
