---
layout: post
title:  "Not a Phish"
author: mainphish
tags:
  - content
  - phish
categories: 
  - blog
---

We talk a lot about phishing emails. After all, this is what this site is
all about (teaching how to recognize and deal with them). Thing is, we 
receive so many (ok, maybe not me, which is why I keep asking for you to
send me some), we may start labelling any supicious emails as phishing.
That would be a myopic of me; messages trying to con people, spam included, 
predate emails. And, spam started to pollute mailboxes everywhere as soon 
as the internet stopped being the domain of researchers and started being
used by normal people to share animations of dancing hamster.
It took decades after that before phishing was a thing.

In hommage to its long and notorious history, and to the fact I received
the emails in question earlier today (and did not have a good phishing
email to talk about), today we will talk about another kind of
unwanted email: good ol' spam.

<img src="/images/2023/phish17.png" 
class="align-center" alt="[Two spam emails: same content, different address
in the From: field]">

In the image above I show that we have not one but two spam emails. 
And they were sent within 10 minutes
from each other. Here is the text version of the emails:.


<pre>
From: fake account
To: Clueless Phish
Date: Jun 23 2023 16:23 
Subject: Re: UNIX Users List

Hi,

I would like to know if you are interested in reaching out to UNIX Users List?

We also have software users of : Oracle Linux, Ubuntu Linux, Red Hat Enterprise 
Linux (RHEL), SUSE Linux Enterprise Server, IBM AIX and many more upon 
response.

List includes: Business Name, Client Name, Title, Verified Email Address, 
Physical Address, Phone Number, Fax Number, Web Page, Industry, Sic Code, 
Revenue Size, Employee Size, LinkedIn etc…

Please let me know your targeted criteria by filling the empty spots below.

Criteria:
Software? (For Example: UNIX, Oracle Linux, Ubuntu Linux etc...)
Job Title? (For Example: CEO, COO, CFO, VP, Directors Etc... Whom do you want to contact)
Geography? (For Example: United States, United Kingdom, Canada etc. From which 
country you needed)

I could then come back to you with the enriched contacts availability & pricing.

Regards,
Fake Account - IT Data Coordinator

To Opt-Out, please answer with Remove in the Subject Line
</pre>

## How to know it is a phishing email

- First of all, both emails have the same content, word by word, and 
differ only by the email they were supposedly sent from 
(two different domains). If that does not say suspicious, I do not know
what will.

- As mentioned earlier, they were sent within 10 minutes from each other.
Just this and the previous bullet is enough to say "not the kind of email I want to click on."

- The `Subject:` starts with a `Re:` as some spam filters will *ass*ume it
is a reply to an ongoing thread, and should not rank it as malicious or at
least suspicious. I do not know how effective this is nowadays, but it is
cheap to try ir.

- They could not be bothered with a proper salutation. That would mean 
they are just machining gun everywhere and hoping for the best.

- Their use of grammar is typical of badly put together phishing, spam, and
other malicious email: *atrocious*. If you just look at the items under
**Criteria** you may think "it almost makes sense" but still will scratch
your head. This spammer decided to go one level up: I present you la creme 
de la creme:

``` 
I could then come back to you with the enriched contacts availability & pricing.
```

I have not seen the butchering of the English language done so superbly 
as here. My ears are still ringing?

## Why are you talking about spam in a phishing awareness website?

- While the email is just spam, what comes after that if you do reply to them
asking for more info may lead to identity theft and other activities better
placed under the phishing umbrella. Not the email, but what follows it.

- The way you handle them -- not clicking or replying to it -- is the same
for both.
