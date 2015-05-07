---
layout: post
title: "PhD week 2:  27th April - 1st May 2015"
---

## Literature review

After changing the focus of my literature review at the end of last week, I've identified a fairly long list of papers related to activity tracking on computing devices, and the use of activity tracking data for Information Retrieval.

A recurring question across many of these papers concerns the way in which we categorise computer use. At one level of abstraction, we can view the user moving the cursor, clicking, and pressing keys, at a level above, we can identify _actions_ from these - moving a window, visiting a URL, opening a document, etc. However, to step up to a higher level still, there are a number of ways we can abstract away further. We can attempt to understand the user's _activities_ - ("Booking a holiday", "Researching a paper", "Paying a bill", "Checking Facebook"), or we can instead try and categorise _types of use_ which cut across individual activities - ("Casual browsing", "Open-ended research", "Performing a task", "Answering a question") in order to attempt to understand a users' computing behaviour.

Both of these are valid approaches, and there's plenty of literature showing useful applications of these types of taxonomy of computer activities to information retrieval problems. However, what's very interesting is the extent to which our choice of categorisation of activities encodes a particular world view, and, often, some subjective notion of the relative _value_ of different activities. Recognising this, and attempting to control for it leads to some interesting research opportunities, by explicitly designing for this subjectivity.

Research opportunities: Explicitly subjective task identification and behaviour change, Situated view of task identification. How devices correspond to modes of use,
How topics correspond to modes of use. Inference running in either direction.

## Properly grokking metrics, models and methods

Being deeply immersed in literature review has also meant I've had to brush up on quite a few IR / ML / Stats basics that I've once learned but have fallen into disuse. In particular, I spent some time revising the various evaluation metrics reported for binary classification problems (accuracy, F1, log-loss), their specific properties, and the conditions under which they diverge. I'm making a little browser-based visualisation of this which I will post soon. I also gave myself a refresher in ensembling techniques (Boosting and Bagging) and their effects on the bias and variance of the ensemble, learnt about [Morphological analysis](https://www.cs.bham.ac.uk/~pjh/sem1a5/pt2/pt2_intro_morphology.html), and refreshed my memory about how [L<sub>1</sub> regression can do something analogous to automatic feature selection](http://en.wikipedia.org/wiki/Least_squares#Lasso_method)

## BRML

I've been working my way slowly through the Linear Models chapter of [BRML](http://web4.cs.ucl.ac.uk/staff/D.Barber/pmwiki/pmwiki.php?n=Brml.HomePage), which has been a really useful exercise. In the past, I've attempted to read the entire textbook in order, and then proceeded to perform a sort of depth-first search through the mathematics behind it, encountering a tricky bit of analysis or vector calculus, and then diverting my attention to properly understanding the mathematical techniques used before carrying on with the book. Perhaps unsurprisingly, this made for pretty slow progress. In contrast, this time, I've started with a specific topic which is (a) reasonably simple, and (b) immediately useful in my practical work, and aimed to achieve a decent working knowledge of that topic, rather than shooting for a comprehensive overview of the whole field in one go. This has proved to be far more successful, both in terms of the amount of material I can cover, as well as my understanding and retention of it. This isn't to say that I'm eliding all the details - I've also been working through derivations on paper where they're unclear, which has been a great help. However, concentrating on a topic with a manageable scope and a clear application has worked wonders.

Other things I've learned from this exercise: My calculus (especially multi-variate) is much better than I feared it might be, and the Kernel Trick is one of the cleverest, most elegant bits of applied mathematics I think I've seen.

## Learning Matlab

I've also dedicated a bit of time this week to learning Matlab / Octave. While It's still not my preferred environment for doing my own work (Python, with the usual scientific libs and iPython notebooks, is still the best compromise between 'language I like' and 'decent scientific tooling' for me), it's been really useful, both in terms of giving me a subtly different perspective on the same problems I might tackle in Python or Scala, and in terms of being able to read and understand other people's Matlab code.

## Other reading

 This article: "[Algorithmic Force and Fascism](http://theoccupiedtimes.org/?p=13764)" at the Occupied Times makes some  interesting points, but ultimately makes a rather weak argument against the use of statistics and computation in public policy from technological determinism. I'd counter that neither specific technology, nor the positivist scientific approach are a problem in themselves (and in fact, the literature on ML and computational statistics is *very* guarded in making claims about the predictive power of models). In my view, rather than constituting an argument against quantitative and algorithmic methods in public policy, this is instead a call for greater critical thinking and self-reflection on the part of those doing the analysis and modelling. In particular, it's imperative that we consider the interests and assumptions of ourselves and those we work for, as well as our place in the wider social context.


