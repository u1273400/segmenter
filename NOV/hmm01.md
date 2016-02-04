
## Gaussian Mixture Models
In this section a Gaussian Random variable and a mixture of Gaussian random variable is derived.  The end product is a Gaussian Mixture Model (GMM). This can be applied to fit real-world data such as speech features.  The GMM as a statistical model for Fourier-spectrum-based speech features plays an important role in acoustic modeling of conventional speech recognition systems.

### Basic Properties
Let $(\Omega,\mathcal{A},P)$ be a probability measure with $E, F, E^c \in \mathcal{A}$
1. $P(E\cup F)=P(E)+P(F)$ if $E \cap F=0$
2. $P(E\cup F)=P(E)+P(F)-P(E\cap F)$
3. $P(E)=1-P(E^c)$
4. $P(E \cup F^c)=P(E)-P(E\cap F)$
5. **Inclusion-Exclusion Formula** $$P(\bigcup_{i=1}^nE_i)=\sum_iP(E_i)-\sum_{i<j}P(E_i\cap E_j)+\sum_{i<j<k}P(E_i\cap E_j \cap E_k) + \dots\ +(-1)^{n+1}P(E_1\cap E_2\cap\dots\cap E_n)$$
![Figure 1](https://selene.hud.ac.uk/u1273400/images/seg_media/ierule.PNG)
**Figure 1: Inclusion Exclusion Rule**
6. $P(\bigcup_{i=1}^nE_i)\le \sum_{i=1}^nP(E_i)$ and $P(\bigcup_{i=1}^\infty E_i)\le\sum_{i=1}^\infty P(E_i)$


## Bayesian/Conditional Probability

There are two ways to consider Bayesian probability.  The first method and the second method is the measure theory method.  The first being a more simpler method than the second, however, the following themes are observable in both.
1. They are methods of obtaining a conditional probability also known as the posterior or updated probability
2. It is based upon a prior evidence known as the prior evidence and an update evidence known as the likelihood evidence

### Bayes Rule Using Ratios
In as much as the using the ratios method of Bayes probability is rather straight forward.  Certain principles need to be adhered to, in order to draw on the gains of this method and use it properly in practical scenarios.  The algorithm at arriving at the posterior probability therefore is as follows:

1. Know the Prior probability
2. Know the likelihood ratios
3. Multiply the marginal variable ratios of the prior and likelihood to obtain the posterior probability

### Bayes Rule from measure theory
The method we just considered is the simple yet intuitive way to look at Bayes Rule.  This method is a means to appreciate the second approach to Bayes Rule which is an in-depth and elaborate approach to solving conditional probability. In as much as the elaborate method goes into great detail in expanding upon probability principles it is a comprehensive study of the subject of Bayesian probability and accounts for many practical scenarios that may be applied to daily probability challenges.  The simplified method looks at probability variables using ratios while the second elaborate method takes a broad and formal approach using the principles of a branch of mathematics referred to as measure theory.

#### Measure Theory Principles
1. **Probability Space**
2. **Types of Probability**
3. **Probability Distributions**
4. **Probability Unions**
5. **Marginal Probability**
6. **Conditional Probability**
7. **Chain Rule**


```python

```
