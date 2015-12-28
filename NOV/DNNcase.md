
## CASE FOR DEEP NEURAL NETWORKS FOR DATA CLASSIFICATION

Contrastive Divergence is an an efficient learning algorithm that allows Deep Belief Networks learn multi-layer generative models from unlabeled data.  This greedy layer-wise pretraining method can be used to initialize a neural network that is fine-tuned with back-propagation (Sarikaya, Hinton & Deoras, 2014).

Neural Networks initialised by Deep Belief Networks were found to perform as well as those that use other algorithms such as Supprt Vector Machines (SVMs), Boosting and Maximum Entropy.  However, these other algorithms depend on supervised learning of pre-classified data.  DBNs on the other hand have the benefit of also accurately classifying unlabeled data.

Up until recently, Neural networks efficiency was impeded by difficulty of training when compared to their probabilistic couterparts such as Hidden Markov Models. In order to overcome this limitation an optimized probabilistic algorithm known as the Restricted Boltzmann Machine (RBM) was invented to incorporate efficient probabilistic training methods using Deep Belief networks to provide fast training algorithms. In other words,Saraki et. al. (2014) assert that DBNs are analogous to Maximum entropy classifiers whose features are being learned rather than being preset.

### Machine Learning

Machine Learning is analogous to human learning due to the similarity of learning from experience for humans beng practically analogous to machines learning from data (Marsland, 2009). 

### NEURAL NETWORKS

Traditional Neural Networks are so called due to their being modeled after the interconnection of brain cells called neurons.  Each neuron in the brain is approximated to be connected to thousands of other neurons.  A particular feature of the brain called plasticity. Plasticity allows neurons to change their particular interconnections to other neurons based on events that occur. It is this feature that is perceived to cause learning in humans(ref.)

In much the same way artificial neural networks are characterized by receiving several inputs, an activation function as well as an output.  These artificial neurons can receive stimuli in the form of inputs and weights associated with each connection can determine the response to a particular set of inputs.  

In particular, the Rosenblatt(1958) perceptron uses a binary function to sub-divide input into to categories. *A perceptron uses a step function that returns +1 if the weighted sum of the inputs, X, is greater than a threshold, t, and -1 if X is less than or equal to t:*  When the perceptrons are layered to form a network, an artificial neural network is formed.  The layout of the network is essential to achieve optimal results. A typical Neural network layout is given in the diagram below:
![Artificial Neural Network](https://selene.hud.ac.uk/u1273400/images/seg_media/nn.PNG)

The Artificial neural network comprises an input layer, a hidden layer and an output layer.  In order to avoid over-fitting, no more than  two layers are used at the hidden layer. The outputs of the hidden layer are weighted linear functions of the inputs wrapped in what is called the activation function.  These outputs aggregrate from one layer to the next.  Some common activation functions outlined by (ref) is shown in the table below (table)

Thus, algebraically, the output of a neural network layer is given by $ \phi(w_1x_1+w_2x_2) $ where $ \phi $ is an activation function like sigmoid, and $ w_i $ weights are being pre-determined by the training algorithm.  Basic training algorithms that are based on the Gradient Descent algorithm include the delta rule, back propagation, quick propagation and RProp (ref).  These methods attempt to converge the neural network by minimizing error based on local inputs and estimating the next iteration step error.

As mentioned the biggest drawbacks of Neural Networks is their complexity which leads to poor effective training algorithms and therefore slow convergence.(ref) heuristic for creating neural networks is as follows:

- *The number of hidden neurons should be between the number of inputs and the number of neurons at the output layer*
- *The number of hidden neurons should be two-thirds the size of the input layer, plus the size of the output layer*
- *The number of hidden neurons should be less than twice the size of the input layer.*
- *The maximum epochs and maximum error define the network convergence point and can be set at 1% tolerance and 1000 iterations or epochs.

## NAIVE BAYES
The Naive Bayes is a supervised, probabilistic classifier.  It does well with data whose inputs are independent from each other and biased towards problems where each variable probability is above zero.  The Naive Bayes probability uses conditional probability to make predictions about future outcomes.  Conditional probabilities involve at least two variables and measures the probability of one or more events based on the presence or absence of one or more other separate variables.  The Naive bayes derivation is better understood from the perspective of the chain rule.



### CHAIN RULE
This is the probability that three or more events will occur simultaneously. The general case of the chain rule is expressed as follows:

$ P(A_1,A_2, ... , A_n)= P(A_1)P(A_2|A_1)P(A_3|A_2,A_1)...P(A_n|A_{n-1}, ... , A_1) $


The Naive Bayes takes advantage of the interplay between conditional probability and joint probability.  Thus, on the left hand side of the equation we hold one of these variables as independent while the others are dependent on the independent variables whilst independent of each other.  So the equation now becomes.

$ P(A_1|A_2, ... , A_n)= P(A_1)P(A_2|A_1)P(A_3|A_1)...P(A_n|A_1) $

## Hidden Markov Models
Hidden Markov Model is a probabilistic Finite state machine that expresses the probability of dependent states as they move in between each other. Kirk (2014) proposes a simplification of HMM using the chain rule and a 3-step algorithm that makes use of Forward-Backward algorithm and Viterbi Algorithm. The three step algorithm defines Evaluation, Decoding and Learning.  Evaluation is the likelihood of a particular sequence given events that occur.  Decoding tries to build the underlying model given the sequence of events.  Learning is the application of the model to make deductions about the model and predict future events based on the model.

### Step1: Evaluation with Forward Backward algorithm
This is the probability of an event happening given the underlying states.  Mathematically, this probability $ P(e_k|s) $ is proportional to the joint distribution of the event and the sequence of states that produced it.  That is
$$ P(e_k|s) \propto P(e_k|s) $$

Using the Markov Assumption this simplifies to
$$ P(e_k|s) = \alpha P(s_{k+1},s_{k+2},...,s_n|e_k)P(s_{1},s_{2},...,s_k,e_k) $$

Graphically, we can represent this probability as the joint probability of the state that produced the event looking at its forward and backward probabilities. *The backward term is lookingat the conditional probability of the hidden state at point k given all the emmissions up to that point.  The backward term is looking at the conditional probability of emmissions k+1 to the end of that hidden point*.


### Step 2:Decoding with Viterbi Algorithm
*Given a sequence of observations, we want to parse out the best path of states given what we know about them.*  Thus mathematically
$$ \pi^* = arg max_{\pi}P(x,\pi) $$
Where $ \pi $ is a state vector and x is the observations.
The Viterbi algorithm constructs a maximum spanning tree using a greedy algorithm to iterate through all the possible steps.  Graphically it is represented by the figure below.

What is bieng attempted is to traverse the set of states in the most optimal fashion.  *We do this by determining the probability that a state will happen given its emmissions as well a the probability that it will transition from the previous state to the current.  Then we multiply those two together to get the probability that the sequence will happen.  Iterating through the entire sequence, we eventually find* the *optimal sequence*.


### Step 3: Learning
The likely hood of a future event given the underlying model can be solved by the Viterbi algorithm estimating the next step in the sequence model.  This is achieved by  by maximizing the next step without any events.  *This is known as the next optimal state emmission combo*. 

## MAXIMUM ENTROPY CLASSIFIERS

*Maximum Entropy based classifiers do not assume statistical independence of the features that are used as predictors.  As such, they allow the combination of multiple overlapping information sources.  The information sources are combined as follows:*

$  \frac{e^{ \sum_i\lambda_{i}f_i(C,W)} }{\sum_{C'} e^{ \sum_i\lambda_{i} f_i(C,W)}} $

*which describes the probability of a particular class C (e.g. call-types) given the word sequence  spoken by the caller.  Notice that the denominator includes a sum over all clases C', which is essentially a normalisation factor of for probabilities to sum to 1.  The f<sub>i</sub> are indicator functions, or features, which are â€œactivatedâ€ based on computable features on theword sequence,
for example if a particular word or word pair appears, or if the parse tree contains a particular tag, etc. The MaxEnt models are trained using the improved iterative scaling algorithm [21] with Gaussian prior smoothing [20] using a single universal variance parameter of 2.0.*

## Boosting
*Boosting is a method that can be used in conjunction with many learning algorithms to improve the accuracy of the learning algorithm. The idea of Boosting is to produce an accurate prediction rule by combining many moderately inaccurate (weak) rules into a single classifier. At each iteration,
boosing adds a new (weak) prediction rule that focuses on samples that are incorrectly classified by the current combined predictor. Even though Boosting is known to be sensitive to noisy data and outliers, in some problems, it is less susceptible to overfitting than most machine learning algorithms.*

*We used a specific implementation of Boosting, AdaBoost using decision stumps, which is described in [6]. Boosting has been applied to a number of natural language processing tasks in the past [9].*

## Support Vector Machines
*Support vector machines (SVMs) are supervised learning methods used for classification. The basic SVM takes a set of input data and predicts, for each given input, which of two possible classes forms the output, making it a non-probabilistic binary classifier.  SVMs are derived from the theory of structural risk minimization[7]. SVMs learn the boundaries between samples of the two classes by mapping these sample points into a higher dimensional space. SVMs construct a hyperplane or a set of hyperplanes in a high-dimensional space, which can be used for classification. Intuitively, a good separation is achieved by the hyperplane that has the largest distance to the nearest training
data point of any class (the â€œfunctional marginâ€), since in general the larger the margin the lower the generalization error of the classifier. The hyperplane separating these regions is found
by maximizing the margin between closest sample points belonging to competing classes. In addition to performing linear classification, SVMs can efficiently perform non-linear classification using what is called the kernel trick, implicitly mapping their inputs into high-dimensional feature spaces. Much of
the flexibility and classification power of SVMs resides in the choice of kernel. Some of the commonly used kernels are linear, polynomial and radial basis functions. In this work, we chose linear kernels to train the SVM since computationally it is faster compared to other kernels, yet there is no significant difference in performance for the current task. This is a fairly standard result for applying SVMs in natural language processing since we are already using a high-dimensional feature vector.*


## REFERENCES

Aitkin, M., & Foxall, R. (2003). Statistical modelling of artificial neural networks using the multi-layer perceptron. Statistics and Computing, 13(3), 227-239. doi:10.1023/A:1024218716736

Kirk, M. (. s. (2014). Thoughtful machine learning: A test-driven approach (Firstition. ed.). Beijing: O'Reilly Media.

Sarikaya, R., Hinton, G., & Deoras, A. (2014). Application of Deep Belief Networks for Natural Language Understanding. IEEE/ACM Transactions On Audio, Speech, And Language Processing, 22(4), 778-784. http://dx.doi.org/10.1109/taslp.2014.2303296
