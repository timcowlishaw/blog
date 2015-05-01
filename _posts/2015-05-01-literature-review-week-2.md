---
layout: post
title: Literature review, week 2
---

## Understanding User Productivity - M Picq 2014

This is a Masters thesis supervised by Emine and Filip from last year, describing a project to measure the effect of time-tracking tools on a users productivity. It provides a useful overview of the literature on tracking and analysing computer usage, and an outline of the process and technical challenges of writing a time-tracking application for Windows, as well as the analysis of user behaviour itself.
One drawback of the experiment (which is highlighted within the paper's own analysis) is the fact that productivity is inherently subjective. While the paper reports a statistically significant ($ p \\leq 0.01 $) increase in user productivity, partitioning the users into those using their computers for professional purposes, and those using them in a personal capacity, indicates that the effect is only significant for the 'professional' users, possibly indicating that the dependent variable in the experiment (a boolean 'productive' vs. 'not productive' judgement per application or site provided by the experimentor) encodes a particular set of assumptions about what constitutes 'productive' behaviour which are biased towards specific processional situations. This could be investigated further (as the report acknowledges) by allowing users to define for themselves which activities are considered productive or not. This only requires a slight relaxation of the assumptions of the experiment: rather than assuming that the classification of an activity as being productive or not-productive is constat globally, we have to assume that it is constant with respect to time for each user. (Of course, this is still a simplifying assumption, but a weaker one than the original study makes). There is also the possibility of some interaction with the results from the reflective behaviour of classifying ones own behaviours, but this could be a useful line of enquiry in its own right - 'reflection' being one of [Whitakker and Sellen]('http://research.microsoft.com/apps/pubs/default.aspx?id=130843')'s  'Five Rs' of lifelogging user behaviour).

Some pointers to other interesting work from the citations:
  - [A Framework for Mobile User Activity
   Logging](http://www.kde.cs.uni-kassel.de/ws/muse2010/proceedings.pdf#page=39) (Woerndl, Manhardt and Prinz 2010) - Prior work on user modelling through activity logging on mobile, combining passive data capture with explicit feedback.
  - [Context as a dynamic construct](http://dl.acm.org/citation.cfm?id=1463117) (Greenberg 2001) - Analysis of the role of user context in human-computer interaction.
  - Several papers on machine-learning approaches to task identification treating
   it as a classification problem:
    - [Enhancing just-in-time e-learning through machine learning on desktop
    context sensors](http://link.springer.com/chapter/10.1007/978-3-540-74255-5_25#page-1) (Lokaiczyk, Faatz, Beckhaus and Goertz 2007)
    - [Automatically classifying emails into activities](http://dl.acm.org/citation.cfm?id=1111471&dl=ACM&coll=DL&CFID=504937992&CFTOKEN=15067425) (Dredze, Lau and Kushmerick 2006)
    - [A hybrid learning system for recognizing user tasks from desktop activities and email messages](http://dl.acm.org/citation.cfm?id=1111473) (Shen, Li, Dietterich and Herlocker 2006)
  - [Switch Detector: An Activity Spotting System for Desktop](http://dl.acm.org/citation.cfm?id=2063947) (Mirza, Chen, Chen, Hussain and He 2011) - A different approach to task identification - using techniques from time-series analysis to detect context switches in user behaviour.
  - A couple of papers describing approaches for soliciting user feedback to tag
   / classifiy activities:
    - [Usage Patterns of Collaborative Tagging Systems](http://jis.sagepub.com/content/32/2/198.short?rss=1&ssource=mfc) (Golder and Huberman 2006)
    - [Lightweight Tagging Expands Information and Activity Management Practices](http://dl.acm.org/citation.cfm?id=1518746) (Oleksik, Wilson, Tashman, Mendes Rodrigues, Kazai, Smyth and Jones 2009)

## ["It's simply integral to what I do": Enquiries into how the Web is Weaved into Everyday Life](http://dl.acm.org/citation.cfm?id=2187836.2187979&coll=DL&dl=ACM) - Lindley, Meek, Sellen and Harper 2012

A diary study which set out to update existing taxonomies of web activities in order to better reflect the ways in which use of the web is intertwined with everyday life and situated within it. Using a grounded theory analysis of the diaries and interviews with the study participants, the paper instead proposes a new taxonomy of 5 "modes" of internet use, which cut across domain, media type and application: ("Respite", "Orienting, "Opportunistic Use", "Purposeful use" and "Lean-back Internet") as well as highlighting two material qualities of the web which enable these modes of use. This could present an interesting opportunity for understanding a more subjective notion of productivity as discussed above - it might be interesting to measure how these 5 modes correlate with self-reported productivity, whether mode can be inferred from user interaction, and whether reporting time spent in each mode of interaction (in a manner analagous to  Picq 2014) produces any improvement in self-reported productivity.

Useful citations:
  - Prior work on taxonomies of user activity:
    - [A goal-based classification of web information tasks](http://eprints.rclis.org/8781/) (Kellar, Watters and Shepherd 2006)
    - [Seize the occasion! The seven-segment system for online marketing](http://www.strategy-business.com/article/19940?pg=all) (Rozanski, Bollman, and Lipman 2001)- 7 'usage occasions' which conflate 'purpose' and 'method' of browsing
    - [A taxonomic analysis of what World Wide Web activities significantly impact people's decisions and actions](http://dl.acm.org/citation.cfm?doid=634067.634167) (Morrison, Pirolli and Card 2001)
    - [How knowledge workers use the web](http://dl.acm.org/citation.cfm?id=503418) (Sellen, Murphy and Shaw 2002)
    - [A field study characterizing web-based information-seeking tasks](http://onlinelibrary.wiley.com/doi/10.1002/asi.20590/abstract?deniedAccessCustomisedMessage=&userIsAuthenticated=false) (Kellar, Watters, and Inkpen 2007) - this one includes some analysis of automatically captured activity logs with a focus on user intents.
  - [How people use the web on mobile devices](http://dl.acm.org/citation.cfm?id=1367619) (Cui and Roto 2009) - identifies contextual factors in web use, and introduces the concept of "personal spce extension"
  - [Basics of Qualitative Research](http://www.sagepub.com/textbooks/Book235578) (Strauss and Corbin 1998) - Reference for the grounded theory methodology used here.
  - [Everyday life information seeking: Approaching information seeking in the context of "way of life"](http://www.tandfonline.com/doi/abs/10.1081/E-ELIS3-120043920#) (Savolainen 1995) - Reference for the idea of 'orienting', as distinct from 'practical information'
  - References for the concept of 'role transitions' in user behavior:
    - [All in a day's work: Boundaries and micro role transitions](http://www.jstor.org/discover/10.2307/259305?uid=363926941&uid=3738032&uid=2&uid=363926901&uid=3&uid=67&uid=62&sid=21106622263423) (Ashforth, Kreiner and Fugate 2001)
    - [Home and Work: Negotiating boundaries through everyday life](http://press.uchicago.edu/ucp/books/book/chicago/H/bo3683629.html) (Nippert-Eng 1995)
  - References on Casual Leisure and Information Behaviours:
    - [Understanding casual-leisure information behaviour](http://www.emeraldinsight.com/doi/abs/10.1108/S1876-0562%282011%29002011a012) (Elsweiler, Wilson, and Kirkegaard 2011)
    - [Leisure and its relationship to library and information science: Bridging
   the gap](https://www.ideals.illinois.edu/handle/2142/13654) (Stebbins, 2009)
  - [Plastic: A metaphor for integrated technologies](http://dl.acm.org/citation.cfm?id=1409667) (Rattenbury, Nafus and Anderson 2008) - citation for the concept of the 'placticity' of the web.
)

## [Cross-Device Search](http://research.microsoft.com/en-us/um/people/ryenw/talks/pdf/MontanezCIKM2014.pdf) (Montañez, White and Huang, 2014)

Study based on commercial search engine logs investigating how and when users transition between two devices between successive queries. Demonstrates a predictive model both for the probability that a device transition occurs, and the probablity of the next device type conditioned on a transition having occured. (The unconditioned probabillity of the next device is less interesting as it is dominated by the large prior probability that no switch occured, hence the 'previous device' feature dominates and the most likely next device is always the previous one). Interesting findings: the topic of the previous query and the overall probability of a transition conditioned on the current device are good predictors for the probability of a transition occuring, however they do not predict the next device well (which is overwhelmingly predicted by the user-specific device transition probability - possibly because the overwhelming majority of users in the study who used more than one device used two). Suggests opportunities for further work including a qualatitive study investigating the reasons for device transitions and the physical way in which they happen, and a similar quantitative study investigating device transitions between search sessions, rather than individual queries.
Interesting cites:

  - Previous work on multi-device usage behaviours:
    - [Characterizing and supporting cross-device search tasks](http://dl.acm.org/citation.cfm?id=2433484) (Wang, Huang and White 2013)
    - ["It's on my other computer!": Computing with multiple devices](http://dl.acm.org/citation.cfm?id=1357177) (Dearman and Pierce 2008)
    - [Working overtime: Patterns of smartphone and PC usage in the daty of an information worker](http://dl.acm.org/citation.cfm?id=1560039) (Karlson, Meyers, Jacobs, Johns and Kane 2009)
    - [Mobile taskflow in context: A screenshot study of smartphone usage](http://dl.acm.org/citation.cfm?id=1753631) (Karlson, Iqbal, Meyers, Ramos, Lee and Tang 2010)
  - [Good abandonment in mobile and PC internet search](http://dl.acm.org/citation.cfm?id=1571951) (Li, Huffman and Tokuda 2009) - 'Good abandonment' - where a user's information need is satisfied without needing to access a resource is mentioned in passing, and isn't something I'd considered as an outcome of an IR task before. This paper expands on this.

## Topic-by-Topic activity estimation for knowledge work lifelog (Okamoto 2014)

Report on a prototype lifelogging application to assist knowledge workers in reviewing their activities. Builds on prior work by the same researcher, incorporating topic-modelling (with Latent Dirichlet Allocation) over the lifelog to generate annotations for summarisation and querying.
Cites:
  - [Annotating Knowledge Work Lifelog: Term Extraction from Sensor and Operation History](http://dl.acm.org/citation.cfm?id=2064025) (Okamoto, Watanabe, Nagano and Cho 2011) - previous work by same authors on which this project builds
  - [Switch Detector: An activity spotting system for desktop](http://dl.acm.org/citation.cfm?id=2063947&dl=ACM&coll=DL&CFID=504937992&CFTOKEN=15067425) (Mirza, Chen, Chen, Hussain and He 2011) - Related prior work
  - [Detecting and correcting user activity switches: algorithms and interfaces](http://dl.acm.org/citation.cfm?id=1502670&dl=ACM&coll=DL&CFID=504937992&CFTOKEN=15067425) (Irvine, Bao, Goodman, Kolibaba, Tran, Carl, Kirschner, Stumpf and Dietterich 2009) - Related prior work

## [Kraken.me - Multi-Device User Tracking Suite](http://dl.acm.org/citation.cfm?id=2638728.2641307) (Schweizer and Schmidt 2014)

Introduces [Kraken.me](http://kraken.me) - a suite of tools for activity tracking across devices, including information from soft and physical sensors, as well as social information about users. Argues for a holistic approach to lifelog data collectio in order to allow exploratory work to be carried out in the future. Also lays out an number of possible future research directions using the data they plan to gather.
Cites:
  - [Evaluation and analysis of users' activity organization](http://dl.acm.org/citation.cfm?id=800045.801580) (Bannon, Cypher Greenspan and Monty 1983) - Early study showing the usefulness of interaction histories for research, using shell command history.
  - [Interaction Data Management](http://link.springer.com/chapter/10.1007%2F978-3-642-23863-5_41) (Schmidt and Godehardt 2011) - Previous work by same authors on desktop activity logging.
  - [CAAD: an automatic task support system](http://bid.berkeley.edu/files/papers/chipaper736-rattenbury.pdf) (Rattenbury and Canny, 2007) - Prior work on clustering on soft-sensor data to identify activities
  - [UICO: An ontology-based user interaction context model for Automatic Task Detection on the Computer Desktop](http://dl.acm.org/citation.cfm?id=1552270) (Rath and Lindstaedt 2009) - More prior work on activity recognition with machine learning
  - [Attention Please! Learning Analytics for Visualization and Recommendation](http://dl.acm.org/citation.cfm?id=2090118) (Duval 2011) - Use of Activity Logging for Technology Assisted Learning

## [Switch Detector: An Activity Spotting System for Desktop](http://dl.acm.org/citation.cfm?id=2063947&dl=ACM&coll=DL&CFID=504937992&CFTOKEN=15067425) (Mirza, Chen, Chen, Hussain and He 2011)

A novel algorithm for detecting activity switches on desktop computers, along with empirical analysis via a user study. Works by grouping all pairs of individual actions where the time between them is less than to the weekly average for that user and application. This approach is justified by empirical evidence gathered from activity logs. Results show an improvement over prior work and baseline in empirical study, but the significance of this is not reported.
Cites:
  - Prior work on activity detection, based on content and behavioural features but ignoring temporal aspects:
    - [Real-time detection of task switches of desktop users](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.138.2689) (Shen, Li and Dietterich 2007)
    - [SWISH: Semantic analysis of window titles and switching history](http://research.microsoft.com/apps/pubs/default.aspx?id=54886) (Oliver, Smith, Thakkar and Surendran 2006)
  - [Frequency-based detection of task switches](http://rahulnair.net/files/Nair%20-%20Frequency-based%20detection.pdf) (Nair, Voida and Mynatt 2005) - Prior work on temporal methods of task-detection, uses a simple moving average over a 5-minute window, and used for comparison in the evaluation section of this paper.
  - [Evaluating personal information management using an activity logs enriched desktop dataset](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.153.7840) (Chernov, Demartini, Herder, Kopycki and Nejdl 2008) - Previous work on activity logging, on which the activity logging software used in this paper was based.

