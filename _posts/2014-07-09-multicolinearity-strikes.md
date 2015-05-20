---
layout: post
title: Day notes 11th July 2014
---

# Multicollinearity strikes!

I've been messing around with some toy text classification problems recently, as a means of exploring [active learning](http://en.wikipedia.org/wiki/Active_learning_(machine_learning)), starting by implementing the algorithm described in a paper called [*"A sequential algorithm for training text classifiers"*](http://dl.acm.org/citation.cfm?id=188495) in python.

One problem I encountered, while trying to train a logistic regression classifier on a binary text classification problem, was the training stage failing as the design matrix (made up of simple term counts per document, minus stopwords) was apparently singular.

This seemed strange, as the matrix of document / term counts was not square, and therefore admittedly not invertible, but not singular by the definition of singularity either. However, since singularity teds to be
