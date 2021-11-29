# 排队系统第一章

# Mathematical Methods to Study Classical Queuing Systems

## what describes for queuing system 

1.input of customers (requests, messages, calls, etc.) 客户的输入，请求，信息，呼叫etc

2.number and types of servers;服务的数量和类型

3.buffer size, 缓冲区大小，

4.service time of customers;服务时间of 客户

5.queue discipline. 队列顺序

### A/B/n/m

Symbol of n:  specifies the number of identical parallel servers (平行服务器的数量)

Symbol of m: for russia is means number of please to wait in buffer . for english is the maximum  number of customers

​           if m = ∞  then the fourth position in the queuing system description is usually omitted.（那么排队系统描述中的第四个位置通常会被省略掉）

Symbol A describes the incoming flow of customers

symbol B characterizes the service time distribution

## Input Flow, Service Tim



Customers arrive at the queue at random time points $t_{1}, t_{2}, \ldots, t_{n}, \ldots$ Let $\tau_{k}=t_k− t_{k−1}$ be the length of the time interval between the arrivals of the (k − 1)th and kth customers, k ≥ 1 (t0 is supposed to be 0) and xt be the number of moments tk lying on the time axis to the left of point t, t ≥ 0.

客户在随机时间点t1 - tn 到达队列让τk =tk-t(k-1)是第（k-1)个和第k个顾客到达之间的时间间隔长度，k≥1（t0被认为是0），xt是位于时间轴上t点左边的时刻tk的数量，t≥0。

The stochastic arrival process (input flow) is assumed to be determined if we know the joint distribution of random values τk 如果我们知道随机值τk的联合分布，就可以假定随机到达过程（输入流量）是确定的

k=1....n for any n, n ≥ 1 or the joint distribution of the random values xt for all t, t ≥ 0.

k=1 . . n 对于任何n，n≥1或者对于所有t，t≥0的随机值xt的联合分布。
             

- Definition 1.1 A stochastic arrival process is called stationary if for any integer $m$ and any non-negative numbers $u_{1}, \ldots, u_{m}$, the joint distribution of random variables $\left(x_{t+u_{k}}-x_{t}\right), k=1, \ldots, m$ is independent of $t$

On the intuitive level, this means that the distribution of the number of customers arriving during a certain time interval depends on the length of this interval and does not depend on the location of this interval on the time axis.

定义1.1 如果对于任何整数$m$和任何非负数$u_{1}, \ldots, u_{m}$，随机变量$\left(x_{t+u_{k}}-x_{t}\right), k=1, \ldots, m$的联合分布与$t$无关，则该随机到达过程称为静止的

在直观的层面上，这意味着在某一时间间隔内到达的顾客数量的分布取决于这一间隔的长度，而不取决于这一间隔在时间轴上的位置。

- Definition $1.2$ A stochastic arrival process is called ordinary if for any $t$ it holds(如果对任何一个t来说，一个随机的到达过程被称为普通的，那么它就会持有)

$$
\lim _{\Delta \rightarrow 0} \frac{P\left\{x_{t+\Delta}-x_{t}>1\right\}}{\Delta}=0
$$

粗略地说，这意味着两个或更多的顾客同时到达几乎是不可能的。

- Definition 1.3 A stochastic arrival process is said to be a flow without aftereffect if the numbers of customers arriving in non-overlapping time intervals are mutually independent random variables.（如果在不重叠的时间间隔内到达的客户数量是相互独立的随机变量，则称随机到达过程为无后遗症流。）

- Definition $1.4$ A stochastic arrival process is said to be a flow with limited aftereffect if the random variables $\tau_{k}, k \geq 1$ are mutually independent.（如果随机变量τk，k≥1是相互独立的，则称一个随机到达过程为具有有限后效应的流。）

- Definition $1.5$ A stochastic arrival process is said to be recurrent $($ or renewal $)$ if it is a flow with limited aftereffect and the random values $\tau_{k}, k \geq 1$ are identically distributed.定义1.5$ 如果一个随机到达过程是一个具有有限后效的流，并且随机值$是$\tau_{k}, k \geq 1$ 同分布的，那么我们就称其为循环性$（$或更新）。

  - Let $A(t)=P\left\{\tau_{k}<t\right\}$ be the distribution function, which completely determines the renewal arrival process.让$A(t)=P\left\{\tau_{k}<t\right\}$为分布函数，它完全决定了更新到达过程。

    If $A(t)$ is the exponential distribution, $A(t)=1-e^{-\lambda t}$ then the first symbol is $M$ in Kendall's notation.如果$A(t)$是指数分布，那$A(t)=1-e^{-\lambda t}$ 么第一个符号是Kendall符号中的$M$。

    If distribution $A(t)$ is degenerate, i.e., the customers arrive at regular intervals, then the first symbol is $D$ in Kendall's notation. 如果分布$A(t)$是退化的，也就是说，顾客是以固定的时间间隔到达的，那么第一个符号是Kendall符号中的$D$。

    If $A(t)$ is hyperexponential,

    如果$A(t)$是超指数的。
    $$
    A(t)=\sum_{k=1}^{n} q_{k}\left(1-e^{-\lambda_{k} t}\right)
    $$



​				where $\lambda_{k} \geq 0, q_{k} \geq 0, k=1, \ldots, n, \sum_{l=1}^{n} q_{l}=1$ then in Kendall's notation the first symbol is $H M_{n} .$ 

​				If $A(t)$ is Erlang with parameters $(\lambda, k)$,
$$
A(t)=\int_{0}^{\infty} \lambda \frac{(\lambda t)^{k-1}}{(k-1) !} e^{-\lambda t} d t
$$
​				then the first symbol is Ek, k is called the order of the Erlang distribution.

- Definition 1.6 The intensity (the rate) $\lambda$ of the stationary stochastic arrival process is the expectation (the mean number) of customers arriving per time unit
  $$
  \lambda=M\left\{x_{t+1}-x_{t}\right\}=\frac{M\left\{x_{t+T}-x_{t}\right\}}{T}, T>0 .
  $$



- Definition $1.7$ Parameter $\alpha$ of a stationary stochastic arrival process is called the positive value, determined as静止的随机到达过程的参数称为a正值，确定为

$$
\alpha=\lim _{\Delta \rightarrow 0} \frac{P\left\{x_{t+\Delta}-x_{t} \geq 1\right\}}{\Delta} .
$$



- Definition $1.8$ A stationary ordinary input flow without aftereffect is called simple.
  The following propositions are valid.一个没有后遗症的静止的普通输入流被称为简单。以下命题是有效的。

  - Proposition 1.1 The input flow is simple if and only if it is stationary Poisson, i.e.,
    $$
    P\left\{x_{t+u}-x_{t}=k\right\}=\frac{(\lambda u)^{k}}{k !} e^{-\lambda u}, k \geq 0 .
    $$
    

  - Proposition 1.2 The input flow is simple if and only if it is recurrent with exponential distribution of time intervals between customer arrivals, $A(t)=1-e^{-\lambda t} .$

  - Proposition $1.3$ If $n$ customers of a simple input flow arrived during a time interval of length $T$ then the probability that a tagged customer arrived during time interval

  - $\tau$ inside the interval of length $T$ does not depend on when the other customers arrived and how the time interval $\tau$ is located inside $T$. This probability is $\tau / T$.

  - Proposition $1.4$ The intensity and the parameter of a simple flow are equal. The mean number of customers arriving during the time interval $T$ is equal to $\lambda T$.

  - Proposition 1.5 Superposition of two independent simple fows having parameters $\lambda_{1}$ and $\lambda_{2}$ is again a simple flow with parameter $\lambda_{1}+\lambda_{2} .$

  - Proposition 1.6 A flow obtained from a simple flow of rate $\lambda$ as a result of applying the simplest procedure of recurrent sifting (an arbitrary customer is accepted to the sifted flow with probability $p$ and ignored with probability $1-p)$ is a simple flow of rate $p \lambda$

  - Proposition 1.7 The flow obtained as a result of the superposition of $n$ independent recurrent flows having a uniformly small rate converges to a simple flow as $n$ increases.









##  