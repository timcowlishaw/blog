---
layout: post
title: Literature review, weeks 3-4
---

## [Context-aware recommender systems for learning: A survey and future challenges](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?reload=true&arnumber=6189308) (Verbert, Manouselis, Ochoa, Wolpers, Drachsler, Bosnic & Duval, 2012)
A survey of existing literature on context-aware recommendations, with an emphasis on technology-enhanced learning (TEL) applications. Includes valuable background on different definitions and taxonomies of context in interaction, as well as an overview of different models for incorporating contextual information into recommender systems.

Cites:

 - [Context-Aware Recommender Systems](http://dl.acm.org/citation.cfm?id=1454068) (Adomavicius and Tuzhilin, 2011) - Earlier work on the use of context in recommendations in general
 - [An Operational Definition of Context](http://dl.acm.org/citation.cfm?id=1770848) (Zimmerman, Lorenz and Opperman 2007) - Work outlining definition and categorisation of interaction contexts.


## [HypTrails - A Bayesian Approach for Comparing Hypotheses about Human Trails on the Web](http://arxiv.org/abs/1411.2844) (Singer, Helic, Hotho and Strohmaier 2015)

Proposes a general approach for comparing and evaluating hypotheses about web-browsing behaviours (expressed as 'trails') within a Bayesian framework. Hypotheses about state transition probabilities are expressed as dirichlet priors on a markov model (using the Trail Roulette approach to estimate parameters), and a partial order is induced over competing hypotheses corresponding to the posterior bayes factor of the hypothesis (wrt the observed data). Provides a principled approach for testing hypotheses about online behaviour in experimental work, as well as pointing to future work in segmenting user behaviours with respect to a set of hypotheses.

Cites:

 - [Detecting memory and structure in human navigation patterns using markov chain models of varying order](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0102070) (P. Singer, D. Helic, B. Taraghi, and M. Strohmaier 2014) - Prior work on use of Markov chains for modelling browsing behaviour:
 - [Inferring markov chains: Bayesian estimation, model comparison, entropy rate, and out-of-class modeling](http://arxiv.org/abs/math/0703715) (C. C. Strelioff, J. P. Crutchfield, and A.W. Hübler 2007) - Text on markov chain models and bayesian estimation in general
 - [Stream prediction using a generative model based on frequent episodes in event sequences](http://research.microsoft.com/apps/pubs/default.aspx?id=71393) (S. Laxman, V. Tankasali, and R.W. White 2008) - previous work outlining an analagous use of Bayes Factors for comparing hypotheses
 - [Bayesian model selection and model averaging](http://www.sciencedirect.com.libproxy.ucl.ac.uk/science/article/pii/S0022249699912786) (Wasserman 2000) - Text on bayesian model selection in general
 - Previous work on the 'Trail roulette' approach to constructing priors for experimental hypotheses:
  - Biostatistics and the medical research council (Gore 1987)
  - [Probablistic Programming & Bayesian Methods for Hackers](http://camdavidsonpilon.github.io/Probabilistic-Programming-and-Bayesian-Methods-for-Hackers/) (Davidson-Pilon 2014)
  - [Eliciting univariate probability distributions](http://www.jeremy-oakley.staff.shef.ac.uk/Oakley_elicitation.pdf) (Oakley 2010)


## [Refinding is not finding again](https://vtechworks.lib.vt.edu/handle/10919/20183) (Capra, Pinney and Pérez-Quiñoes 2005)

Experiments into differences in user behaviour between finding and refinding tasks in information retrieval. Highlights the importance of the concept of post-value recall (the situation whereby a user only discovers that the information is valuable after having accesssed it), and the role of procedural and episodic memory in refinding tasks.

Cites:

  - [Post-Valued Recall Web Pages: User Disorientation Hits The Big Time](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.3.7688) (Wen 2003) - source for concept of Post-value recall

## [Rethinking the web as a personal archive](http://research.microsoft.com/apps/pubs/default.aspx?id=183834) (Lindley, Marshall, Banks, Sellen, Regan)

Interview-based qualitative study concerned with how users store, organize and interact with personal media online. Mostly concerned with media created by the participants, but has applications to refinding of information in general (several participants saw the ability to refind information as essentially equivalent to ownership of it).

