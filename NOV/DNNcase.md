
## CASE FOR DEEP NEURAL NETWORKS FOR DATA CLASSIFICATION

Contrastive Divergence is an an efficient learning algorithm that allows Deep Belief Networks learn multi-layer generative models from unlabeled data.  This greedy layer-wise pretraining method can be used to initialize a neural network that is fine-tuned with back-propagation (Sarikaya, Hinton & Deoras, 2014).



Neural Networks initialised by Deep Belief Networks were found to perform as well as those that use other algorithms such as Supprt Vector Machines (SVMs), Boosting and Maximum Entropy.  However, these other algorithms depend on supervised learning of pre-classified data.  DBNs on the other hand have the benefit of also accurately classifying unlabeled data.

Up until recently, Neural networks efficiency was impeded by difficulty of training when compared to their probabilistic couterparts such as Hidden Markov Models. In order to overcome this limitation an optimized probabilistic algorithm known as the Restricted Boltzmann Machine (RBM) was invented to incorporate efficient probabilistic training methods using Deep Belief networks to provide fast training algorithms. In other words,Saraki et. al. (2014) assert that DBNs are analogous to Maximum entropy classifiers whose features are being learned rather than being preset.

## NAIVE BAYES
The Naive Bayes is a supervised, probabilistic classifier.  It does well with data whose inputs are independent from each other and biased towards problems where each variable probability is above zero.  The Naive Bayes probability uses conditional probability to make predictions about future outcomes.  Conditional probabilities involve at least two variables and measures the probability of one or more events based on the presence or absence of one or more other separate variables.  The Naive bayes derivation is better understood from the perspective of the chain rule.



### CHAIN RULE
This is the probability that three or more events will occur simultaneously. The general case of the chain rule is expressed as follows:

$ P(A_1,A_2, ... , A_n)= P(A_1)P(A_2|A_1)P(A_3|A_2,A_1)...P(A_n|A_{n-1}, ... , A_1) $


The Naive Bayes takes advantage of the interplay between conditional probability and joint probability.  Thus, on the left hand side of the equation we hold one of these variables as independent while the others are dependent on the independent variables whilst independent of each other.  So the equation now becomes.

$ P(A_1|A_2, ... , A_n)= P(A_1)P(A_2|A_1)P(A_3|A_1)...P(A_n|A_1) $


## MAXIMUM ENTROPY CLASSIFIERS

*Maximum Entropy based classifiers do not assume statistical independence of the features that are used as predictors.  As such, they allow the combination of multiple overlapping information sources.  The information sources are combined as follows:*

$  \frac{e^{ \sum_i\lambda_{i}f_i(C,W)} }{\sum_{C'} e^{ \sum_i\lambda_{i} f_i(C,W)}} $

*which describes the probability of a particular class C (e.g. call-types) given the word sequence  spoken by the caller.  Notice that the denominator includes a sum over all clases C', which is essentially a normalisation factor of for probabilities to sum to 1.  The f<sub>i</sub> are indicator functions, or features, which are “activated” based on computable features on theword sequence,
for example if a particular word or word pair appears, or if the parse tree contains a particular tag, etc. The MaxEnt models are trained using the improved iterative scaling algorithm [21] with Gaussian prior smoothing [20] using a single universal variance parameter of 2.0.*

## Boosting
*Boosting is a method that can be used in conjunction with many learning algorithms to improve the accuracy of the learning algorithm. The idea of Boosting is to produce an accurate prediction rule by combining many moderately inaccurate (weak) rules into a single classifier. At each iteration,
boosing adds a new (weak) prediction rule that focuses on samples that are incorrectly classified by the current combined predictor. Even though Boosting is known to be sensitive to noisy data and outliers, in some problems, it is less susceptible to overfitting than most machine learning algorithms.*

*We used a specific implementation of Boosting, AdaBoost using decision stumps, which is described in [6]. Boosting has been applied to a number of natural language processing tasks in the past [9].*

## Support Vector Machines
*Support vector machines (SVMs) are supervised learning methods used for classification. The basic SVM takes a set of input data and predicts, for each given input, which of two possible classes forms the output, making it a non-probabilistic binary classifier.  SVMs are derived from the theory of structural risk minimization[7]. SVMs learn the boundaries between samples of the two classes by mapping these sample points into a higher dimensional space. SVMs construct a hyperplane or a set of hyperplanes in a high-dimensional space, which can be used for classification. Intuitively, a good separation is achieved by the hyperplane that has the largest distance to the nearest training
data point of any class (the “functional margin”), since in general the larger the margin the lower the generalization error of the classifier. The hyperplane separating these regions is found
by maximizing the margin between closest sample points belonging to competing classes. In addition to performing linear classification, SVMs can efficiently perform non-linear classification using what is called the kernel trick, implicitly mapping their inputs into high-dimensional feature spaces. Much of
the flexibility and classification power of SVMs resides in the choice of kernel. Some of the commonly used kernels are linear, polynomial and radial basis functions. In this work, we chose linear kernels to train the SVM since computationally it is faster compared to other kernels, yet there is no significant difference in performance for the current task. This is a fairly standard result for applying SVMs in natural language processing since we are already using a high-dimensional feature vector.*

## REFERENCES

Sarikaya, R., Hinton, G., & Deoras, A. (2014). Application of Deep Belief Networks for Natural Language Understanding. IEEE/ACM Transactions On Audio, Speech, And Language Processing, 22(4), 778-784. http://dx.doi.org/10.1109/taslp.2014.2303296


```python

```
