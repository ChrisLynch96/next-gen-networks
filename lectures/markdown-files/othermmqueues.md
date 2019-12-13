# Other M/M... queues

Number of other queuing systems similar to M/M/1

* M/M/1/N: there is now a finite buffer (System capacity = N)
* M/M/m: m servers instead of one
* M/M/$\infty$: infinite number of servers
* M/M/m/m: m servers without queuing

## M/M/1/N queue

* Poisson arrival process
* Exponential service
* a single server
* Finite capacity of N customers in the system

### Markov chain model

Local balance equation: $P_n = (\frac{\lambda{}}{\mu})^nP_0, 0 <= n <= N$

$P_n = \frac{(1-p)p^n}{1-p^{N+1}}, 0 <= n <= N$

$\bar{n} = E[n] = \sum_{n=0}^{N}nP_n = \frac{p}{1-p} - \frac{(N + 1)p^{N + 1}}{1-p^{N + 1}}$

## Blocking probability

* Blocking probability is an important performance measure for systems with infinite capacity.

* The blocking probability is the probability that an arriving customer will find the system full.
  * Blocking probability: $P_n$
  * Rate of rejected customer: $\lambda{}P_n$

## M/M/$\infty$

Infinite number of servers

Every arriving customer is put into service

Only service time is considered

$P_n = (\frac{\lambda}{\mu})^n\frac{P_0}{n!} = (\frac{\lambda}{\mu})^n\frac{e^{}\frac{-\lambda}{\mu}}{n!}, n=0,1,2...$

Expected number in the system is N = $\frac{\lambda}{\mu}$

Average Delay per customer:

$T = \frac{N}{\lambda} = \frac{1}{\mu}$

i.e how long it takes to serve a customer

## M/M/m queue

Identical to the M/M//1 queue except that there are m servers

Arriving customers are routed to any available server, if none are available the customer joins the single queue

![](./markdown-files/images/MMm-queue.png)

### Probability of queuing

"Erlang C" Formula

$P_Q = \frac{(mp)^m}{m!(1-p)}P_0 = (\frac{1}{m!})(\frac{\lambda}{\mu})^m\frac{1}{(1-p)}p_0$

$p = \frac{\lambda}{m\mu}$ for M/M/m queue

P_0 is defined further down

### M/M/m expected number in the queue

The expected number in the queue but not in service is...

$N_Q = P_Q\frac{p}{(1-p)}$

Expected time in the queue:

$W = \frac{N_Q}{\lambda} = \frac{pP_Q}{\lambda{}(1 - p)} = \frac{P_Q}{m\mu - \lambda}$

Expected delay per customer (queuing and waiting):

T = \frac{1}{\mu} + W = \frac{1}{\mu} + \frac{P_Q}{m\mu - \lambda}

Expected number in the system:

$N = \lambda{}T = \frac{\lambda}{\mu} + \frac{\lambda{}P_Q}{m\mu - lambda} = mp + \frac{pP_Q}{1 - p}$

## M/M/m/m queue

Also known as the m server loss system

No queueing allowed, the last m denotes the number of permitted customers.

### Blocking probability

$P_m = (\frac{\lambda}{\mu})^m\frac{P_0}{m!} = \frac{(\frac{\lambda}{\mu})^m\frac{1}{m!}}{}$

fuck the notes I'll finish these later

## Acronyms
