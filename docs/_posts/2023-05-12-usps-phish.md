---
layout: post
title:  "USPS Phisher"
author: mainphish
tags:
  - content
  - phish
  - image
categories: 
  - blog
---

I seem to keep being given really bad phishing emails. This one may not
be as bad as the last one, but Mr. Clueless Phisher here sure needs to go
back to phishing school.

<img src="/images/2023/phish16.png" 
class="align-center" alt="[Phishing undecided whether it pretends to be
from UPS or USPS]">

What do you want me to tell about it? It is just *there*. Let me take a break,
get some fresh air, stop rolling my eyes (it is giving me a headache), and then
see what I can talk about it.

<pre>
From: <no-reply@vcita.com>
To: <mailinglist@example.com>
Date: Apr 4 2023 16:35
Subject: Your UPS package Delivery

# Package Delivery

**Dear Customer**,
As a reminder, USPS informs you that your shipment NÂ° US/293815612 is still pending instructions from you.
-----------------------------------------------------------------------------
Confirm the payment of the home delivery costs (1,99 USD)
and the shipment of the package by clicking on the following
button:
------------------------------------------------------------------------------
Arrived at USPS Origin Facility 
 
	
                              [Send My Package]

                             Sent by UPS Delivery
                        Stuttgart, Germany | 9877655651
                              infoleeet@gmail.com
</pre>


## Yeah, this one has too many giveaways...

- So, have you decided if you are [UPS](https://www.ups.com) or 
[USPS](https://www.usps.com/)? Hint: one is owned by the US government and the
other is a private company.

- It may come as a shock to you, but UPS's email address is probably not
`infoleeet@gmail.com`.

- My spidey sense also tells me they are not based off Stuttgart.

- With that said, that would explain why they are using Non-US formatting,
such as comma instead of period to denote decimal place and `NÂ` instead of
`#` (or even spell `number` out).

- The `[Send My Package]` is the link to the malicious payload. I guess it
does not look too silly when compared to the rest of the email. Thoughts?

Mr. Clueless Phisher: *what is wrong with you?* Did you skip phishing class when
they were showing how to do this kind of phishing email? 
What is wrong with you?
I really hope your mother never sees this; I can't help but imagine all the
hard work she had to do to put you through phishing school. All those long
hours she worked... and this is how you thank her?

