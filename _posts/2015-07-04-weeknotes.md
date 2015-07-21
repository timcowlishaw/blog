---
layout: post
title: "Weeknotes:  21st June - 3rd July 2015"
---

*(A bumper lot this week, as I'm off on holiday this morning and have been rather
busy getting things finished beforehand! From now on, I'm going to write my
weeknotes from Wednesday to Wednesday, in order to have them coincide with my
weekly supervisory meetings, since this is when I typically need to take stock
of my progress and plan the next week.)*

This week I've spent a load of time working on my task tracker. I'm using the
Windows accessibility API in order to listen for and log UI interactions
- however, I was having real trouble working out how to get information about
the process that fired the event. With some help from Filip (and with reference
to the code that Emine's Masters student from last year wrote for her own
study), I've finally managed to crack it, learning a hell of a lot about
PInvoke, and calling C APIs from F# in the process. I'm now working on building
a simple user interface for the logger, and am going to then leave it running in
the background for a few days (while using my windows VM for everyday tasks) and
look at the distribution of events captured in order to work out where I should
focus my efforts next. I'm also going to look into writing a version for OSX too
- since that's what I use day to day, it'll make it a lot easier to evaluate on
my own usage.

I've also reviewed the literature on exploratory search - this was prompted by
reading the findings in [one of Manisha and Emine's
publications](http://dl.acm.org/citation.cfm?id=2662076) which suggested that
the technique they were proposing performed better on exploratory queries as
opposed to focused ones. I'd been thinking about this distinction for a while
(especially with reference to [Siân Lindley et al's classification of daily
internet browsing
habits](http://dl.acm.org/citation.cfm?id=2187836.2187979&coll=DL&dl=ACM)), so
was very glad to find a way into the existing literature on the topic. [White
and Roth's book on the
subject](http://www.morganclaypool.com/doi/abs/10.2200/S00174ED1V01Y200901ICR003)
has proved to be really useful, and has tied together several disparate strands
of my current research. In particular, there's two arguments that they make that
are especially relevant to my research: Firstly, that systems which support
exploratory search behaviours should treat search behaviours as a long-term,
iterative and synergistic process (which chimes very nicely with my main
research focus - the use of holistic, long-term activity logs for information
retrieval). Secondly, White and Roth make reference to the trade-off between
Recall and Precision, and identify the fact that exploratory search requires
a higher level of recall compared to typical focused search tasks. I've been
thinking for a while about how active learning techniques could be incorporated
into search and retrieval systems, and one of the main challenges I've come
across is reconciling the user's need to be shown the most-likely relevant
results, while the active learning system requires the user to judge the
most-uncertain results  - this is roughly analogous to the explore-exploit
trade-off of reinforcement learning. White and Roth's assertion that recall
matters more than precision to users engaged in exploratory search activities is
particularly interesting in light of this, as it suggests a situation in which
the user's interests and the learning systems interest would be more closely
aligned - since the user privileges recall at the expense of precision, the
system can elicit judgements on uncertain examples without loss of user
satisfaction. This process could even be seen as a form of computer-aided
serendipity in which the user and system jointly explore the frontier of
relevance.

In other Active-Learning news, I also reviewed a [couple](http://dl.acm.org/citation.cfm?id=1101831) of [papers](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=6420837) on active
semi-supervised clustering which elicit pairwise must-link and cannot-link
constraints from users in order to arrive at an optimal clustering. I can see
a couple of challenges for my use case - in particular, my particular
application would really benefit from an online learning algorithm - since
a users activity log is longitudinal, with new activities (and new judgements)
arriving sequentially, it makes sense to use an online algorithm, rather than
re-training from scratch periodically. In addition, we can reasonably expect the
number of clusters to vary dynamically over time - while both approaches I read
about allow for the number of clusters to be inferred, the time-varying nature
of our particular problem is a little more subtle. Intuitively, the problem of
assigning interactions or resources to ongoing activities sounds a lot like
a [Chinese Restaurant Process](https://en.wikipedia.org/wiki/Chinese_restaurant_process), so I'm planning on looking into the literature on Dirichlet process mixture models, in order to see if there's anything useful there. In particular, [Andreas Vlachos](https://sites.google.com/site/andreasvlachos/) (a member of [Sebastian's lab](http://mr.cs.ucl.ac.uk/) who are also based in our office) has done some work on [active learning for DPMMs](http://dl.acm.org/citation.cfm?id=1870525), which might well be relevant here - I will look into this in the coming weeks.

Jiyin and I continued preparing for our field study - making amendments to our
ethics committee application, and working out how we will store the activity log
data we collect for further analysis. We've devised a simple schema for log
messages which incorporates all the data produced by both our loggers, and are
now working on a system to persist it. Given the log data is just a stream of
JSON objects, delivered over HTTP, I suspect [Logstash](https://www.elastic.co/products/logstash) (with the [HTTP input](https://github.com/moshen/logstash-http-input)) might well do what we need without us actually having to do any development work, which would be nice. I'll be looking into this when I'm back from holiday.
As part of the process of completing our ethics application, we also had to go
back over our proposed methodology, which highlighted a couple of shortcomings.
In particular, in soliciting task labels from users, we've opted to allow users
to describe their tasks with free text labels, in order to reflect our lack of
prior knowledge about the participants' activities. However, this has one important
drawback, in that it does not allow us to make comparisons *between*
participants, given that there's no common set of descriptors for tasks. In
order to address this, we could come up with a higher-level set of 'task
categories' shared between users, to which they can assign each task - however,
the issue then is deciding upon a principled set of categories which provides
adequate coverage. Another approach (which I prefer), would be to elicit
commonalities between participants as part of the analysis process, or in
interviews after the study. [Grounded Theory](https://en.wikipedia.org/wiki/Grounded_theory) offers a useful methodology for this, and the [Affinity diagram](https://en.wikipedia.org/wiki/Affinity_diagram) would be a useful technique to elicit task categorisations in the post-study interview. I'm going to read up more on this and formulate a more concrete methodology next week.

We had the first meeting of our office Machine Learning interest group on the
2nd, including staff and students from UCL, and BBC R&D. It was great to find
out more about others interests and activities, and to explore useful ways
of supporting each other. We decided to get started by agreeing on a paper to
read and discuss in a 'journal club' format, and to reconvene in a month. We're
still deciding on our first paper, but the general consensus was that we'd like
to go back to some of the original publications on deep learning, and develop an
understanding of it from the ground up.

Interesting links:

 - An interesting case study / tutorial on running a [high-volume web crawl on
   Amazon AWS](http://www.michaelnielsen.org/ddi/how-to-crawl-a-quarter-billion-webpages-in-40-hours/).
 - A clear and thorough take-down of some of the most common misconceptions
   about the [Greek economic crisis](http://wire.novaramedia.com/2015/06/in-defence-of-greece-6-myths-busted/).
 - Still on Greece, [Alex Andreou's thoughtful, poignant essay on the failure of
   the European ideal](https://www.byline.com/column/11/article/126).
 - A [savage critique of Silicon Valley's obsession with disruption](https://pando.com/2012/10/24/travis-shrugged/) and unhealthy
   fascination with Ayn Rand.
 - Dan W's [fascinating essay and photographs](http://www.iamdanw.com/wrote/what-are-borders-anyway/) on Baarle-Herzog - a cluster of 22 tiny Belgian enclaves within the Dutch village of Baarle-Nassau.
 - Chris Dillow on the [conflict between managerialism and innovation](http://stumblingandmumbling.typepad.com/stumbling_and_mumbling/2015/06/managerialism-vs-innovation.html).
 - A Goodreads list of [thrillers with left-leaning politics](https://www.goodreads.com/list/show/32367.liberal_left_wing_thrillers)

Music: [Petrels](https://open.spotify.com/album/0nxvx8wY0PPzfTQpNHlSFO), [Tim
Hecker](https://open.spotify.com/album/3Slfl3Ui9sRXobar6rgbKs), [Vessels](https://open.spotify.com/album/38Y2J5gBPqQYAQV1rBQwaL), [Holly Herndon](https://open.spotify.com/album/1x1agDGl1Y7npXRF7u3prS), [Lorenzon Senni](https://open.spotify.com/album/2qvFt99a5Ly9BMKFmlbhuZ), [Alessandro Cortini](https://open.spotify.com/album/4hnN6DMOe2DooMiGwWbw9n), [Fennesz](https://open.spotify.com/album/0xnL6goTzcRFKzbrleXfpF), [Some incredible South African disco](https://open.spotify.com/album/0vUxR6hsn75o2EcoyapAHo), [Laurel Halo](https://open.spotify.com/album/0dlVirw96s48bOpC7LQDNI), [Julius Eastman](https://open.spotify.com/album/7kUE7O7jfE4As66da1C4Lr), [Arthur Russell](https://open.spotify.com/album/5kFfUmxBL6eXcyABd45CDB), [Sparks](https://open.spotify.com/album/4jwO7dt0trrGu0ozSVNRgo), [Pet Shop Boys](https://open.spotify.com/album/60xS3EDuOFXLMJLSjwSUZa), [East India Youth](https://open.spotify.com/album/2li0SgHlqjpPF2gqTr5FHh) and [Shit and Shine](https://open.spotify.com/album/6VmkXYpF6yxFga498ICXnh).
