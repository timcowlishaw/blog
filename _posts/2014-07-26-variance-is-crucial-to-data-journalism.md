---
layout: post
title: Variance is crucial to data journalism
---

[This article about the latest Retail Sales Index figures][1] on the Guardian
yesterday caught my eye as a very good example of a frequent oversight in
data-driven reporting, namely, a failure to attempt to investigate or report the
variance of a statistic. This might sound like a very dull, technical, point,
but it's of fundamental importance to the most basic level of statistical
literacy.

The guardian article reports on a fall in the retail sales index of
like-for-like sales in June vs the previous June of 0.8%, and reports (well,
speculates, but this isn't made explicit) that the cause of this fall is
concerns over an imminent interest rate rise. Aside from the rather questionable
assumption of causality (and the lack of any attempt to caveat it), there's
a deeper problem here. Namely - is that fall of 0.8% actually a fall at all?

This might sound like nonsense, but it's a really fundamental question. Whenever
we take a measurement of something, it's inherently approximate, and we can
expect, if we take multiple measurements, that they will all differ slightly.
The variance of a set of measurements measures the amount of this variation that
we see.

So therefore, it's natural to ask, is that 0.8% fall consistent with the natural
variation in the retail sales index, or is it greater, consistent with some real
change in spending habits? And the answer is, we just don't know, as the
Guardian don't say, and the [source statistics][2], are closed, available only
to paying customers.

So therefore, we've got an article that claims that consumer spending has
dropped (drastically! shoppers "put the brakes on" their spending, apparently),
as a result of negative sentiment caused by an interest rate rise. However,
without some extra data, we can't be sure whether (a) fears of an interest rate
rise really did cause this drop, or even (b) whether there was a drop at all!

Is there anything we can do about this? Well, the ONS publish a [similar set of
statistics][3], and the BRC, who produce the retail price index, helpfully
provide a [comparison of the two statistics][4], which helps us understand the
differences.

Using the ONS data, we can perform our own analysis, and maybe gain some insight
into whether the Guardian is right or wrong to have perceived a drop in retail
sales.

So, I downloaded [the data][5] and [loading it into ipython][6]. I've chosen the time
series called EAIN, representing the non-seasonally adjusted %year-on-year
change per month in value for all businesess, as this seems the best match to the BRC's
figure, based on what we know about their methodology (The BRC's
comparison notes explicitly suggests that non-seasonally-adjusted sales
values, rather than volumes are the best comparator).

Now, things get intereting - the ONS reported that this measure _grew_ by 3.4% in June 2014!

So, if we were to hastily conclude that this was a real effect (as the Guardian
did with the BRC figure), we might well come up with a headline like "Shoppers
splash out as recovery takes hold". So now, we've got two articles, with
completely contradictory messages, based on statistics that are ostensibly
measuring the same thing!

So, the natural question now, is "which one is correct?", and the most likely
answer, I think, is probably "neither". Since we've got two measurements, one
measuring a small upward movement, and one measuring a small downward movement,
it's

[1]: http://www.theguardian.com/business/2015/jul/14/interest-rate-fears-consumer-spending?commentpage=1
[2]: http://www.brc.org.uk/bis/default.asp?main_id=3
[3]: http://www.ons.gov.uk/ons/rel/rsi/retail-sales/june-2014/index.html
[4]: http://www.brc.org.uk/downloads/RSM_and_ONS.pdf
[5]: http://www.ons.gov.uk/ons/rel/rsi/retail-sales/june-2014/tsd-retail-sales--may-2014.html
[6]: http://nbviewer.ipython.org/gist/timcowlishaw/99632356b3857ff622f5
