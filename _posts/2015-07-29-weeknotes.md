---
layout: post
title: "Weeknotes:  22nd July - 29th July 2015"
---

This was my first full week back from holiday, but it didn't take too long for
me to get back into the swing of things! First order fo business was to catch up
with Jiyin - she'd begun to work on a server application for our computer use
study while I was away, so we looked at that together and discussed what other
work needed to be done with it. The main outstanding piece of work is on the
user interface - Participants will need to authenticate themselves, define
a 'Todo list' for the day, and subsequently annotate their daily computing
activity with tasks from this list. We spent some time discussing and sketching
out how the User Interface could work in each of these cases. We also had a chat
about the timing of our study and ways of recruiting participants - we're in
a slight bind as many of the submission deadlines for conferences we might want
to publish at are in October, but as the undergraduate students only return at
the end of September, we might have trouble recruiting a suitable number of
participants before then! We had a chat with [John](https://www.ucl.ac.uk/uclic/people/j-dowell), my second supervisor
about this, as he works in the [Human-Computer Interaction department](https://www.ucl.ac.uk/uclic), who perform this sort
of study quite frequently and he gave us some useful advice - pointing us
towards the mailing list for masters students (who are here all summer working
on their dissertations), and the psychology department subject pool. In
addition, we finalised the design of the pre-questionnaire we'll use as part of
the study, and created a Google form to administer it.

Subsequently, I put together a quick interactive prototype of one of our ideas
for the log annotation UI, in order to test it out in something approximating
real use. This was a really useful process - for me, it's almost as quick to
knock together an interactive prototype in HTML/CSS/JS using [Materialize CSS](http://materializecss.com/) to provide a library of standard UI elements, as it would be to do the same in something like [Balsamiq](https://balsamiq.com/) or [UXPin](http://www.uxpin.com/), and allows me to quickly prototype a broader set of interactions than could be done with a standard wireframing tool. This was an invaluable process - trying out our own design and performing ad-hoc usability testing on other colleagues highlighted several shortcomings immediately, and we were able to refine our design to compensate for them.

Most of the rest of the week was spent working on my activity logger software
- I gave it a simple system tray icon user interface, and made it output the
  event log to a CSV file, rather than simply spewing information to the
console - the [WPF NotifyIcon](http://www.codeproject.com/Articles/36468/WPF-NotifyIcon#wpfapi) library, and [this blog post](http://putridparrot.com/blog/creating-a-wpf-application-in-f-a-more-complete-solution/) on creating a WPF application in F# were both really useful for this. I then let it run while I completed a few simple tasks using my Windows VM as I'd use my regular computer.

Analysing the results was very interesting, it appears the accessibility API
events are very low level - referring to the creation, deletion and ordering of
individual UI elements. Am now investigating how best to identify higher-level
user actions (such as opening an application, saving a file, or switching
between windows) from this stream. There's further metadata about the object
which fires the event (in the form of an [IAccessible](https://msdn.microsoft.com/en-us/library/windows/desktop/dd373678.aspx) object) which I'm not yet logging, so will look into that that this week, to see if there's any additional data that will help us identify higher-level actions. I'm also going to investigate methods of automatically identifying repeating patterns in these low level logs that correspond with some higher level action - I'm going to look at some of the literature on [learning](http://epublications.marquette.edu/psych_fac/58/) [with](http://www.sciencedirect.com/science/article/pii/S016794730800087X) [categorical](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.30.761) [time-series](http://arxiv.org/abs/1505.01300) here (Which sadly seems a little thin on the ground) to see if offers any clues. I've also created logs of single UI 'gestures' (minimise a window, open an application, paste some text, etc.) to use as a source of ground truth for this analysis.

I also read through Andreas Vlachos' papers
on [semi-supervised](http://www.cl.cam.ac.uk/~alk23/eacl-09.pdf) and
[active](http://mlg.eng.cam.ac.uk/pub/pdf/VlaGhaBri10.pdf) DPMM learning. His
algorithm is based on a modified Gibbs sampler, so I also did some revision on
Gibbs sampling in general - both [BRML](http://web4.cs.ucl.ac.uk/staff/D.Barber/pmwiki/pmwiki.php?n=Brml.HomePage) and [Resnik and Hardisty](http://www.umiacs.umd.edu/~resnik/pubs/LAMP-TR-153.pdf) had loads of useful background here.
Vlachos' model definitely seems appropriate to the problem at hand, as
I mentioned last week - if you view each underlying task being carried out by
a user as a probabilistic process which generates actions and resources, and
the entire activity stream as a mixture over these tasks, the DPMM seems like
a natural method of modelling it. I'll definitely look into using Vlachos's
algorithm in the analysis of my field study data, however, I can anticipate some
problems in using it (in its current form) in application - In particular, in
order to interactively cluster activities into tasks on real usage, we'd need
some way of deriving an online algorithm for Vlachos' constrained DPMM model.
This is probably a good opportunity for further research. In the coming weeks,
I'm planning to have a go at implementing Vlachos's work myself, in order to
better understand the details of how it works.

At the complete other end of the spectrum of my research interests, I've also
been reading Corbin and Strauss's [Basics of Qualitative Research](https://www.goodreads.com/book/show/2299298.Basics_of_Qualitative_Research), in order to learn more about Grounded Theory, and to prepare myself for the user activity study we're organizing. Jiyin, Emine and I have talked at some length about how we can classify computing activities at a higher level, across different users, and I'm quite keen to use a GT analysis in order to discover a high level classification that reflects users own understanding of their tasks and how they link together, and which reflects the available evidence. I'm planning to write a separate, more detailed post with my notes and thoughts from reading Corbin and Strauss soon, but in the meantime I'm particularly taken with the way that Grounded Theory appears to offer a principled *generative* process for developing hypotheses and theory from data, in contrast to the traditional quantitative scientific method's *discriminative* process for falsifying existing hypotheses and theory. In fact, I can see how the two work very naturally together - using Grounded Theory to develop and discover hypotheses for testing, then quantitative methods to formulate tests for their veracity.

Otherwise, I've read Ahmed Awadallah et al's paper on [Supporting Complex Search
Tasks](http://research.microsoft.com/en-us/um/people/sdumais/cikm2014-hassanetal.pdf),
attended a seminar by [Maria-Florina Balcan](http://www.cs.cmu.edu/~ninamf/) on
[Learning submodular
functions](https://smartech.gatech.edu/bitstream/handle/1853/31222/GT-CS-09-14.pdf)
(which was super interesting, and I can see a very obvious application of it to
the sort of query recommendation work in Awadallah's paper that I will write
about in more detail soon), and (in a very small way) helped [Jeremy Corbyn get
nominated for Labour Leader by the Walthamstow
CLP](http://walthamstowclp.blogspot.co.uk/2015/07/leader-and-deputy-nomination-meeting.html)
on Saturday (more thoughts on which are [here](http://blog.timcowlishaw.co.uk/2015/07/26/why-i-am-supporting-jeremy-corbyn-for-labour-leader/)).

**Interesting links:**

 - [A fascinating documentary](https://www.youtube.com/watch?v=y6v1VxB5Lss) on
Harold Wilson's two tenures as Prime Minister, and the extraordinary attempts
to remove him from power.

 - [Some vague but tantalising
   details](http://musically.com/2015/07/20/spotify-discover-weekly-personalised-mixtape-playlist/)
about the thnking behind Spotify's 'Discover Playlist' feature, which I've
been enjoying this week. Matt Ogle's comments on the use of algorithms that
build upon and complement human behaviour are very reminiscent of [Abigail
Sellen's ideas around 'synergy' in intelligent systems](http://blog.timcowlishaw.co.uk/2015/06/11/designing-computer-systems-that-see/).
 - Tim Harford on [the Alchemist's Fallacy and the spread of ideas](http://timharford.com/2015/07/its-tough-turning-ideas-into-gold/)
 - An excellent Jacobin essay on the [politics of the working day](https://www.jacobinmag.com/2015/07/luce-eight-hour-day-obama-overtime/), which formed a nice complement to [Sian Lindley's paper on the relationships between time and technology](http://research.microsoft.com/apps/pubs/?id=241770).
 - An example implementation of a Gibbs sampler in [functional Scala code](https://darrenjw.wordpress.com/2013/10/04/a-functional-gibbs-sampler-in-scala/)
 - A short, but very important blog post from Paul Krugman, on [Uber's two
   innovations](http://krugman.blogs.nytimes.com/2015/07/25/uber-and-the-new-liberal-consensus/?module=BlogPost-Title&version=Blog%20Main&contentCollection=Opinion&action=Click&pgtype=Blogs&region=Body) - which reminds us both that technology is not somehow beyond ideology, but that we can also embrace technological innovation in a critical way, unpacking it from the reactionary politics that all too often are tied up with it.
 - Pacheco Pereira on the [European crisis and the 'end of history'](http://www.twitlonger.com/show/n_1sn55ig?new_post=true)
 - A spellbinding [panel discussion](http://www.unofficialbritain.com/landscape-punk-to-supermarket-car-parks-unofficial-britain-live-in-stoke-newington/) hosted by Influx Press featuring Gareth E.Rees, Gary Budden, Tina Richardson and David Southwell talking about storytelling, (psycho-)geography, walking, and more.
 - An interesting look at [The Guardian's 'Creative sprint' process](https://www.theguardian.com/info/developer-blog/2015/jul/27/the-user-experience-of-creative-sprintsl)
 - A thought-provoking [essay on Markfield park, Tottenham, and the
   gentrification of London](http://newlexicons.blogspot.co.uk/2015/07/markfield-park-and-politics-of-existence.html) by Gary Budden
 - Fascinating piece on the [psychological effects of modern capitalist
   society](http://thoughcowardsflinch.com/2015/07/26/whats-wrong-with-people/),
and how they led to the rise of identity politics.
 - Interesting piece on the [millenial generation, and emergent forms of left-wing politics](http://www.thenorthstar.info/?p=12361)

**Music:** [Algiers](https://open.spotify.com/album/24hXu3nSvxjwfYbbJIG3lU0), One
track off the new [Darkstar album](https://open.spotify.com/album/5jwd3ONfalS7gjPci9I7AQ), [Wu-Tang Clan](https://open.spotify.com/album/36j7xkJKwcxBkWwdVoTvI4), Loads of great stuff on my [Spotify discover playlist](https://open.spotify.com/user/spotifydiscover/playlist/2bnesr5EaTzlQS6Nmimhbk), [In Aeternam Vale](https://open.spotify.com/album/5oFlTSiw7I6iSk3PdRSzq9), Various stuff on [Blue Tapes](https://bluetapes.bandcamp.com/album/vol-1).
