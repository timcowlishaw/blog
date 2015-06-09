---
layout: post
title: "Weeknotes:  25th - 31st May 2015"
---

### PhD ###

This week I wrote up a few potential research directions, for discussion with Emine and Filip. That discussion was really useful - helping me synthesise most of those ideas into a single focus for the next few months of my research, without becoming too defuse or losing coherence. Briefly - we're going to be looking at task identification on the desktop, using active machine learning techniques to incorporate user feedback, and have devised a series of studies to investigate the value of this, and which will hopefully get us some interesting results fairly rapidly. Next week, I'm going to begin writing up a more concrete research plan for the coming months, as well as working on the specifics of designing studies to test my research hypothesis.

I've also continued with some literature review - in particular, I've come
across the [work](https://scholar.google.com/citations?user=Oxm1HmwAAAAJ&hl=en) of [Yi Chen](https://people.aalto.fi/index.html?profilepage=isfor#!yi_2_chen) - formerly of Dublin City University, and now at the Helsinki Institute for Information Technology, who has done a lot of work on lifelogging and desktop activity tracking for information retrieval, and in particular for information refinding, with a particular focus on supporting users cognitive processes for information recall. This has been really useful, both in terms of familiarising myself with the current state-of-the-art in my field, and in terms of better understanding the psychological aspects to information retrieval - an area with which I'm currently rather unfamiliar.

Another aspect to the literature review process in general which I've noticed is
the extent to which it improves my knowledge and understanding of the research
process itself. In particular, reading reports on field and lab studies in HCI has broadened my understanding of the techniques and procedures that could be usefully applied in my own work. Additionally, I'm getting better at reading research papers with a critical eye - on encountering two similar studies seemingly reaching opposite conclusions, for instance, I'm now beginning to be able to identify differences in methodology and assumptions that account for the discrepancy, and absorb how that might impact my own work.

I think I need to improve the organization of my reading somehow, in two
respects. Firstly, I need to come up with a system for organizing how papers in
the literature are related, and how I discovered them. If I discover an
important paper through a citation in another, for instance, it's useful for
future recall (and just an understanding of my field in general) to record this
connection, somehow.  In addition, I need to make sure I record which resources
in the literature are relevant to which areas of my own research. I will look
into ways of doing this in the coming weeks. In addition, I'm not really being
very disciplined about organising material that I haven't yet read. I'm
accumulating potentially interesting references faster than I can read them, but
haven't really given any thought to prioritising these. As a result, I've now
produced an ordered 'queue' of twenty or thirty high-priority references, which
I will work through, one or two a day. This should help me get into a better
routine, as well as making sure I spend my time on the most relevant literature.

In other organizational news - I'm making a 'todo' list for the week, directly
after my supervisory meetings on Wednesday, and roughly dividing it into days.
This has had a marked improvement on my productivity, and also helps me get back
into the flow of things quickly on a Monday morning!

Other work news:

I had a useful chat to [Jiyin](https://jiyinhe.wordpress.com) about our shared
work interests and opportunities for working together. We've realised that as
well as there being several opportunities for collaboration within the group,
there's also scope for sharing data, and crucially infrastructure, between our
projects. In particular, while Manisha, Jiyin and I are working on logging information related to user activity, we've realised that the storage and analysis of this data is a shared concern, and therefore it doesn't really make sense for all three of us to individually implement storage and analysis tooling for our own projects. Therefore, we're gathering use cases from our own work with a view to designing and building a shared data store for all our projects, and a common protocol to talk to the software we each develop for our studies. More personally, this has also been really useful in helping me understand how my own work will fit into the shared interests of the group, and has given me a better understanding of the form my own work will take, through observing how more experienced researchers go about theirs!

I've also had some time this week to continue my reading of
[BRML](http://web4.cs.ucl.ac.uk/staff/D.Barber/pmwiki/pmwiki.php?n=Brml.HomePage),
I've now completed the chapter on linear models - which while also helping me
revise material with which I'm already familiar, also helped deepen that
knowledge and put it on a more rigorous footing. From here I'm planning to look
into methods of extending Support Vector Machines to output well-calibrated
probabilities - [Platt Scaling](http://en.wikipedia.org/wiki/Platt_scaling), and
[Relevance Vector Machines](http://en.wikipedia.org/wiki/Relevance_vector_machine) to name two.
Next, however,  I'm going to dive into the BRML chapters on Bayesian linear
models and Gaussian processes (which in turn should help me with Relevance
Vector Machines in the future).

### Interesting links and other reading ###

* [http://pandaproject.net/](PANDA) is an open-source, searchable newsroom database. Having worked with [BBC News Labs](http://www.bbcnewslabs.co.uk/) in the past, I'm really interested in applications of my research to journalism and news gathering in particular, and have been thinking about opportunities for research in this direction. It's encouraging that others in the open-source community are thinking about newsroom information needs specifically and developing tools to support them, and might also be a good opportunity for a future collaboration?

* [Fetching](http://fetching.io/) announced the public release of their API, and
  I've got in touch to request a key and introduce myself, with a view to
explore opportunities for collaboration - I've been using their self-hosted
version for a couple of months, and it's really useful for refinding previously
seen information on the web.

* [Paul Krugman](http://www.nytimes.com/2015/05/25/opinion/paul-krugman-the-big-meh.html) wrote a great short piece on reasons to be skeptical of over-exuberant claims about the effect of technological progress on the economy

* [This essay](http://www.buzzfeed.com/whyman/the-kebab-shop-cat-tweet-and-the-inauthenticity-of-hv17) on content, experience, and the [kebab shop cat tweet](https://twitter.com/thwphipps/status/545882463911030784) is both the first time I've seen Walter Benjamin quoted on Buzzfeed, and an exellent thought-provoking examination of the social role of 'viral' content.

* [Ich Bin Capital](http://motherboard.vice.com/read/i-am-capital) - a piece on
  the economics of personal data and how our identies are becoming commodified,
that makes many of the points I was getting at in my [Right to the Network](http://blog.timcowlishaw.co.uk/2015/04/27/digital-public-space-and-the-right-to-the-city/) essay in a far clearer and more powerful way.

* [A fascinating story](http://www.qsl.net/n1irz/woodpeck.html) (via [Simon](http://www.polkaspots.com/)) about how radio hams in the 1970s 'ganged up' to disrupt a Soviet radar system.

* [Robert Clayton's series of photographs](https://i-d.vice.com/en_gb/article/estate-post-industrial-ruin-at-the-end-of-thatchers-britain) of a Birmingham council estate in 1991 - A poignant reminder of what's changed and what's stayed the same in post-industrial Britain

* [Socialist in the city](https://socialistinthecity.wordpress.com/2015/05/30/greece-buy-stocks/)'s post on why the Greek bailout is an issue of existential importance to capitalism and the finance industry in that it represents a collision between democracy and financial obligations.

* [An interesting piece](http://www.electronicbookreview.com/thread/firstperson/serial) on The Wire (which I'm half way through watching again)
  and its relationship to other forms of media - the novel and the video game,
as well as the tension between the institutions and indivuduals depicted by it
(I love the idea that it departs from the classic heroic cop show, in which
brave individuals triumph over adversity, by depicting all individuals as
essentially lacking agency - being blown around by the forces of the flawed
institutions of which they're a part. In David Simon's words: "The town is what
it is.")

* A blog post that really chimed with me on the [nonsense of 'aspiration'](http://labourelection2015.com/2015/05/25/labour-leadership-contenders-aspiration-isnt-enough/) in political discourse - making the point that aspiration by definition ccorresponds to *unrealiseable* ambitions and goals, rather than achievable ones, and achieves it's rhetorical power precisely through it's unattainability.

* The always-excellent Chris Dillow on [What Labour can learn from Dave
  Brailsford](http://stumblingandmumbling.typepad.com/stumbling_and_mumbling/2015/05/the-brailsfordian-road-to-socialism.html) and the importance of democratic decision making and incremental improvement.

### Music I have enjoyed ###

This week I have mostly been listening to: [Prurient](https://open.spotify.com/album/5Pm2WvqxlDttK4hTx1vKe3), [Blanck Mass](https://open.spotify.com/album/2f6y5TjWHIuaiBY9A2ZtHm), [Leafcutter John](https://open.spotify.com/album/5Zrj1vEGuuxveRvKh01FaW), [Colin Stetson and Sarah Neufeld](https://open.spotify.com/album/5XWTi7aJnVcihhmN3vGqwD), and [Holly Herndon](https://open.spotify.com/album/1x1agDGl1Y7npXRF7u3prS).
