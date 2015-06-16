---
layout: post
title: "Designing Computer Systems that See - Notes on a lecture by Abigail Sellen"
---

[Abigail Sellen](http://research.microsoft.com/en-us/people/asellen/), from
Microsoft Research, came to [give a guest
lecture](http://events.ucl.ac.uk/event/event:h6i-i8g3nuuu-czxr74/designing-computer-systems-that-see)
at UCL yesterday. Sellen's work has featured fairly prominently in my research
so far, in particular her [paper with Steve
Whittaker](http://research.microsoft.com/apps/pubs/default.aspx?id=130843)
investigating the use of lifelogging technology, and laying out some principles
for the design of lifelogging systems, and her work with [S&icirc;an Lindley et.
al.](http://research.microsoft.com/apps/pubs/?id=159317) on the ways in which use
of the web is situated within everyday life and routines. While the topic of her
talk was ostensibly the design of systems with some computer vision component,
a lot of the insights she shared from her experiences with this are very
applicable to the design of intelligent systems more generally, and were very
useful in helping me to examine and articulate some aspects of my own research
interests. I'll briefly share my notes on the lecture here.

The main theme of the talk was *symbiosis* in the design of computer
systems, which Sellen described as a continuously-evolving process whereby human
needs shape the design of a technology system, which in turn shapes the
behaviour of the humans interacting with it, in response. Giving examples from
her own work at MSR, she elaborated on how this symbiosis
manifests itself in a system's behaviour, as well as ways of designing for
symbiosis in intelligent systems.

Principally, it seems to me that the main challenges for the design of such
systems are ones of perception and intelligibility. The system must be able to
perceive the relevant information it needs from its environment, and in turn,
its output must be intelligible by the users interacting with it. This might
seem like a simple point, but, as Sellen shows, both of these processes can be
hampered in ways that are sometimes subtle. For instance, in a [medical
visualisation system controlled by
gestures](http://dl.acm.org/citation.cfm?id=2541899) (for use in a sterile
operating theatre environment), the gesture-detection algorithm was often be
confused by two people dressed in identical scrubs, stood in front of each
other. It was discovered by the MSR team developing this system that this
problem was solved by enabling a feature originally intended for debugging,
whereby the surgeon was given feedback, in the form of a stick-man-like graphic
overlaid on the video feed, showing how the algorithm perceived the people in
its environment. That way, they could quickly identify and remedy the source of
any interference.

This use of perception-revealing feedback from the algorithm to the user was
a recurring theme in the talk, and designing ways of visualising this feedback
seems to be one of the central challenges. For instance, in a system designed to
[assist in the diagnosis of Multiple Sclerosis using computer
vision](http://dl.acm.org/citation.cfm?id=2686930), it was discovered that
clinicians were mistrustful of the output of the algorithm, due to the fact that
it's decisions were opaque. Presenting a visualisation of the amount of tremor
detected in the patient's limbs over time (one of the principal features in the
classification algorithm) to the clinician along with the automatic
classification alleviated this, without the need to change the way the system
worked internally - illustrating the reasons why an algorithm has
arrived at a given output is more effective in making it intelligible to the
user, than attempting to explain how it did so.

Another interesting example, which is especially relevant to my own interests,
(and for which I can't currently find a reference or link), concerned a mobile
application allowing users to curate collections of real-life objects, by
photographing and tagging them. The application attempted to automatically
identify the photographed object, and the three most-likely classifications were
presented to the user, encouraging them to select the appropriate one, or to
provide a more accurate classification, from which the object classification
algorithm would learn in future. Sellen pointed out that the misclassifications
presented here also played a valuable role in revealing the system's perception
of the world to the user, enabling them to understand how the system arrived at
its judgements. In this way, they functioned as a feedback mechanism in two ways -
 explicitly soliciting feedback on classifications, while also implicitly
shaping use of the system by revealing the algorithm's perception of the world.

Sellen also described another interesting consequence of this feedback - users
were also curious about how the algorithm would perceive various objects, and
would experiment with photographing things in order to see the suggested
classifications. In this way, the misclassifications also afforded a kind of
serendipity in the way the users themselves viewed the world and used the
application - this is particularly interesting to me as I've been thinking about
how active learning techniques such as uncertainty sampling (which by design
present the most-uncertain classifications to the user) might also be used to
model some sort of serendipity in information retrieval.

The correspondence between Sellen's work and active learning techniques seems
fairly natural to me, in a way that's pretty fundamental. Sellen talked about
how she sees the role of intelligent systems as being to work in partnership
with humans, enabling rather than replacing them, and active learning is an
obvious technique to facilitate this goal in general.

A couple of other shorter observations, noted here for posterity:

Sellen highlights the value in intelligent systems that perceive the world in
a *different way* to humans, rather than emulating them. This is a useful thing
to keep in mind. I can imagine many ways in which this difference could manifest
itself however: As well as the obvious one of sensing different stimuli as input,
this difference could manifest itself in terms of different ways of
agglomerating this input into higher level features and output actions, different lengths and accuracies of recall of perceived stimuli over time, or simply presence in the world at a different time or space to the user. The central thing here is to look at both the needs and *capabilities* of the user and to design a system around both.

A question from the audience pointed out the correspondence between Sellen's
work and the HCI literature on *Distributed Cognition*. This is an area I've
come across before and not examined fully yet, and so will definitely now do so
as a priority.


