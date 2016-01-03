
## Random Calculus

### Introduction
In this section we discuss the concept of conditional time dependence component.  In order to model randomness in signals (noise signals), we introduce the notion of random processes.  Note that the tools are deterministic mathematical constructs; randomness only enters when observations are conducted.  We first state the clasic definition of random processes.



### Definition 1.  Random Processes
*A random (or stochastic) process $\{X_t,t\in T\}$ is a collection of random variables on the same probability space $(\Omega, \mathcal{F},P)$.  The index set T is usually representing time and can be either an interval [t<sub>1</sub>,t<sub>1</sub>] or a discrete set.  Therefore the random process X can be written as a function:*
$$ X : \mathbb{R} \times \Omega \rightarrow \mathbb{R}, (t,\omega) \mapsto X(t,\omega) $$

*In the stochastic interpretation, a sample $\omega$ is chosen from the sample space $\Omega$ "at random".  This yields the "stochatic signal" or "noise signal" r(.,$\omega$) defined on index set T.  This signal is also denoted as sample path, realisation or trajectory.*

#### Notation Remark
We introduced random or stochastic processes as functions wth to arguments: t and $\omega$.  We will, however, omit the argument $\omega$ for brevity as it is done in most text books: X(t,$\omega$)=X(t).

By the definition of random processes, we know that the amount of information is increasing with time.  Again, we need the concept of sigma algebras.  We assume that information is not lost with increasing time and therefore the corresponding $\sigma$-algebras will increase over time as more and more information becomes available. This concept is called filtration.

### Definition 2 Filtration/adapted process
A collection $\{\mathcal{F}_t\}_{t\ge0}$ of a sub $\sigma$ algebras is called filtration if, for every $s\le t$ we have $\mathcal{F}_s\subseteq\mathcal{F}_t$.  The random variables $\{X_t:0\le t\le\infty\}$ are called adpated to the filtration $\mathcal{F}_t$ if, for every t, X<sub>t</sub> is meaurable with respect to $\mathcal{F}_t$.
![Figure 1](https://selene.hud.ac.uk/u1273400/images/seg_media/r1.PNG)
**Figure 1** Example of a filtration

The concept of a filtration is easily understood with a simple example

#### Example 1
Suppose we have a sample space of four elements: $\Omega=\{\omega_1, \omega_2, \omega_3, \omega_4\}$.  At time zero, we do not have any information about which $\omega$ has been chosen.  At time T/2 we know whether we have $\Omega=\{\omega_1, \omega_2\}$ or $\{\omega_3, \omega_4\}$. At time T, we have full information

Therefore, we have the folloing $\sigma$-algebras:
$$ \mathcal{F}_t=\left\{
\begin{aligned}[lcr]
\{0,\Omega\}, && t \in [0, \frac{T}{2}) \\
\{0,\{\omega_1,\omega_2\},\{\omega_3,\omega_4\},\Omega\}, && t \in [\frac{T}{2}, T) \\
\mathcal{F}_{max}=2^{\Omega}, && t=T
\end{aligned} \right\} $$


```R

```
