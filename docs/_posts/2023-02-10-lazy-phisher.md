---
layout: post
title:  "Lazy Phisher"
author: mainphish
tags:
  - content
  - phish
  - image
  - attachment
  - PDF
categories: 
  - blog
---
A while ago we praised a phisher who had some pride on his profession. 
Those are a rare breed; most of them are lazy, unmotivated, non-creative types
who only care about meeting their quotas. You probably have met them
at work, at the department of motor vehicles, or tax services: they are they
type of people who would deflate a balloon by just walking into the room.
Unfortunately today's example belongs to this mediocre majority:

<img src="/images/2023/phish9.png" class="align-center" alt="Mediocre phishing email with payload">

Text version:
<pre>
Date: Jan 24, 2023, 10:29
From: harveyfcarberryl879@gmail.com
To: Clueless Phish
Attachment: pdfFiles_DIGIB1LL4257.pdf
Subject: DIGI-B1LL#1111 #QKCS13669476 of renewal

    Dear customer,
    Thanks for your renewal with us, your product has been updated,
    79268154 (invoiceID)

    Thank you
    Team Bills
</pre>

It is really hard to comment on this email because it screams phishing, and
not in a good way:

- I know that the email addresses used by the attackers are throwaway ones, 
  but couldn't they bother to disguise it a bit?
- *Team Bills*? I know they meant "Billing Team" and probably are not
  English speakers, but this feels like they translated one word at a time
  and hoped for the best. Searching online would have solved this.
- Yes, it has the old malware-in-attachment technique, whose filename
  does not match the subject (both mention a "*DIGIBILL*" with distinct 
  numbers)
- Was my mything product updated or renewed? Or perhaps took off in a flying
  saucer? Get your story right, dude!

I really want to find this phisher and shout "*what is wrong with you?*"
Is this guy a contractor found at elancer or full time worker?
What kind of training is his manager providing?
