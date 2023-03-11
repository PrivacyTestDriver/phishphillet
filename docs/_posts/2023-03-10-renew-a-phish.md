---
layout: post
title:  "Renew a Phish"
author: mainphish
tags:
  - content
  - phish
  - image
  - link
categories: 
  - blog
---
Today (it is still Friday) I received this more clever variation of the 
ol' invoice phishing email. 

<img src="/images/2023/phish12.png" class="align-center" alt="Phishing email with malicious attachment">

Text version:
<pre>
Date: Fri, Mar 10, 2023 at 1:22 PM 
From: Cg Vh <cgvh622@gmail.com>
To: Clueless Phish
Attachment: 
Subject: Renew your membership now for big savings ( DEWUIY-23797 )

Thanks

[Malicious Attachment "Renewal details # 3729792.jpg"]
</pre>

At first glance it has enough clues for us to know what they are up to

- The email address is a dead giveaway, specially if
you glance *but do not download* the attached "invoice" showing the 
GeekSquad logo. GeekSquad has its own domain and would never use an email
address whose username looks like the output of a cat walking on the keyboard.
- The `Subject:` of the email is classic for this kind of email.

The clever touch is that they made the invoice a jpg file instead of the
usual pdf or word doc. Don't get me wrong: there are ways to hide malware in
that (I have not sat down to inspect the file yet, so I am going from the
standpoint these phishers are clever until proven wrong), but the 
malware detection products out there (should) know how to find them in
the pdfs and Microsoft Office docs, not in an image. Case in point, you can
see that gmail claims it is ok:

```bash
Attachment scanning in Gmail
To help protect your inbox, Gmail blocks attachments when malware 
is detected. You should still only download attachments from 
people you trust. Learn more [Link]
```

As a result, someone may think "*hmmm, gmail said is ok, and I can barely see 
what this is all about. Let me download it and open it. 
What could possibly go wrong?*"

<img src="/images/2023/whatcouldgowrong.gif" class="align-center" alt="What could possibly go wrong?">

Your virus scanner will **not** flag it either. But, depending on which program you use to open it, malware is unleashed.

Clever girl.
This is an example why I asked for your phish, or potential phishes:
if it looks suspicious, let someone like me who enjoys tearing them apart
investigate.
Fun fact: 
I downloaded it, and it is 1.6 MB. That is a bit much for an invoice.
But, so far I have not setup an environment where I feel comfortable enough
to examine it.
