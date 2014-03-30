---
layout: post
title:  "How do spammers harvest your e-mail address?"
date:   2014-03-26 17:00:00
---

This is an update on the research I did under the guidance of [Jeff Huang](http://jeffhuang.com/) (now assistant professor at Brown University) titled [How do spammers harvest your e-mail address?](https://experiment.com/projects/how-do-spammers-harvest-your-e-mail-address).

-------------

As an experienced ex-blogger and an avid internet marketer, I can firmly say that every Internet user with an email address has received spam email more than just once. Spam is not just unsolicited, unapproved contact by a stranger; sometimes spam can lead to loss of money and even theft of identity. As spammers get more sophisticated, it becomes difficult for anyone to differentiate spam emails from genuine emails. Companies all across the world, irrespective of their market, location or size, incur loss of resources, human power and money due to spam. Tech companies, like Google and Yahoo, use about 30 billion watts of electricity (1) - that's enough electricity to power 3 million houses for a year. It’s amazing just to think about how much energy and money these companies would save if there was no spam. 

But it's not just the companies that suffer losses from email spam. People like you and me are spending a lot of time reviewing spam, and even with strong spam filters they still have to check their spam folder for misclassified email. Everyone has had the problem where an important email fell into the spam folder. 

<iframe title="Why this research?" width="480" height="390" src="https://player.vimeo.com/video/40080540" frameborder="0" allowfullscreen></iframe>

Back in August 2012, I stumbled upon this amazing research opportunity presented by the Information School at the UW – to be a part of the research to find out how spammers harvest peoples' email addresses, and how it can be prevented. I instantly related to this research since I have been at the receiving (and sadly, sending) side of spam emails, and I understand what a spam email really costs – nothing to the sender, a lot to the receiver.

I was super excited to get started with this research project. We were super lucky to be funded early on [Experiment.com](https://experiment.com/home) and I worked on this for about a year. We were looking at the root of the problem - how spammers get your email addresses in the first place. To make a medical analogy, there is treating the illness after it's already happened, and there is learning more about the root cause of the illness so it can be prevented completely.

Now, there have been many such studies in the past (see *References* below), so how is this study different from the others? For one, this is new, raw data we collected. The Internet space moves so fast, that to be ahead of spammers and scammers, you have to find out how they operate - and how they operate changes all the time. Secondly, most other (newer) studies are not as comprehensive as this one is. They usually just cover social network spam, or sites selling email lists. We tried to cover as much ground as possible, and collect as much data as possible to back us up.

So, here are the results we got after one year of waiting and after posting email addresses to numerous different types of websites and online services.

#### First, a cloud.

![](http://i.imgur.com/bMsibZ2.png)

This is a simple cloud of the words spammer use the most in their email subject lines. The most used words, as seen, are "free", "credit", "score", "home" etc. I expected "viagra" to be one of the top words, but I guess they are not using it in subject lines to bypass spam filters.

### And now, the meat of the study. Or should I say the spam. ;-)

#### First, where is our data coming from?

Emails were posted to a variety of different platforms in different quantities. Each email was only posted once on the web to make sure we get very pristine data.

![](http://i.imgur.com/JArs4V7.png)

A human-readable list of the platforms with the number of emails posted there:

* App store reviews (Apple, Chrome, Firefox etc): 4
* Blog comment: 119
* Blogging site (wordpress, blogger etc): 142
* Craigslist discussion board: 6
* File hostedon Dropbox: 12
* Ecommerce sites like Amazon: 5
* Facebook profile, wall and pages: 5
* File on server: 21
* Forum profiles: 234
* Github: 1
* Google doc: 7
* Google drawing: 2
* Greeting card generator sites: 18
* Guestbook: 12
* Loyalty Programs: 10
* Mailing list: 85
* \<meta> tags of websites: 4
* Other social networks: 5
* PDF on server: 8
* Paste sites like Pastebin: 21
* Reddit: 9
* Scribd: 10
* Slideshare: 5
* Spammy mailing lists: 51
* Twitter: 2
* UW Directory: 1
* Usenet: 98
* Video site (YouTube video description/title): 53
* Whois: 5
* Wiki sites: 84
* Yahoo Answers: 25

Since we wanted to study how to prevent spam, I also tested a lot of different email obfuscation techniques, and the graph below shows the distribution of them.

![](http://i.imgur.com/BUmIAtK.png)

**([See what they mean](https://experiment.com/u/hr9x0w))**

And a human-readable list of obfuscations with the number of emails that were used for each one:

* <span> splitting: 6
* ASCII: 17
* Comment: 3
* Different Hyperlink: 114
* HTML Unicode: 45
* Image: 21
* Invalid: 260
* Invisible: 59
* JavaScript: 18
* None: 484
* ROT-13: 2
* email (at) irchiver (dot) com: 1
* email @ irchiver . com: 23
* email @ irchiver.com: 18
* email AT irchiver DOT com: 5
* email AT irchiver.com: 1
* email [@] irchiver.com: 1
* email [at] irchiver [dot] com: 15
* email [at] irchiver.com: 8
* email at irchiver dot com: 2
* email-@-irchiver-.-com: 13
* email-@-irchiver.com: 2
* email-AT-irchiver-.-com: 1
* email-AT-irchiver.com: 11
* email-at-irchiver-dot-com: 4
* email-at-irchiver.com: 2
* email[@]irchiver.com: 1
* email[@]irchiver[.]com: 12
* email[at]irchiver.com: 2
* email[at]irchiver[.]com: 2
* email[at]irchiver[dot]com: 17
* email[at]irciver.com: 2
* iFrame: 2

I also tried some different ways of spreading email, like making email anchored vs plain text or clickable vs bare text.

![](http://i.imgur.com/cw4CaoM.png)

![](http://i.imgur.com/g35oRQy.png)

So what's an anchored email link? [This](karan@goel.im). And what's not? This -> [karan@goel.im](karan@goel.im). In some cases, for example when emails were embedded in images, it's not valid. That's "invalid".

The way we classified emails as "clickable" or not follows almost the same rules - [this](karan@goel.im) this clickable but karan@goel.im is not.

#### How how much spam did we get, and when?

At the time of producing these charts, we got about 18000 spam emails across all 1000-ish emails posted.

[![](http://i.imgur.com/eReQyI0.png)](http://i.imgur.com/eReQyI0.png?1)

As seen in the graph, the amount of emails per week peaked after 20 weeks. This 20-week period could be the time interval it took search engines to crawl, index and rank the pages where these emails were posted.

Also see the [gallery of charts for emails per week by different platforms](http://imgur.com/a/VMN7F#0).

[![](http://i.imgur.com/nIm5Tp5.png)](http://i.imgur.com/nIm5Tp5.png)

As seen in the timeline above, there's an influx of weekly spam in late October (that's 2 months after the study began), and during the holiday season. These were the times when email posting activity was at its peak, so seeing more spam is expected.

The weekly activity of spammers seems pretty consistent and not surprising. Early weekdays are busy, but activity settles down a bit on the weekends.

[![](http://i.imgur.com/cHwTD90.png)](http://i.imgur.com/cHwTD90.png)

Not many people check their emails on weekdays, so no point in wasting bandwidth, right?

#### Platforms

As seen in the box plot below, almost all [platforms](https://experiment.com/u/ocVekA) I posted to sent spam - whether they were publicly indexable by search engines or not, every website has the potentiable to be scraped by spammers.

[![](http://i.imgur.com/I2U8KSj.png)](http://i.imgur.com/I2U8KSj.png)

Notably, spammy mailing lists send the most spam. These mailing lists include sites that promise you free credit scores, or insurance quotes, or free ipads etc. These sites stink of spam, but people still continue to give them their email addresses.

Surprisingly, emails in whois details of a domain also sent a ton of spam, even though most whois services hide emails as an image. Why is that? Because those sites that do not obfuscate email addresses are enough for spammers to harvest emails from.

##### Some platforms that sent no spam at all:

- App Store (Email posted in reviews)
- Ecommerce (Used to sign up on sites like Amazon)
- Facebook (In page description and profile - all public)
- File on server (A txt file hosted on my own server)
- Google doc
- Google drawing
- Twitter (Email in a tweet)

#### Obfuscation

(I can finally spell this word!)

I used [a ton of obfuscation techniques](https://experiment.com/u/hr9x0w))) to test as many of them as possible.

[![](http://i.imgur.com/2HYF2XS.png)](http://i.imgur.com/2HYF2XS.png)

Simple name mangling (*email [at] irchiver.com* etc) works no more, sadly. Some more modern ways do work - ROT13, ASCII characters etc seem to work the best. To use them, though, you have to use scripts or software which might not be always available.

##### Obfuscation strategies worked the best and sent no spam at all:

* `<span>` splitting (In HTML, parts of email in different `<span>` tags)
* ASCII (Covert email characters to ASCII)
* HTML Unicode (Convert email characters to unicode)
* Image (Post email as an image)
* ROT-13 (A character shift algorithm)
* email (at) irchiver (dot) com
* email @ irchiver . com
* email [at] irchiver [dot] com
* email-@-irchiver-.-com
* email-AT-irchiver.com
* iFrame (Post email on one page, and embed in iFrame in a different page)

#### So how should I share my emails online?

I'm glad you asked. Our study indicates that spammers are getting more and more sophisticated, and getting access to even private pages and databases to harvest emails from. Their parsers work better than ever, and simple email mangling is just not as efficient now.

So is there no way to beat spammers? Of course there is.

- If you're posting an email address on a website whose source code you can control, use a [cipher](http://en.wikipedia.org/wiki/ROT13) or [ASCII](http://www.asciitohex.com/) or [Unicode](http://www.asciitohex.com/) encoding. This makes your email look like normal text, but the source is nothing like normal text.

- If it looks too good to be true, avoid it. Trust me. No one will give you a free iPad in exchange for your email address. Huge databases of emails are built and sold this way, so once you are in the loop, it's almost impossible to prevent spam.

- Make your email unscannable. Canonical email scraper simple scrape the source code of a page and look for email addresses. Use a (highly) mangled email address (like karan-AT-goel-DOT-im). This affects end-user experience since they cannot just copy-paste your email address now slighlty but saves your email from spammers.

- Keep your eyes open when filling forms. Many sites I posted to had small checkboxes at the bottom of the form, which were checked by default, but give permission to websites to send you marketing emails or in some cases send your email to advertisers. Watch out for these!

- Be careful in forums, chats and discussion boards. These are the biggest source of emails for spammers. If you must give out email address, use disposable email addresses.

- If you own domain name(s), opt for WhoisGuard. WhoisGuard avoids spam issues by placing registrar's information in whois and provides an option to redirect email and regular mail to your real address.


------

​At the end of last summer, when I was crunching the data set for interesting finding, I discovered that for some reason, some of the data was tainted by Gmail. Jeff had set a filter at the beginning of the study to redirect all email (including and especially spam) to inbox directly. However, Gmail randomly decided to not do that, and so we lost some part of the data (spam is deleted by Gmail every month). We do not know how much data we lost (I estimate about 5-10%), but it is enough to prevent us from publishing a paper. :(

I have made all scripts used to analyse the data available on [Github](https://github.com/karan/SpamHarvestUW). This code was written when I was just starting to learn Python, so please excuse the code quality.

What do you think of our research? Reach out to me via Twitter ([@TheKaranGoel](http://twitter.com/TheKaranGoel)) or via email: karan@goel.im

----------

### References:

(1) James Glanze, "Power, Pollution and the Internet" (NYTimes), 22 September 2012 <http://www.nytimes.com/2012/09/23/technology/data-centers-waste-vast-amounts-of-energy-belying-industry-image.html>

### Related work

Kyumin Lee, James Caverlee, Steve Webb, "The Social Honeypot Project: Protecting Online Communities from Spammers", 2010

Craig A. Shue, Minaxi Gupta, Chin Hua Kong, John T. Lubia, Asim S. Yuksel, "Spamology: A Study of Spam Origins", 2009

Center For Democracy & Technology, "Why Am I Getting All This Spam?", 2003
