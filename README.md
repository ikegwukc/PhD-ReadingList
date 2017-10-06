
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
| Knn | Accuracy / error rate | Greedy Search |  
| SVM             | Precision and recall | Beam Search Search |  
| Decision trees  | Likelihood | Continous Optimization|  
| Neural Networks | Cost / Utility | Gradient descent |  

----
## Application

## Tutorials
