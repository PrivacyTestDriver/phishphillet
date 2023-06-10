---
layout: post
title:  "Verify a Phish"
author: mainphish
tags:
  - content
  - phish
categories: 
  - blog
---

This is a plain simple phishing email. No attachments and the link to
the site where you are supposed to either give your info to or be compromised,
or both, looks rather innocent. Contrary to some previous examples, its
simplicity is elegant.

<pre>
From: Postmaster Report <postmaster@compromised.site.org>
To: mailing-list-manager@compromised.site.org
Date: May 25 2023 20:53 -0400
Subject: [Mailing List] Notification: Email Verification Required

                                 Attention :
      Your email account mailing-list-manager@compromised.site.org is currently marked inactive.
     To avoid account shut down kindly verify your email and password to
   complete verification now.
                               [1]VERIFY EMAIL
   This service is free of charge
   compromised.site.org  (c) 2023 All rights reserved

References

   1. https://gokinggroups.com/webmail-verification/Universal.html#mailing-list-manager@compromised.site.org
</pre>

## How to know it is a phishing email

Before you ask, there are some dead giveaways this is a phishing email

- That trademark of scam messages, be them phishing or fake job offers or
whatever, the notorious `kindly` is there. These phishers just cannot let
it go...

- `verify your email and password to complete verification now.` Sounds
like that line was provided to us by the Redundant Department of Redundant
Redundancies (RDRR).

- Urgency is also a trademark of phishing emails: don't give time for the
mark to think. 

- This service is free of charge! At first I was going to make fun of that, 
since I would expect any verification to be free, but then I learned that
Yahoo Mail charges for customer support. Still, since they are not Yahoo...

- The website they put together (it is down already; they are not designed to
be up for a long time) is trying to phish the credentials of the mailing list
administrator account. I wish I had thought on saving that website for later
analysis, but I was already in my pajamas. But, from the email link, we can see
the code is, as it indicates, universal: you pass the username you want to
steal the password from and it creates a website asking for it. 
No matter what you say, it is nice and clean.

This phishing email is proof that you do not have to go out of your way or
scream your lungs out to phish some credentials out.
