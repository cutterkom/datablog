+++
type    = "post"
title     = "Machine Learning in Economics"
date    = "2016-12-13"
categories  = ["Economics"]
tags    = ["Economics", "Notes", "Machine Learning"]

+++



["How will machine learning impact economics?" - Quora, Susan Atney](https://www.quora.com/How-will-machine-learning-impact-economics)

>in the longer run econometricians will modify the methods and tailor them so that they meet the needs of social scientists primarily interested in conducting inference about causal effects and estimating the impact of counterfactual policies 

- ML is broad term, she uses narrowly

## 2 branches in ML

### 1. supervised learning
- features/covariates/x to predict outcome y
- methods: LASSO, random forest, regression trees, support vector machines
  - common feature: cross-validation to select model complexity = off-the-shelf ML methods
  - = training and test data sets
    - = repeatedly estimate model on part of the data --> test it on another part
    - find the **“complexity penalty term”** that fits the data best in terms of **mean-squared error of the prediction** (the squared difference between the model prediction and the actual outcome)
* cross-sectional econometrics (traditional): one model specified, robustness checks by looking at 2 or 3 alternatives
* but econometrics is not only about good prediction
  * prediction != causal effect
  * sometimes goodness-of-fit is reduced in order to estimate causal effect, e.g. changing prices
  * "Techniques like instrumental variables seek to use only some of the information that is in the data – the “clean” or “exogenous” or “experiment-like” variation in price—sacrificing predictive accuracy in the current environment to learn about a more fundamental relationship that will help make decisions about changing price. This type of model has not received almost any attention in ML."
* her research: take ML methods and apply them  to causal inference
  * required: change objective function, b/c "ground thruth of causal parameter not observed in any test set"
  
> Statistical theory plays a bigger role, since we need a model of the unobserved thing we want to estimate (the causal effect) in order to define the target that the algorithms optimize for.

* she's researching on developing a statistical theory, e.g. random forests
  
### 2. unsupervised learning

* no outcome variable y
* find clusters of similar objects
* she did: find clusters of news articles on a similar topic

> They are commonly used to group images or videos; if you say a computer scientist discovered cats on YouTube, it can mean that they used an unsupervised ML method to find a set of similar videos, and when you watch them, a human can see that all the videos in cluster 1572 are about cats, while all the videos in cluster 423 are about dogs. **I see these tools as being very useful as an intermediate step in empirical work, as a data-driven way to find similar articles, reviews, products, user histories, etc.**



[Susan Athey on how economists can use machine learning to improve policy](https://siepr.stanford.edu/highlights/susan-athey-how-economists-can-use-machine-learning-improve-policy)



> "Supervised machine learning is basically about prediction"

> "You have some features (x's) and you try to predict (y's). The innovations from machine learning have been to **find really effective ways** to do that, especially **in an environment when there are lots of x's and you don't have a theory for exactly how the x's should predict the y's.**"

ML: systematic way of selecting which factors matter and why

**Applied to Policy problems**

* detained in jail pending trials, who released on bail? 

**What ML can't**

> But these techniques currently do not uncover how changing one factor affects others --which is at the heart of evaluating policy impacts. 

**Athnes research**

* modify supervised ML to be able to ask this questions: I change one factors - what happens? 

* ensure effects are valid and not product of chance

> "In some sense, these are methods that could open up the ability to discover what is in the data without the risk that you are going to end up with a false discovery"


## Arguments against ML in Econometrics

[link](https://www.quora.com/Why-is-econometrics-isolated-from-the-big-data-machine-learning-revolution)

- econometricians want to explain observed phenomena

- some ML techniques (neural network, SVM, ensemble) have difficult time quantifying impact of one variable on the observed phenomena
- philosophical diff: econometricians start with theory, ml starts with data
- times series have LOTS of problems; not controllable in ML, but with manual handwork:
  - Controlling multicollinearity (controlling VIF)
  - Finding co-integrated series
  - Controlling spurious relations
  - Controlling over-fitting
  - Controlling and solving autocorrelation problem
  - Controlling and solving heteroscedasticity problem

* ML about prediction/optimal path; econometrics about causation
  * ML could help in forecasting
