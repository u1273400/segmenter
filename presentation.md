
# NEW WORKFLOW FOR COMPUTER SCIENCE RESEARCH

## JOHN ALAMINA
### NOVEMBER, 2015

*"Separation of concerns makes for good modular design - Can there be exceptions to this rule?"*

## Contents<a name="contents"></a>

1. [Prerequisites](#prerequisites)
2. [Disclaimer](#disclaimer)
3. [The new workflow](#workflow)
4. [GIT & GitHub](#git)
5. [Jupyter](#jupyter)
6. [Markdown](#markdown)
7. [A case for Neural Networks](#case)
8. [Keeping it simple - *hopefully*](#simple)
9. [Concluding Remarks](#remarks)
10. [Appendix I - Git commands](#A1)
11. [Appendix II - Useful links](#A2)


## [Prerequisites](#contents)<a name="prerequisites"></a>
1. GIT
2. GITHUB account

## [Disclaimer](#contents)<a name="disclaimer"></a>
#### Warning this material is experimental and may appear to have content that may seem to be more of ‘academic hipsterism’ and as such may not appear to find immediate advantage nor usability.  However, once successfully applied, may also be addictive with a ‘no turning back’ tendency. A middle ground is therefore sought at the end but this is only an attempt to find and evolutionary reason for adoption.

## [The New Workflow](#contents)<a name="workflow"></a>


```python
'''
By way of introduction
'''
```


## [GIT](#contents)<a name="git"></a>


## [Jupyter](#contents)<a name="jupyter"></a>
Jupyter is an acronym that was formed from the fusion of three scripting languages being fused into one environment namely
- Julia
- Python and
- R

## [MarkDown](#contents)<a name="markdown"></a>
Markdown is a counter intuitive means of authoring documents on the web.



## [A case for Neural Networks](#contents)<a name="case"></a>

Contrastive Divergence is an an efficient learning algorithm that allows Deep Belief Networks learn multi-layer generative models from unlabeled data.  This greedy layer-wise pretraining method can be used to initialize a neural network that is fine-tuned with back-propagation (Sarikaya, Hinton & Deoras, 2014).



Neural Networks initialised by Deep Belief Networks were found to perform as well as those that use other algorithms such as Supprt Vector Machines (SVMs), Boosting and Maximum Entropy.  However, these other algorithms depend on supervised learning of pre-classified data.  DBNs on the other hand have the benefit of also accurately classifying unlabeled data.

Up until recently, Neural networks efficiency was impeded by difficulty of training when compared to their probabilistic couterparts such as Hidden Markov Models. In order to overcome this limitation an optimized probabilistic algorithm known as the Restricted Boltzmann Machine (RBM) was invented to incorporate efficient probabilistic training methods using Deep Belief networks to provide fast training algorithms. In other words,Saraki et. al. (2014) assert that DBNs are analogous to Maximum entropy classifiers whose features are being learned rather than being preset.

### NAIVE BAYES
The Naive Bayes is a supervised, probabilistic classifier.  It does well with data whose inputs are independent from each other and biased towards problems where each variable probability is above zero.  The Naive Bayes probability uses conditional probability to make predictions about future outcomes.  Conditional probabilities involve at least two variables and measures the probability of one or more events based on the presence or absence of one or more other separate variables.  The Naive bayes derivation is better understood from the perspective of the chain rule.



#### CHAIN RULE
This is the probability that three or more events will occur simultaneously. The general case of the chain rule is expressed as follows:

$ P(A_1,A_2, ... , A_n)= P(A_1)P(A_2|A_1)P(A_3|A_2,A_1)...P(A_n|A_{n-1}, ... , A_1) $


The Naive Bayes takes advantage of the interplay between conditional probability and joint probability.  Thus, on the left hand side of the equation we hold one of these variables as independent while the others are dependent on the independent variables whilst independent of each other.  So the equation now becomes.

$ P(A_1|A_2, ... , A_n)= P(A_1)P(A_2|A_1)P(A_3|A_1)...P(A_n|A_1) $


### MAXIMUM ENTROPY CLASSIFIERS

*Maximum Entropy based classifiers do not assume statistical independence of the features that are used as predictors.  As such, they allow the combination of multiple overlapping information sources.  The information sources are combined as follows:*

$  \frac{e^{ \sum_i\lambda_{i}f_i(C,W)} }{\sum_{C'} e^{ \sum_i\lambda_{i} f_i(C,W)}} $

*which describes the probability of a particular class C (e.g. call-types) given the word sequence  spoken by the caller.  Notice that the denominator includes a sum over all clases C', which is essentially a normalisation factor of for probabilities to sum to 1.  The f<sub>i</sub> are indicator functions, or features, which are â€œactivatedâ€ based on computable features on theword sequence,
for example if a particular word or word pair appears, or if the parse tree contains a particular tag, etc. The MaxEnt models are trained using the improved iterative scaling algorithm [21] with Gaussian prior smoothing [20] using a single universal variance parameter of 2.0.*

### Boosting
*Boosting is a method that can be used in conjunction with many learning algorithms to improve the accuracy of the learning algorithm. The idea of Boosting is to produce an accurate prediction rule by combining many moderately inaccurate (weak) rules into a single classifier. At each iteration,
boosing adds a new (weak) prediction rule that focuses on samples that are incorrectly classified by the current combined predictor. Even though Boosting is known to be sensitive to noisy data and outliers, in some problems, it is less susceptible to overfitting than most machine learning algorithms.*

*We used a specific implementation of Boosting, AdaBoost using decision stumps, which is described in [6]. Boosting has been applied to a number of natural language processing tasks in the past [9].*

### Support Vector Machines
*Support vector machines (SVMs) are supervised learning methods used for classification. The basic SVM takes a set of input data and predicts, for each given input, which of two possible classes forms the output, making it a non-probabilistic binary classifier.  SVMs are derived from the theory of structural risk minimization[7]. SVMs learn the boundaries between samples of the two classes by mapping these sample points into a higher dimensional space. SVMs construct a hyperplane or a set of hyperplanes in a high-dimensional space, which can be used for classification. Intuitively, a good separation is achieved by the hyperplane that has the largest distance to the nearest training
data point of any class (the â€œfunctional marginâ€), since in general the larger the margin the lower the generalization error of the classifier. The hyperplane separating these regions is found
by maximizing the margin between closest sample points belonging to competing classes. In addition to performing linear classification, SVMs can efficiently perform non-linear classification using what is called the kernel trick, implicitly mapping their inputs into high-dimensional feature spaces. Much of
the flexibility and classification power of SVMs resides in the choice of kernel. Some of the commonly used kernels are linear, polynomial and radial basis functions. In this work, we chose linear kernels to train the SVM since computationally it is faster compared to other kernels, yet there is no significant difference in performance for the current task. This is a fairly standard result for applying SVMs in natural language processing since we are already using a high-dimensional feature vector.*

### REFERENCES

Sarikaya, R., Hinton, G., & Deoras, A. (2014). Application of Deep Belief Networks for Natural Language Understanding. IEEE/ACM Transactions On Audio, Speech, And Language Processing, 22(4), 778-784. http://dx.doi.org/10.1109/taslp.2014.2303296


## [Keeping it Simple - *hopefully*](#contents)<a name="simple"></a>

## [Concluding Remarks](#contents)<a name="remarks"></a>

## [Appendix I - Git Commands](#contents)<a name="A1"></a>
- git clone *url* (to make a local copy of a remote repository in an empty folder)
- git commit -m *message* (comcommits checked out branch)

## [Appendix  II - Useful Links](#contents)<a name="A2"></a>
- [Pandoc Installation](https://github.com/jgm/pandoc/releases/tag/1.15.2)
- [MikTex Installation](http://miktex.org/download)
- [Learn Git By Udacity](https://www.udacity.com/course/viewer#!/c-ud775/l-3105028581/e-3073678898/m-3073678899)
- [Git Installer](https://confluence.atlassian.com/bitbucket/set-up-git-744723531.html)
- [Learn Git Branching](http://cdn-thumbshot-ie.pearltrees.com/dd/f6/ddf6671bc8562cf5537625d27510bef8-b52square.jpg)




```python

```
