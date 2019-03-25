---
layout: post
title: "[GSoC] Letor Learning Notes"
---

# Letor from a search engine prospective

<div align = right> By Cong Ding, Mar. 25, 2019, Learning notes from <a href=http://terrierteam.blogspot.com/2013/03/learning-to-rank-research-using-terrier.html>the blogs</a>
</div>

## Top K Retrieval (Sample)

* BM25 is sufficient for Letor

* sample size for different situations (more @ [paper](http://www.dcs.gla.ac.uk/~craigm/publications/macdonald12inrt_ltr.pdf))

* Dynamic pruning (WAND): conservative/aggressive strategies

**Conclusion:** The sample size varies from query to query, we need to apply different pruning methods(safe/unsafe) in conformity with the scenarios.

## Feature Extraction





## Learned Model Application

