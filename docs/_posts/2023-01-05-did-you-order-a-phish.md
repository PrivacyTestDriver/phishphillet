---
layout: post
title:  "Did You Order a Phish?"
author: mainphish
tags:
  - content
  - image
  - phish
categories: 
  - blog
  - phish
---

Today's phishing email is a classic for two reasons
- It is the ol'invoice phishing email, showing a bill to a product you or
someone at your place of work may have bought. [
McAfee](https://www.mcafee.com/) does sell 
antivirus software.
- I had saved it in March of last year but only found it today. 
That does not diminish its relevancy because invoice phishing emails 
are still popular.

<img src="/images/2023/phish8.png" 
class="align-center" alt="Phishing email pretending to have a McAfee 
antivirus invoice">

Some phishers seem to have decided that embeding malicious code as payloads 
into either the email itself (thanks to HTML-aware emails) or in the
attached documents -- Microsoft Word/Excel/Powerpoint documents, PDF files, 
or even some image formats -- was a bit too time consuming. 
Or, it was being picked up by the usual mail scanners and deleted. 
So, what can they do? Well, elicit the help from the user! 
Ok, you may argue that all phishing campaigns rely on social engineering, 
and you would be correct. 
But, how can that be craft to evade scanners once the users are conned? 

At first glance, it seems this email will be innefective, as it starts rather carelessly:

1. The return address is a typical quasi-randomly created Gmail one; they could not be bothered with making it sound like it came from a billing department as it claims to be.
1. Also notice they do not even specify the company they are hailing from; they just said something about a Billing Department.
1. This email from some billing department from an unknown company is about the purchase of McAFEE Total 360. Note the name of the company is McAfee, not 
McAFEE.

What seems to be carelessness is actually genius. You see, most people who read this email will not pay attention to the return email address and lack of a business name. All they will focus on is the 3rd item listed above: they just received what seems to be a bill for a software they can't remember ordering. What to do?

There is a phone number prominiently on the bottom of the email. That is the clever move. I expect the next moves to play out as follows:

1. Customer's 
([the mark](https://en.wikipedia.org/wiki/Traveling_carnival#Games)) 
mind will focus on, as mentioned above, the fact they are seeing an 
*unexpected $300 bill*. Why did they receive it? Was that an accident? Did someone with a similar name ordered it? This is the fear component of the phishing email.
1. It says the charge mode is "Auto Debit!" I too have no idea of what "Auto-Debit" means. Maybe they wanted to say auto renewal using a debit card. But the point is these words create a sense of urgency, which is another component of a good phishing email.
1. So, they call the phone number to fing what is going on. The person on the other end, who is an Eastern European man called Peggy (bonus points if you know which old ad I am alluding to), will maybe ask for the mark's personal (before you get excited, GDPR does not apply to criminals since by definition they do not follow the law) and credit/debit card information to "confirm" (read: store and sell) if that was the card used. However, it would make more sense if he...
1. Peggy will probably ask the mark to go to a website and then download and install something in the mark's computer (ideally a work one) to check if the McAFEE program is installed and then uninstall it. As expected, that is a trojan horse to help deploy the real payload. The good thing about being on the phone is that Peggy can help the mark work around the malware protection software in place so the trojan can be successfully installed.

## What to do
If you receive such email, take a break before acting on it. 
Then, if you received it at work, reach out to your IT security people and 
ask for help. Or, send it to us, so we analyze it and tell you if it is
indeed malicious. If so, we would love to add to our collection and
create a post about it.

Relying on software to magically find and delete such emails does not work 
all the time. *You* the user is the most important line of defense.


