---
layout: post
title: "[GSoC] Letor Learning Notes"
---

# Letor from a search engine prospective

Learning notes from the [blogs](http://terrierteam.blogspot.com/2013/03/learning-to-rank-research-using-terrier.html) and more papers about click model.


## Top K Retrieval (Sample)

* sample size for different situations (more @ [paper](http://www.dcs.gla.ac.uk/~craigm/publications/macdonald12inrt_ltr.pdf))

* Dynamic pruning (WAND): conservative/aggressive strategies

**Conclusion:** The sample size varies from query to query —— Too big (poor efficiency) v.s. too small (poor effectiveness). We need to apply different pruning methods(safe/unsafe) in conformity with the scenarios.

## Feature Extraction

* learned approaches
* query independent/ query dependent
* query features matter



## Click Models

### Some problems:

1. position bias —— punishment
2. cold start 
3. click influenced by appearance —— collect more session information
4. data sparseness —— data smoothing

### Basic Click Models

#### 1. Random Click Model (RCM)

The probability of each document is equal. Used as baseline. Only one parameter.

#### 2. Click-through Rate Models (CTR)  

##### 2.1 Rank-Based CTR Model (RCTR)

P related to the document's rank

##### 2.2 Document-based CTR Model (DCTR)

using query-document pair to set up the model

#### 3. Position-based Model (PBM)

Click = Examine and Attracted 

consider E and A as independent variables

**Attention:** attractiveness decided by the contents shown in the search result page instead of the whole document. E is related to position.

![PBM](https://congding.info/blog/pics/PBM.png)

![PBM2](https://congding.info/blog/pics/PBM2.png)

#### 4. Cascade Model (CM)

based on the hypothesis that the user browse the documents from top to bottom and stop until satisfied. Only click one time in the session.

![CM1](https://congding.info/blog/pics/CM1.png)

![CM2](https://congding.info/blog/pics/CM2.png)

#### 5. Dynamic Bayesian Network Model (DBN)

Add a parameter S to show that if the user is satisfied by the document.

If satisfied, the session ends, else, the user goes on to examine the next document (if attractive).

![DBN1](https://congding.info/blog/pics/DBN1.png)

![DBN2](https://congding.info/blog/pics/DBN2.png)

##### Simplified DBN Model (SDBN)

assume γ = 1, easy for parameter estimation.

and if S always = C, AKA σ = 1，SDBN will degrade as cascade model.

TO BE CONTINUED FOR OTHER MODELS

#### Summary

![sum1](https://congding.info/blog/pics/summary1.png)

![sum2](https://congding.info/blog/pics/summary2.png)

### Parameter Estimation

two methods:

1. THE MLE ALGORITHM

2. THE EM ALGORITHM

All random variables can be observed —— MLE

hidden variables —— EM 

#### MLE

MLE for SDBN:

![MLE1](https://congding.info/blog/pics/MLE1.png)

![MLE2](https://congding.info/blog/pics/MLE2.png)

![MLE3](https://congding.info/blog/pics/MLE3.png)

TO BE CONTINUED (I really need to install a jekyll plug-in for LaTeX support! )

#### EM

TO BE CONTINUED

### Architecture

data collecting -> data cleaning -> data mining -> system integration

### Effect Evaluation

1. MAP (mean average precision)
2. MRR (mean reciprocal rank)







