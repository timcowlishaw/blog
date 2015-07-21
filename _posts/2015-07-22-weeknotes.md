---
layout: post
title: "Weeknotes:  4th July - 22nd July 2015"
---

For the last two weeks, I was on holiday in France!

![](https://igcdn-photos-b-a.akamaihd.net/hphotos-ak-xaf1/t51.2885-15/11352288_950985818276449_748165880_n.jpg)

I did find the time to read Don Norman's "[The Design of Everyday Things](https://www.goodreads.com/book/show/840.The_Design_of_Everyday_Things)" while
I was away though, which was a really useful introduction to the psychology of
interaction, and refresher of some basics of interaction design, and the
human-centred design process. At times I felt that he places a little too much
faith in the power of the design process to anticipate future needs and problems
(Complex systems produce emergent, unpredictable properties and effects
- something that isn't mentioned), but in general it's an excellent work.

There's only been two days since I got back, so these notes will be brief.
 I've continued to work on my desktop activity logger -
designing and building a user interface around the logging software I've
already developed, which has been a bit of a crash course in Windows GUI
programming. Not really understanding the trade-offs, I fairly arbitrarily
decided to use
[WPF](https://msdn.microsoft.com/en-us/library/ms754130(v=vs.110).aspx) instead
of Windows Forms, then subsequently realised this made it more difficult to
create a system tray icon, since this is a Windows Forms component. happily, the
[WPF NotifyIcon](http://www.hardcodet.net/wpf-notifyicon) library provides
a solution, and after finally getting it to load ([F# does not automatically load
libraries referenced in XAML files](https://github.com/fsprojects/FSharpx.Extras/issues/159)), and working out [how to add an icon
image to a Visual Studio project](http://stackoverflow.com/questions/278943/in-wpf-how-do-i-specify-the-path-to-a-file-nested-in-a-directory-using-xaml) to, I'm now getting along nicely and hope to have the logger software finished this week.

Jiyin has started writing a server application to store the data for our study,
and I've been working on deploying it to a server for testing. We've also been prototyping
the user interface for our study participants to annotate their activity logs,
and will begin implementing that next week. We've also designed the
pre-questionnaire for the study and submitted it for ethical approval.

Interesting links: (A bumper crop since I've had plenty of time to read!)

 - [Solomon Hughes](http://www.morningstaronline.co.uk/a-f9c2-Crime-against-left-wing-thrillers#.Va5xTBNVhBe) on the proud tradition of the left-wing thriller.
 - [SE Smith](http://www.theguardian.com/commentisfree/2015/jul/06/blame-technology-capitalism-smartphones) on how technology is blamed for failings of capitalism.
 - A really useful blog post from Alex McLean on his experience [publishing the
   proceedings of ICLC as open access](http://yaxu.org/how-to-publish-open-access-conference-proceedings/).
 - An [interview with an italo disco expert on his favourite record](http://www.electronicbeats.net/rewind-an-expert-on-how-italo-disco-became-cool-again/)
 - A great essay in Jacobin on the need to make the case for a [creative,
   interesting socialism](https://www.jacobinmag.com/2015/07/russian-revolution-art-vonnegut-equality/) which echoes [many of my own thoughts](http://blog.timcowlishaw.co.uk/2015/06/15/our-politics-is-utopian-or-it-is-nothing/).
 - An [interview with Darran Anderson, author of 'Imaginary Cities'](http://www.citymetric.com/skylines/interview-darran-anderson-author-imaginary-cities-architecture-power-jetsons-1238)
 - An essay on [expertise and elitism](http://thefederalist.com/2014/01/17/the-death-of-expertise/).
 - Paul Wolinski on [Live-coding and improvisation](http://www.paulwolinski.co.uk/?p=357).
 - A fascinating bit of archive video of [my home town in the 70s](http://player.bfi.org.uk/film/watch-welcome-to-redhill-the-jewel-of-the-south-1975/#.VZ2FtzQrE-o.facebook).
 - A [critique of the aesthetics of DeepDream](http://jtnimoy.com/blogs/projects/50616707-deepdream-avoiding-kitsch), making a case for more critically engaged artistic uses of the technology.
 - George Orwell on ['Why Socialists Don't believe in
   fun'](http://orwell.ru/library/articles/socialists/english/e_fun) - a fascinating essay on utopia in politics and fiction.
 - Paul Mason's essay on the 'sharing economy' and [the end of capitalism](http://www.theguardian.com/books/2015/jul/17/postcapitalism-end-of-capitalism-begun), as well as Jacobin's [critique of it](https://www.jacobinmag.com/2015/07/mason-guardian-capitalism-new-economy-post-work/).

Music: [Intergalactic FM](https://intergalacticfm.com/) - a non stop mix of incredible disco and italo, [Richard Skelton](https://open.spotify.com/album/4m6zYEEfGTMEF9hQls3ZBj) (and his '[The Inward Circles](https://theinwardcircles.bandcamp.com/album/belated-movements-for-an-unsanctioned-exhumation-august-1st-1984)' alter ego) and [Chrononautz](http://thequietus.com/articles/18314-chrononautz-noments-stream).

