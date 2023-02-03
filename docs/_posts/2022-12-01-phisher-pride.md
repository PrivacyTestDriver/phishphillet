---
layout: post
title:  "Phisher Pride"
author: mainphish
date:   2022-12-01 21:23:30 +0000
tags:
  - content
  - image
  - phish
categories: 
  - blog
---

We continue our series on phishing emails. I am glad to say a phisher heard 
my plead and stepped up to the challenge before Black Friday ended!


<img src="/images/2022/phish7.png" class="align-center" 
alt="Phishing email claiming victim won a yeti cooler">

We have here an email that claims to be coming from American Express which states there is a problem in my card and I need to click on the link to find out. Let's ignore the fact of wether or not I have an American Express card or this article would have ended right here. The timing was good: lot's of people are going crazy purchasing milliong of trinkets online, and then they receive an email saying their card has a problem. Did they go over the limit? Was it's information stolen?

Good show old boy!

If I had such a card, what should I do next? The answer depends on how much effort we want to put in this:

## For the impatient
You can't see in the picture but the From: field looks like this:

`From: American Express MyCredit Guide <transunion@em-tuci.transunion.com>`

Why would [TransUnion](https://www.transunion.com/), a US consumer credit 
reporting company, be sending emails for 
[American Express](https://www.americanexpress.com/)? This should be enough for us to immediately drop this email and move on.

## For the willing to spend a bit more time

First of all, when in doubt of whether a suspicious email is legit or not, find the official contact number/email of the company in question and reach out to them. In this case, I did call them. American Express said if they send an email, it will contain

- Your name.
- The last 4 digits of your card.

This email only contains the first name, so per American Express, 
it is at best suspicious. 
They did ask me to forward it to `spoof@americanexpress.com`, which I did.

## For those with time to deep dive and ponder on the implications
Some of you may remember that TransUnion suffered a data breach recently. What if this data is being used to create targeted phishing email? And, what if the criminals are able to either impersonate transunion email addresses or still have access to their servers so they can send emails through their servers? To answer that we need to look in the email header:

<pre>ARC-Authentication-Results: i=1; mx.google.com;
       dkim=pass header.i=@em-tuci.transunion.com header.s=scph0919 header.b="ou/BSRUG";
       spf=pass (google.com: domain of msprvs1=19329inrhx0ms=bounces-266758@bounce.em-tuci.transunion.com 
designates 147.253.210.36 as permitted sender) smtp.mailfrom="msprvs1=19329inrhX0MS=bounces-266758@bounce.em-tuci.transunion.com";
       dmarc=pass (p=REJECT sp=REJECT dis=NONE) header.from=em-tuci.transunion.com
Return-Path: &ltmsprvs1=19329inrhX0MS=bounces-266758@bounce.em-tuci.transunion.com%lt
<u>Received: from mta-210-36.sparkpostmail.com (mta-210-36.sparkpostmail.com. [147.253.210.36])</u>
        by mx.google.com with ESMTPS id 62-20020a630141000000b004778207ac4dsi7561754pgb.396.2022.11.26.12.06.50
        for <b>Clueless Sheep</b>
        (version=TLS1_2 cipher=ECDHE-ECDSA-AES128-GCM-SHA256 bits=128/128);
        Sat, 26 Nov 2022 12:06:50 -0800 (PST)
Received-SPF: pass (google.com: domain of msprvs1=19329inrhx0ms=bounces-266758@bounce.em-tuci.transunion.com designates 147.253.210.36 as permitted sender) client-ip=147.253.210.36;
Authentication-Results: mx.google.com;
       dkim=pass header.i=@em-tuci.transunion.com header.s=scph0919 header.b="ou/BSRUG";
       spf=pass (google.com: domain of msprvs1=19329inrhx0ms=bounces-266758@bounce.em-tuci.transunion.com designates 147.253.210.36 as permitted sender) smtp.mailfrom="msprvs1=19329inrhX0MS=bounces-266758@bounce.em-tuci.transunion.com";
       dmarc=pass (p=REJECT sp=REJECT dis=NONE) header.from=em-tuci.transunion.com
X-MSFBL: fXbaPXh+ne/E8ZM3Y6OyFt9TLlavvIujqeENrG6IrbY=|eyJyIjoicmF1YnZvZ2V sQGdtYWlsLmNvbSIsIm1lc3NhZ2VfaWQiOiI2MzgxZGE3MTgyNjM0YmI3ZmY3ZiI sInN1YmFjY291bnRfaWQiOiIwIiwiY3VzdG9tZXJfaWQiOiIyNjY3NTgiLCJ0ZW5 hbnRfaWQiOiJzcGMifQ==
DKIM-Signature: v=1; a=rsa-sha256; c=relaxed/relaxed; d=em-tuci.transunion.com; s=scph0919; t=1669493210; i=@em-tuci.transunion.com; bh=g54YI3MysS1MVd8EV8xjgfkc97E2Z2epcQAJzoXhCkw=; h=To:Message-ID:Date:Content-Type:Subject:From:List-Unsubscribe:
	 From:To:Cc:Subject; b=ou/BSRUG3cUbJKbYUZ1LVr3J0Z3xP7nFJPUjPutaxPAlyQU2bd2vFDbfNHxdU0LbB
	 HxEwc9YzSTrKnrbFfjcLwSxfZk48k6br1t4DI9fsDgWAimdohpxIGKK6ukD2NE1q/L
	 SESZw9WVeXNvoEVjsYIPh67accGucYF32laIH8ICsqeopmxSoaxsrjHBa/MBjqYZAz
	 8r+jHG+Ilr/QzlJ0Lq5rGA/hJGnHR3lPbkuVRFBsrnV9841IbsIpQDVOUdW172sQbQ
	 zZ+JErYKYYvpwmjqd6A4XMPu3TG9QcymMjHHYqcXRmtL4OdKzB8GKtksDI4uLakZkw
	 8HR0NVWvPUjzQ==
</pre>

At first glance it seems the email came straight from TransUnion, specifically from the host called `em-tuci.transunion.com`. But, then we find the most interesting entry in the above header exerpt (which I highlited):

`Received: from mta-210-36.sparkpostmail.com (mta-210-36.sparkpostmail.com. [147.253.210.36])`

It seems this email came from `mta-210-36.sparkpostmail.com`, whose IP (`147.253.210.36`) has been whitelisted by `bounce.em-tuci.transunion.com` as a sender. From there it ends up in the Clueless's gmail account relying on transunion's server's relationship with google's.

### But, who is SparkPost?
Short version, it is a 
[mass emailing service](https://www.sparkpost.com/email-sending-service). 
They seem to be well-known enough for Microsoft to have 
[instructions on how to access them](https://learn.microsoft.com/en-us/connectors/sparkpost) 
using a connector from within Azure. 
Does that mean they were compromised or the attackers obtained the 
TransUnion's credentials to use this service?

### So, is this Spearphishing via Service (T1566.003)?
If we read the [MITRE ATT&CK](https://attack.mitre.org/techniques/T1566/003/)
entry, sounds like a very good possibility.

## Some kind of Conclusion
Even though this phishing email was much more well thought out than that insult mentioned in the last entry of the series, if you stop and examine it -- without first clicking on its links -- you can still identify it as such rather quickly, without needing to tear down through its raw contents. Don't get me wrong: doing that is fun, but if you are trying to go trhough your daily routine and see this email, in less than 5 minutes you can make a call of whether it is legit or suspicious.

Ok, more if you have to wait on the phone listening to elevator music to talk to a company to verify if they sent said email.


