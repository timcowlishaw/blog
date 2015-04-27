---
layout: post
title: PhD week 1:  19th-24th April 2015
---

I haven't written anything here for ages, but a lot's been going on. I've moved
house, done lots of interesting work (with [data.gov.uk](http://data.gov.uk),
[Retechnica](http://retechnica.com), and the
[BBC](http://www.bbc.co.uk/rd)). However, my biggest piece of news is that
I've begun a PhD at [University College London](http://ucl.ac.uk), working with
[Emine Yilmaz](http://mediafutures.cs.ucl.ac.uk/people/emineyilmaz/) in the
[Media Futures](http://mediafutures.cs.ucl.ac.uk/) group. My research
proposal is as follows:

> **Lifelogging**: The practice of automatically recording aspects of one's own daily life and activities, leads to some interesting opportunities in information retrieval - including challenges related to search and discovery of the lifelog data itself, as well as the use of this data to help satisfy other information needs. More specifically, it seems likely that lifelog data could provide a valuable source of information about the context of a users information needs. Since information needs and information-seeking behaviours have been shown to be significantly influenced by contextual factors, we propose that incorporating data from lifelogs into information retrieval systems ought to lead to increased accuracy and user satisfaction. Given this, the primary goals of this project are to (1) develop lifelogging systems that can log and categorise all the activities of a user while using a computer, and (2) develop information retrieval systems that can use this information to improve accuracy and user satisfaction.

My research sits at the intersection of Information Retrieval, applied Machine Learning and Human Computer Interaction, and my topic certainly seems like a pretty fertile domain for research in all these areas. Very exciting!  I'm going to revive the week-notes habit I tried to get into last year, as I think the discipline of writing up my activities every day will help keep me focused on my research and help me measure my progress, as well as providing some much needed practice at written communication of my reasearch, and an opportunity for critical self-reflection. So, with that in mind, here's what I've been up to over the last week.

## Lifelogging literature review

This was a bit of a false start in some respects, but also very useful in others - Emine and [Filip](http://research.microsoft.com/en-us/people/filiprad/) (a researcher at Microsoft Research with whom I'll also be working) suggested I start with [this paper](http://research.microsoft.com/apps/pubs/default.aspx?id=130843) and work my way out through the citation graph, with particular focus on inbound citation references from the last couple of years, in order to get a good overview of the state of the art in our area. However, it's become fairly apparent that the term 'Lifelogging' is overwhelmingly used in the literature to refer to uses of wearable cameras for capturing everyday life, which isn't necessarily our focus, meaning we perhaps have to dig a little deeper to get an overview of current work that's more specifically relevant to our interests. That said though, there's still a lot of value to us, even though the application domain is rather different - the Sellers and Whittaker paper linked above is a great overview of HCI-focused work in the field, with valuable links to relevant material in the psychology literature, and to experimental results on the effectiveness of lifelogging in supporting various information retrieval tasks. It also proposes a useful taxonomy of information needs that can be supported by life-logging applications (The "five R": Recollecting, Reminiscing, Retrieving, Reflecting and Remembering Intentions), and some valuable design principles for lifelogging applications backed up by experimental evidence. In addition, [Doherty and Caprani 2011](http://doras.dcu.ie/16460/) contains some useful work on identifying classes of human activity from visual lifelogs, in particular an experimental process for evaluating lifelog data that could be very easily adapted to our purposes. Also, [Bolaños, Gorolera and Radeva 2013](http://dl.acm.org/citation.cfm?id=2506032) apply Active Learning to data recovered from lifelogs, which is an area of particular interest. I've now got another list of papers which are more closely related to our research interests (the use of contextual information about computer and mobile device use for information retrieval purposes) which I'll be working through this week.

## Screen-scraping Google Scholar

I've written a little iPython notebook to grab all the papers that reference a specific one and spit out some nice structued JSON. I've then been able to use this to get a broad overview of the field - ranking papers by a weighted average of recency and number of citations for instance, or investigating which researchers commonly co-author papers. While this initially seemed like a bit of a yak-shave, it's certainly been useful in the initial stages of my literature review in order to get an idea of where in the literature I should be focusing my attention.

## Having a play with Swift and Cocoa

I spent a couple of hours playing arond with Swift and Cocoa with a view to writing a lifelogging / time tracking utility for Mac OS X which I can use in the spirit of eating my own dogfood (I already use RescueTime, but I'm not yet convinced it quite covers the same use-case, for reasons I'll go into in detail another time). This was a really interesting experience - Swift is a very well-thought-out language with a lot of features that appeal to me personally (Strong static types, An optional value type), and the Xcode toolchain is excellent. There's perhaps a slight paucity of introductory documentation (I really wanted a high-level overview of how a Cocoa app is structured, and had to do some digging to find one, eventually finding [this book](http://shop.oreilly.com/product/0636920034285.do) in the library which had exactly what I wanted), but overall, it's a pretty pleasant environment to work in.

## Other things:

  - I finished my [Contributoria article](https://www.contributoria.com/issue/2015-05/551000321045c8eb71000132) on [Digital Public Space and the Right to the City](http://blog.timcowlishaw.co.uk/2015/04/27/digital-public-space-and-the-right-to-the-city/)
  - I came across [the lifelogging task](http://ntcir-lifelog.computing.dcu.ie/) at the [NTCIR conference](http://research.nii.ac.jp/ntcir/index-en.html) that looks interesting and potentially very relevant to my research. Am keenly awaiting further details!


## This week:

 - Further literature review - I'll post my detailed notes on each paper I read at the end of the week
 - Some Machine Learning revision - [Manisha](http://www0.cs.ucl.ac.uk/staff/M.Verma/) and I are both going to read a chapter a week of [BRML](http://web4.cs.ucl.ac.uk/staff/D.Barber/pmwiki/pmwiki.php?n=Brml.HomePage) (This week, Linear models!) and get together for  a chat every Friday to talk through what we've learned.


