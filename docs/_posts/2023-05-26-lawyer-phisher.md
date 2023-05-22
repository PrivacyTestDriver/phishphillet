---
layout: post
title:  "Lawyer Phisher?"
author: mainphish
tags:
  - content
  - phish
  - image
categories: 
  - blog
---

Phisher this time is a bit more clever than the average one we have been 
dealing with recently. Yes, I know it does not take much, but I will take
what I can get. 

<pre>
Reply-To: jamesfort@fortsolicitor.com
From: James Fort <jamesf@innovateisndustries.com>
To: <cluelessSheep@example.com>
Date: May 20 2023 19:43 -0400
Subject: Kindly Confirm Upon Receipt

Greetings,

My name is James Fort, a Solicitor and Senior Partner in the Law
Firm of Fort & Co. Solicitors. Kindly confirm the receipt of this
email to my direct contact email address
(jamesfort@fortsolicitor.com)

Regards,
James Fort
</pre>

## How to know it is a phishing email

Before you ask, there are some dead giveaways this is a phishing email

- That trademark of scam messages, be them phishing or fake job offers or
whatever, the notorious `kindly` is there not once but *twice* as proud as 
it can be.

- Why is the email address in the `From:` field different than that in the
`Reply-To:` field, specially if this is supposed to be a 
[solicitor](https://en.wikipedia.org/wiki/Solicitor) who has a domain for
his legal enterprises? `innovateisndustries.co` not only does not sound like
`fortsolicitor.com` but also has different connotations. 

- Related to the above, the fact the email goes out of its way to say "*use
`jamesfort@fortsolicitor.com` and not the email this is coming from*" makes
it even more suspicious.

- Why do I need to confirm I receive an email from this soliciting phisher?
I understand the idea is to weasel around the (rather usueless) phishing and
malware detection filters, but this is like asking to ask: if you have business with me, tell me about it.
You would make the Nigerian Prince sad.

## I am OK with this phisher because I actually had to put some effort

But, this time I could not resist. I had an itch to scratch: is there a
company with a website called `innovateisndustries.com`? If so, it would mean
they are either plain impersonating or just took their domain/website/email
over. In this case, the answer is: there are many sites with similar names
(which is probably why they chose it), but none exactly like it. So, I decided
to check how old `innovateisndustries.com` is. If it is not too old, they
just created it for the phishing email. Here is what I found:

```bash
   Domain Name: INNOVATEISNDUSTRIES.COM
   Registry Domain ID: 2778555624_DOMAIN_COM-VRSN
   Registrar WHOIS Server: whois.synergywholesale.com
   Registrar URL: http://synergywholesale.com
   Updated Date: 2023-05-20T15:47:49Z
   Creation Date: 2023-05-06T11:46:31Z
   Registry Expiry Date: 2024-05-06T11:46:31Z
   Registrar: Synergy Wholesale Pty Ltd
   Registrar IANA ID: 1609
   Registrar Abuse Contact Email:
   Registrar Abuse Contact Phone:
   Domain Status: ok https://icann.org/epp#ok
   Name Server: NS1.CLOUD-CD832E.MANAGED-VPS.NET
   DNSSEC: unsigned
   URL of the ICANN Whois Inaccuracy Complaint Form: https://www.icann.org/wicf/
>>> Last update of whois database: 2023-05-22T03:53:37Z <<<
```

The most important line here is the `Creation Date: 2023-05-06T11:46:31Z`. 
This domain is not even a month old, which is yet another clue this is a 
phishing email. And, what about `fortsolicitor.com`? Glad you asked:

```bash
   Domain Name: FORTSOLICITOR.COM
   Registry Domain ID: 2765984400_DOMAIN_COM-VRSN
   Registrar WHOIS Server: whois.launchpad.com
   Registrar URL: http://www.launchpad.com
   Updated Date: 2023-03-17T20:35:28Z
   Creation Date: 2023-03-17T20:35:28Z
   Registry Expiry Date: 2024-03-17T20:35:28Z
   Registrar: Launchpad.com Inc.
   Registrar IANA ID: 955
   Registrar Abuse Contact Email: abuse@hostgator.com
   Registrar Abuse Contact Phone: 602-226-2389
   Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
   Name Server: NS8617.HOSTGATOR.COM
   Name Server: NS8618.HOSTGATOR.COM
```

It was created two months ago and if we take a look at its homepage:

```
   HostGator                                                                    
                                                                                
Let's set up your website!                                                      
                                                                                
Let's set up your website!                                                      
                                                                                
   Login                                                                        
                                                                                
Log in to                                                                       
HostGator                                                                       
                                                                                
Log in to                                                                       
HostGator                                                                       
                                                                                
   Support                                                                      
                                                                                
Get                                                                             
Support                                                                         
                                                                                
Get                                                                             
Support                                                                         
                                                                                
Copyright HostGaor
```

we see they just got the HostGator account and never really built a website.

Is this a bit above and beyond what we needed to do to find if this is a 
phishing email? Yes. But, since this phisher actually took time to get some
domains instead of just faking it and using gmail address, we owed to him
to show he started right laying together the required infrastructure.
Unfortunately then he dropped all the goodwill he earned by providing a
rather easy to detect phishing email.

Overall, it is not a bad effort... if this was a first homework in an 
entry level phishing class.
