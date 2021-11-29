

[TOC]

When studying classical Markovian queuing systems, it is useful to apply known results for the so-called birth-and-death processes.

在研究经典的马尔科夫排队系统时，对于所谓的出生和死亡过程，应用已知的结果是很有用的。

A birth-and-death process $i_{t}, \quad t \geq 0$ is a special case of a homogeneous continuous-time MC with a finite or countable state space. Let us consider a birthand-death process with a countable state space $\{0,1,2, \ldots\} .$ The matrix $Q$ of the infinitesimal coefficients (a generator) of the process has a three-diagonal structure

生死过程$i_{t}, \quad t \geq 0$是具有有限或可数状态空间的同质连续时间MC的一个特殊情况。让我们考虑一个具有可数状态空间$\{0,1,2, \ldots\} .$ 的生死过程。$该过程的无穷小系数矩阵$Q（一个发生器）具有三对角结构
$$
Q=\left(\begin{array}{ccccc}
-\lambda_{0} & \lambda_{0} & 0 & 0 & \ldots \\
\mu_{1} & -\left(\lambda_{1}+\mu_{1}\right) & \lambda_{1} & 0 & \ldots \\
0 & \mu_{2} & -\left(\lambda_{2}+\mu_{2}\right. & \lambda_{2} & \ldots \\
\vdots & \vdots & \vdots & \vdots & \ddots
\end{array}\right)
$$




Parameter $\lambda_{i}$ is called the birth intensity and $\mu_{i}$ is the death intensity of state $i$.

参数$\lambda_{i}$称为出生强度，$u_{i}$为状态$i$的死亡强度。

Probabilities $p_{i}(t)=P\left\{i_{t}=i\right\}, i \geq 0$ arranged in a row vector $\mathbf{p}(t)=$ $\left(p_{0}(t), p_{1}(t), p_{2}(t), \ldots\right)$ satisfy an infinite system of equations

概率$p_{i}(t)=P\left\{i_{t}=i\right\}, i\geq 0$排列在行向量$\mathbf{p}(t)=$ $\left(p_{0}(t), p_{1}(t), p_{2}(t), \ldots\right)$满足一个无限的方程式系统
$$
\frac{d \mathbf{p}(t)}{d t}=\mathbf{p}(t) Q
$$
with the normalization condition $\mathbf{p}(t) \mathbf{e}=1$. If the initial probability distribution $\mathbf{p}(0)$ is known then the solution of this system of equations has the form

归一化条件$\mathbf{p}(t) \mathbf{e}=1$。如果初始概率分布$\mathbf{p}(0)$是已知的，那么这个方程组的解有如下形式
$$
\begin{array}{l}
\mathbf{p}(t)=\mathbf{p}(0) e^{Q t} \\
\text { Denote } \\
\rho_{k}=\frac{\prod_{l=0}^{k-1} \lambda_{l}}{\prod_{l=1} \mu_{l}}, k \geq 0 .
\end{array}
$$
Given that the series $\sum_{k=0}^{\infty} \rho_{k}$ converges and the series $\sum_{k=1}^{\infty} \prod_{i=1}^{k} \frac{\mu_{i}}{\lambda_{i}}$ diverges, the stationary state probabilities of the birth-and-death process $i_{t}, t \geq 0$

鉴于该行$\sum_{k=0}^{\infty} \rho_{k}$ 收敛，该行 $\sum_{k=1}^{\infty} \prod_{i=1}^{k} \frac{\mu_{i}}{\lambda_{i}}$发散，出生和死亡过程的固定状态概率为 $i_{t}, t \geq 0$
$$
p_{i}=\lim _{t \rightarrow \infty} p_{i}(t), i \geq 0
$$
exist and they are defined by relations存在，并且它们是由以下关系定义的
$$
p_{0}=\left(\sum_{k=0}^{\infty} \rho_{k}\right)^{-1}, p_{i}=p_{0} \rho_{i}, i \geq 1 .
$$

## Definition of the Quasi-Birth-and-Death Process and Its Stationary State Distribution

In the study of many queuing systems, for example, systems with $M A P$ and (or) service processes like $P H$, systems operating in a random environment, tandem queues, etc., it becomes necessary to analyze the stationary behavior of a two- or multidimensional Markov process $\xi_{t}=\left\{i_{t}, \mathbf{v}_{t}\right\}, t \geq 0$ with state space

在许多排队系统的研究中，例如，具有$M A P$和（或）P H$等服务过程的系统、在随机环境中运行的系统、串联队列等，有必要分析二维或多维马尔可夫过程$的$\xi_{t}=\left\{i_{t}, \mathbf{v}_{t}\right\}, t \geq 0$状态空间的固定行为。
$$
\mathcal{S}=\left\{(i, \mathbf{v}), \mathbf{v} \in \mathcal{V}_{i}, i \geq 0\right\}
$$
where $\mathcal{V}_{i}$ is a finite set if the Markov process $\xi_{t}=\left\{i_{t}, \mathbf{v}_{t}\right\}, t \geq 0$ is twodimensional, or some finite set of finite-dimensional vectors if the Markov process $\xi_{t}=\left\{i_{t}, \mathbf{v}_{t}\right\}, t \geq 0$ is multidimensional.

其中${V}_{i}$是一个有限集，如果马尔科夫过程是 $\xi_{t}=\left\{i_{t}, \mathbf{v}_{t}\right\}, t \geq 0$二维的。如果马尔科夫过程$\xi_{t}=\left\{i_{t}, \mathbf{v}_{t}\right\}, t \geq 0$ 是多维的，则是一些有限的有限维向量集合。



Enumerate the states of the process $\xi_{t}=\left\{i_{t}, \mathbf{v}_{t}\right\}, t \geq 0$ in lexicographic order and combine the states for which the component $i_{t}$ has value $i$ into the macro-state $i$, sometimes also called the level of process $\xi_{t}=\left\{i_{t}, \mathbf{v}_{t}\right\}, t \geq 0$. According to such an enumeration, the generator $Q$ of this process can be presented in a block form $Q=\left(Q_{i, l}\right)_{i, l \geq 0}$, where $Q_{i, l}$ is a matrix formed by the intensities $q_{(i, \mathbf{r}) ;(l, \mathbf{v})}$ of the process $\xi_{t}, t \geq 0$ transitions from state $(i, \mathbf{r}), \mathbf{r} \in \mathcal{V}_{i}$ to state $(l, \mathbf{v}), \mathbf{v} \in \mathcal{V}_{l}$. The diagonal elements of matrix $Q_{i, i}$ are defined as $q_{(i, \mathbf{r}) ;(i, \mathbf{v})}=-\sum_{(j, \mathbf{v}) \in \mathcal{S} \backslash(i, \mathbf{r})} q_{(i, \mathbf{r}) ;(j, \mathbf{v})}$

按词典顺序列举过程$\xi_{t}=\left\{i_{t}, \mathbf{v}_{t}\right\}, t \geq 0$ 的状态，并将组件$i_{t}$具有值$i$的状态合并为宏观状态$i$。有时也称为水平过程$\xi_{t}=\left\{i_{t}, \mathbf{v}_{t}\right\}, t \geq 0$。根据这样的列举，这个过程的生成器$Q$可以以矩阵形式呈现$Q=\left(Q_{i, l}\right)_{i, l \geq 0}$，其中$Q_{i, l}$是一个由强度$q_{(i,\mathbf{r}); (l, \mathbf{v})}$的过程$\xi_{t}, t \geq 0$从状态$(i, \mathbf{r}), \mathbf{r} \in \mathcal{V}_{i}$转换的强度。到状态$(l, \mathbf{v}), \mathbf{v} \in \mathcal{V}_{l}$。矩阵$Q_{i, i}$的对角线元素定义为$q_{(i, \mathbf{r}) ;(i, \mathbf{v})}=-\sum_{(j, \mathbf{v}) \in \mathcal{S} \backslash(i, \mathbf{r})} q_{(i, \mathbf{r}) ;(j, \mathbf{v})}$



The process $\xi_{t}=\left\{i_{t}, \mathbf{v}_{t}\right\}, t \geq 0$ is called a multidimensional (vector) QuasiBirth-and-Death process $(Q B D)$ if its irreducible block generator $Q=\left(Q_{i, l}\right)_{i, l \geq 0}$ can be presented in the form

过程$\xi_{t}=\left\{i_{t}, \mathbf{v}_{t}\right\}, t \geq 0$被称为多维（矢量）准生死过程$(Q B D)$，其不可简化的块发生器$Q=\left(Q_{i, l}\right)_{i, l \geq 0}$可以以下列形式呈现
$$
Q=\left(\begin{array}{ccccc}
Q_{0,0} & Q_{0} & O & O & \ldots \\
Q_{2} & Q_{1} & Q_{0} & O & \ldots \\
O & Q_{2} & Q_{1} & Q_{0} & \ldots \\
\vdots & \vdots & \vdots & \vdots & \ddots
\end{array}\right)
$$
It follows from the form (2.21) of generator $Q$ that the sets $\mathcal{V}_{i}$ for different values of $i, i>0$ here coincide.

从生成器$ Q $的形式（2.21）可以得出，对于$ i的不同值，i> 0 $的值的集合$ \mathcal{V} _ {i} $是一致的

Theorem 2.1 A necessary and sufficient condition for the existence of a stationary probability distribution of the $M C \xi_{t}, t \geq 0$ is the validity of inequalities

定理2.1 $M C \xi_{t}, t \geq 0$的平稳概率分布的存在的充要条件是不等式的有效性
$$
\mathbf{y} Q_{2} \mathbf{e}>\mathbf{y} Q_{0} \mathbf{e}
$$
where the row vector $\mathbf{y}$ is the unique solution of the system of linear algebraic equations

其中行向量${y}$是线性代数方程组的唯一解
$$
\mathbf{y}\left(Q_{0}+Q_{1}+Q_{2}\right)=\mathbf{0}, \mathbf{y e}=1
$$
The proof of this condition is given in 这个条件的证明在 [93]. This condition is also automatically obtained from conditions 这个条件也是自动从条件中获得的 (2.66)-(2.67) proved below in Sect. $2.4$ for MCs of $M / G / 1$ -type. Below we assume that condition $(2.22)$ holds. Then there exist limits

下面第2.4节证明了$M / G / 1$类型的MCs。下面我们假设条件$(2.22)$成立。那么存在着极限
$$
\pi(i, \mathbf{v})=\lim _{t \rightarrow \infty} P\left\{i_{t}=i, \mathbf{v}_{t}=\mathbf{v}\right\}, \mathbf{v} \in \mathcal{V}_{i}, i \geq 0
$$
which are called stationary state probabilities of the MC. 

这被称为MC的静止状态概率。



Corresponding to a lexicographic ordering of the MC states, we group these probabilities into row vectors

对应于MC状态的词法排序，我们将这些概率分为行向量
$$
\boldsymbol{\pi}_{i}=\left(\pi(i, \mathbf{v}), \mathbf{v} \in \mathcal{V}_{i}\right), i \geq 0
$$
Theorem 2.2 The vectors of stationary state probabilities of the $M C \xi_{t}, t \geq 0$ are calculated as follows:

定理2.2 $M C\xi_{t}, t\geq 0$的静止状态概率向量计算如下。
$$
\boldsymbol{\pi}_{i}=\boldsymbol{\pi}_{0} \mathcal{R}^{i}, i \geq 0
$$
where matrix $\mathcal{R}$ is a minimal non-negative solution of the matrix equation

其中矩阵$\mathcal{R}$是矩阵方程的最小非负解
$$
\mathcal{R}^{2} Q_{2}+\mathcal{R} Q_{1}+Q_{0}=O
$$
and vector $\pi_{0}$ is the unique solution of the following system of linear algebraic equations:

和向量$pi_{0}$是以下线性代数方程组的唯一解。
$$
\begin{aligned}
\pi_{0}\left(Q_{0,0}+\mathcal{R} Q_{2}\right) &=\mathbf{0} \\
\pi_{0}(I-\mathcal{R})^{-1} \mathbf{e}=1
\end{aligned}
$$
Proof It is known that vector $\pi=\left(\pi_{0}, \pi_{1}, \pi_{2}, \ldots\right)$ is a solution of the system of equilibrium equations

证明 已知向量$\pi=\left(\pi_{0}, \pi_{1}, \pi_{2}, \ldots\right)$是平衡方程组的解
$$
\pi Q=\mathbf{0}
$$
with the normalization condition具备归一化条件


$$
\pi \mathbf{e}=1
$$
Suppose that the solution of system (2.28) has the form (2.24). Substituting vectors $\pi_{i}, i \geq 1$ of form $(2.24)$ into equations

假设系统（2.28）的解具有（2.24）的形式。将形式为$(2.24)$的向量$\pi_{i}, i\geq 1$代入方程中
$$
\pi_{i-1} Q_{0}+\pi_{i} Q_{1}+\pi_{i+1} Q_{2}=\mathbf{0}, i \geq 1
$$
of system $(2.28)$, it is easy to see that these equations result in the identities if matrix $\mathcal{R}$ satisfies matrix equation $(2.25) .$ Substituting vectors $\pi_{i}, i \geq 1$ of form $(2.24)$ into equations

系统$(2.28)$，很容易看出这些方程的结果是相同的
如果矩阵$\mathcal{R}$满足矩阵方程$(2.25).$ 将$(2.24)$形式的向量$\pi_{i}, i\geq 1$替换为方程
$$
\pi_{0} Q_{0,0}+\pi_{1} Q_{2}=\mathbf{0}
$$
of system ( $2.28$ ), we obtain that vector $\pi_{0}$ satisfies Eq. $(2.26)$. 系统（$2.28$），我们得到向量$\pi_{0}$满足公式$（2.26）$。

It is known, see [93], that the ergodicity condition (2.22) holds if and only if the spectral radius $\varrho(\mathcal{R})$ of matrix $\mathcal{R}$ is strictly less than $1 .$ 

众所周知，见[93]，遍历条件是(2.22) 当且仅当谱系半径为$\varrho(\mathcal{R})$ 的矩阵$\mathcal{R}$严格来说小于1

Under this condition, the series在此条件下，该系列 $\sum_{l=0}^{\infty} \mathcal{R}^{l}$ converges and is equal to 收敛并等于 $(I-\mathcal{R})^{-1} .$ Equation (2.27) now follows from (2.24) and the normalization condition 方程（2.27）现在由（2.24）和归一化条件得出$\sum_{i=0}^{\infty} \pi_{i} \mathbf{e}=1$.



Note that matrix $\mathcal{R}$ can be represented in the form 可以用以下形式表示 $\mathcal{R}=Q_{0} \mathcal{N}$, where entries其中，条目 $\mathcal{N}_{\mathbf{v}, \mathbf{v}^{\prime}}$ of matrices $\mathcal{N}$ characterize the average time the 表述了在这一过程中的平均时间。$\operatorname{MC} \xi_{t}=\left\{i_{t}, \mathbf{v}_{t}\right\}, t \geq 0$ is in
some macro-state $i$ before it enters level $i-1$ the first time given that the component $\mathbf{v}_{t}$ transits from state $\mathbf{v}$ to state $\mathbf{v}^{\prime}$ during this time.处于
在第一次进入$i-1$层之前，鉴于组件$\mathbf{v}_{t}$在这段时间内从状态$\mathbf{v}$过渡到状态$\mathbf{v}^{\prime}$，所以在某个宏观状态$i$。

Various methods are used to solve Eq. (2.25). The simplest of them is the method of successive approximations. The zero matrix is taken as an initial approximation $\mathcal{R}_{0}$ for matrix $\mathcal{R}$. The formula for calculating successive approximations follows in an obvious manner from $(2.25)$ in the form



使用各种方法来求解方程。 （2.25）。 其中最简单的是逐次逼近法。 零矩阵作为矩阵$ \mathcal {R} $的初始近似值$ \mathcal {R} _ {0} $。 显然，用于计算逐次逼近的公式遵循$（2.25）$的形式

#### 2.3.0

$$
\mathcal{R}_{k+1}=\left(\mathcal{R}_{k}^{2} Q_{2}+Q_{0}\right)\left(-Q_{1}\right)^{-1}, k \geq 0
$$
We note that the inverse matrix in $(2.30)$ exists since matrix $Q_{1}$ is an irreducible subgenerator. It is shown in [93] that the sequence of matrices $\left\{\mathcal{R}_{k}, k \geq 0\right\}$ given by recursion (2.30) converges to the minimal non-negative solution of matrix equation $(2.25)$

我们注意到$(2.30)$中的逆矩阵存在，因为矩阵$Q_{1}$是一个不可还原的子生成器。[93]中显示，由递归（2.30）给出的矩阵序列$\left\{\mathcal{R}_{k}, k \geq 0\right\}$收敛到矩阵方程$（2.25）$的最小非负解。

Another algorithm, the so-called algorithm with logarithmic reduction, uses the relation另一种算法，即所谓的对数还原算法，使用了以下关系
$$
\mathcal{R}=Q_{0}\left(-Q_{1}-Q_{0} \mathcal{G}\right)^{-1}
$$
between the matrix $\mathcal{R}$, which is a solution of Eq. (2.25), and the matrix $\mathcal{G}$, which is a solution of the matrix equation

矩阵$\mathcal{R}$与矩阵$\mathcal{G}$之间的关系，后者是公式（2.25）的解，是矩阵方程的解。
$$
Q_{0} \mathcal{G}^{2}+Q_{1} \mathcal{G}+Q_{2}=O
$$


In turn, matrix $\mathcal{G}$ is found by the method of successive approximations on the basis of the relation

反过来，矩阵$\mathcal{G}$是在关系的基础上通过连续近似的方法找到的
$$
\mathcal{G}=\left(-Q_{1}\right)^{-1} Q_{0} \mathcal{G}^{2}+\left(-Q_{1}\right)^{-1} Q_{2}
$$
The above results for QBD processes are easily extended to the case when the block generator of the process $\xi_{t}, t \geq 0$ has the form

上述关于QBD过程的结果很容易扩展到过程$\xi_{t}, t\geq 0$的块状发生器的情况。
$$
Q=\left(\begin{array}{ccccc}
\tilde{Q}_{0,0} & \tilde{Q}_{0} & O & O & \ldots \\
\tilde{Q}_{2} & Q_{1} & Q_{0} & O & \ldots \\
O & Q_{2} & Q_{1} & Q_{0} & \ldots \\
\vdots & \vdots & \vdots & \vdots & \ddots
\end{array}\right)
$$
where matrices $\tilde{Q}_{0,0}, \quad \tilde{Q}_{0}, \quad \tilde{Q}_{2}$ can have size different from that of blocks $Q_{0}, Q_{1}, Q_{2}$, and blocks $\tilde{Q}_{0}, \tilde{Q}_{2}$ are not square matrices unlike (2.21).

其中矩阵$\tilde{Q}_{0,0}, \quad\tilde{Q}_{0}, \quad\tilde{Q}_{2}$的大小可以与块$Q_{0}, Q_{1}, Q_{2}$不同，并且块$tilde{Q}_{0}, \tilde{Q}_{2}$不是方形矩阵，与（2.21）不同。

In this case, a necessary and sufficient condition for the existence of a stationary state distribution for the process $\xi_{t}, t \geq 0$ is also given by inequality $(2.22)$ where vector $\mathbf{y}$ is the solution of system (2.23). The formulas for calculating the vectors of stationary state probabilities have the following form here:

在这种情况下，过程$\xi_{t}, t\geq 0$的静止状态分布存在的必要和充分条件也由不等式$（2.22）$给出，其中向量$\mathbf{y}$是系统（2.23）的解。这里计算静止状态概率向量的公式有如下形式。


$$
\pi_{i}=\pi_{1} \mathcal{R}^{i-1}, i \geq 1
$$
The above results for QBD processes are easily extended to the case when the block generator of the process $\xi_{t}, t \geq 0$ has the form

上述关于QBD过程的结果很容易扩展到过程$\xi_{t}, t\geq 0$的块状发生器的情况。

where matrix $\mathcal{R}$ is the minimal non-negative solution of matrix equation $(2.25)$, and vectors $\pi_{0}$ and $\pi_{1}$ are the unique solution of the following system of linear algebraic equations:

其中矩阵$\mathcal{R}$是矩阵方程$(2.25)$的最小非负解，而向量$\pi_{0}$和$\pi_{1}$是以下线性代数方程组的唯一解。
$$
\begin{array}{c}
\boldsymbol{\pi}_{0} \tilde{Q}_{0,0}+\boldsymbol{\pi}_{1} \tilde{Q}_{2}=\mathbf{0} \\
\boldsymbol{\pi}_{0} \tilde{Q}_{0}+\boldsymbol{\pi}_{1}\left(Q_{1}+\mathcal{R} Q_{2}\right)=\mathbf{0} \\
\boldsymbol{\pi}_{0} \mathbf{e}+\boldsymbol{\pi}_{1}(I-\mathcal{R})^{-1} \mathbf{e}=1
\end{array}
$$
Similarly, the above results can be generalized to the case of $Q B D$ processes for which not one but some finite number $J$ of block rows of the process block generator have a form different from the one in $(2.21)$.

同样，上述结果可以推广到$Q B D$过程的情况，对于这些过程块发生器的块行不是一个而是一些有限数量的$J$，其形式与$(2.21)$中的不同。

For illustration, we apply the above information for $Q B D$ processes to the analysis of a $M A P / P H / 1$ -type queue.

为了说明问题，我们将上述关于$Q B D$进程的信息应用于$M A P / P H / 1$型队列的分析。

```mermaid

```

