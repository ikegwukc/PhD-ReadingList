
# PhD Reading List

## Table of Contents

- [Foundational](https://github.com/ikegwukc/PhD-ReadingList#foundational)
  - [The Discipline of Machine Learning](https://github.com/ikegwukc/PhD-ReadingList#the-discipline-of-machine-learning-by-tom-m-mitchell)
  - [A Few Useful Things to Know about Machine Learning](https://github.com/ikegwukc/PhD-ReadingList#a-few-useful-things-to-know-about-machine-learning-by-pedro-domingos)
- [Application](https://github.com/ikegwukc/PhD-ReadingList#application)
- [Tutorials](https://github.com/ikegwukc/PhD-ReadingList#tutorials)

## Foundational

----
##### [The Discipline of Machine Learning by Tom M Mitchell](http://www.cs.cmu.edu/~tom/pubs/MachineLearning.pdf)  

This document provides a brief and personal view of machine learning. Good to think of this paper as a foundational paper for machine learning.

Overall endeavor of machine learning:  "How can we build computer systems that automatically improve with experience, and what are the fundamental laws that govern all learning processes?"

A more precise def described by Tom Mitchell. - A machine learns with respect to a particular task T, performance metric P, and type of experience E. This varies by how a researcher chooses T, P, and E.

"Machine Learning focuses on the question of how to get computers to program themselves from an experience with some initial structure."

There's another field that is related to machine learning which is human learning. How do human's learn? The results are less than that of stats.

Tom Mitchell also talks about applications of machine learning. Speech Recognition, computer vision, robot control, applications in physical sciences.

General future use-cases of Machine Learning according to Tom Mitchell:  Application requires that is too complex for people to manually design the algorithm. The application requires that the software customize to its operational environment after it is fielded.

Current Research Questions (2006+):
- Can unlabeled data be helpful for supervised learning?
- How can we transfer what is learned for one task to improve learning in other related tasks? I interpreted this as disproving the Free Lunch Theorem. However this could also be Transfer Learning.
- What's the best strategy for agents that collecting their own training data?
- To what degree can we have both data privacy and the benefits of data mining?
- Can we build never-ending learnings? Learner that just continues to learns no matter which dataset given?
- Can we use machine learning theories and algorithms to help explain human learning?
- Can we design programming languages containing machine learning primitives? (LBJava?; SML?)
- Will computer perception merge with machine learning?ZZ
----  

##### [A Few Useful Things to Know about Machine Learning by Pedro Domingos](https://homes.cs.washington.edu/~pedrod/papers/cacm12.pdf)  
**There a lot of useful gems in this paper **  
Developing successful machine learning applications requires a substantial amount of "black art"  that is hard to find in textbooks. This article summarizes 12 lessons and multiple pitfalls to avoid for machine learning researchers and practictioners.  

For this paper Pedro focuses on classification however any concept could be applied to another type of machine learning.

```
Question: With the bewildering variety of learning algorithms available how can you determine which one to use?
```

They're thousands of frameworks to follow however they all consist of combinations of the following 3 components:
- Representation - A classifier (some model) being able to be represented in a formal lanaguage that a modern computer can handle.
- Evaluation - An evaluation function that distingiushes a good model from a bad one.
- Optimization - A method to search among the classifiers in the potential representations for the highest-scoring one.  

Here are examples for classifiers:  

| Representation | Evaluation | Optimization |
| -------------- | ---------- | ------------ |
| KNN | Accuracy / error rate | Greedy Search |  
| SVM             | Precision and recall | Beam Search Search |  
| Decision trees  | Likelihood | Continuous Optimization|  
| Neural Networks | Cost / Utility | Gradient descent |  

Most textbooks are organized by representation, and it's easy to overlook the fact that the other components are equally important.

The fundamental goal of machine learning is to generalize beyond the examples in the training set. No matter how much data we have, it is very unlikely that we will see those exact examples again at test time.

The most common mistake among machine learning beginners is to test on the training data and have the illusion of success. If the chosen classifier is then tested on new data it is often no better than random guessing. So if you hire someone hold out some data. If you are a practictioner hold out some data for testing. It is possible  to tune your data from the testing unattentionally.
```
Sort of my take on the above paragraph. Split into train and test. Then use cross validation on train. then finally test when ready.
```

We generally don't have access to the function we want to optimize we have you use an evaluation method on the training set and a surrogate for the testing set.


*Unforunately*, every learner must embody some knowledge or assumuptions beyond the data to generalize beyond it. (No free Lunch theorem)

Great analogy: Programming is a lot of work that involves building from scratch. However machine learning is similar to farmering where we let nature do most of the work. Farmers combine seeds with nuterients to grow crops. Learners combine knowledge with data to grow programs.

If our knowledge and data we have are not sufficient to determine the correct classifier, we end up choosing a classifer that "hulluncinates" (also known as overfitting). Commonly this is recognized when you get a 100% accuracy on your training data and a significantly lower amount on your testing dataset.

This occurs in other forms too and generalizes to bias and varience.

Bias is a learners tendency to consistently learn the wrong thing. Varience is the tendency to learning random things irrespective of the real signal.

Cross validation &  regularization & other methods can be used to combat overfitting.

Another problem in machine learning is the curse of dimensionality. Generalizing becomes exponentially harder as the dimensionality grows assuming the training size remains the same.

*[I won't speak too much about theoretical guarantees. The main concepts that I took from this section is that in practice you will not get a specific guarantee and it's quite easy to disprove because of the no free lunch theorem. The main role of theorectical guarantees in machine learning is n used more as a source of understanding for algorithm design.]*

Feature engineering is probably the most important factor. Nowadays feature engineering is becoming more automated.

After you finish feature engineering and you select the best model possible you can either put more effeort into designing a clever algorithm. Or you can  throw more data at it. Simpler learners (parametric) may not be able to improve significantly given more data usually complex learners (non-parametric) are better.  However applying occam's razor try the simplest learners first then progress to complicated learners.

Having many learners apply to the data is better than just one. Using boosting or bagging yields better results than just using one learner.

Every function can be represented however that does not mean it can be learned also correlation does not imply causation.

----
## Application

## Tutorials
