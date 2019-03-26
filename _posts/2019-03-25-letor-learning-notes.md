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



### Parameter Estimation

two methods:

1. THE MLE ALGORITHM

2. THE EM ALGORITHM

All random variables can be observed —— MLE

hidden variables —— EM 

#### MLE

MLE for SDBN:

![MLE1](https://congding.info/blog/_posts/MLE1.png)

![MLE2](https://congding.info/blog/_posts/MLE2.png)

![MLE3](https://congding.info/blog/_posts/MLE3.png)

to be conitued (I really need to install a jekyll plug-in for LaTeX support! )

#### EM

to be continued

### Architecture

data collecting -> data cleaning -> data mining -> system integration

### Effect Evaluation

1. MAP (mean average precision)
2. MRR (mean reciprocal rank)







