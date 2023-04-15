---
layout: post
title:  "Bitcoin Phisher"
author: mainphish
tags:
  - content
  - phish
  - image
categories: 
  - blog
---

A lot of people think that buying some magic app will block all phishing 
emails. 
If you have been following this blog, you know that these programs only get the
really badly put together ones. I mean the ones that are as obvious as
someone running naked inside the post office with a "arrest me" cape.
You really do not need to put too much effort to bypass those tools and their
filters; as today's example will show you can be pretty lazy and effective.

<img src="/images/2023/phish14.png" 
class="align-center" alt="[Phishing email claiming they recorded you doing
naughty things in front of the computer camera]">

This email showed up in another mailing list I belong to earlier today; 
I removed the 
identfying parts (should have used `mailinglist@example.com` but I was in a 
hurry on Gimp) to protect the innocent. Here is the text version of the email;
I made sure I preserved all the typos and bad formatting for your enjoyment.

<pre>
From: <mailinglist@example.com>
To: <mailinglist@example.com>
Date: 14 Apr 2023 02:34:33 +0400
Subject: Your personal data has leaked due to suspected harmful activities.

Hi there!I am a professional hacker and have successfully managed to hack 
your operating system.
Currently I have gained full access to your account. In addition, I was 
secretly monitoring all your activities and watching you for several months. 
The thing is your computer was infected with harmful spyware due to the fact 
that you had visited a website with porn content previously. 
Let me explain to you what that entails. 
Thanks to Trojan viruses, I can gain complete access to your computer or any 
other device that you own.It means that I can see absolutely everything in 
your screen and switch on the camera as well as microphone at any point of 
time without your permission. In addition, I can also access and see your 
confidential information as well as your emails and chat messages.You may be 
wondering why your antivirus cannot detect my malicious software. Let me 
break it down for you: I am using harmful software that is driver-based, 
which refreshes its signatures on 4-hourly basis, hence your antivirus is 
unable to detect it presence.I have made a video compilation, which shows 
on the left side the scenes of you happily masturbating, while on the 
right side it demonstrates the video you were watching at that 
moment..All I need is just to share this video to all email 
addresses and messenger contacts of people you are in communication with on 
your device or PC. Furthermore, I can also make public all your emails 
and chat history.I believe you would definitely want to avoid this from 
happening. Here is what you need to do - transfer the Bitcoin equivalent of 
1250 USD to my Bitcoin account (that is rather a simple process, which 
you can check out online in case if you don't know how to do that).Below is 
my bitcoin account information (Bitcoin wallet): 
**[BITCOIN CODE HERE]**Once the required amount is 
transferred to my account, I will proceed with deleting all those videos 
and disappear from your life once and for all. Kindly ensure you complete 
the abovementioned transfer within 50 hours (2 days +). I will 
receive a notification right after you open this email, hence the countdown 
will start.Trust me, I am very careful, calculative and never make 
mistakes.If I discover that you shared this message with others, 
I will straight away proceed with making your private videos 
public.Good luck!
</pre>


## How to know it is a phishing email (even when the phishing filter does not)

- While I like the salutation ("*Hi there! I am a professional hacker!*"), 
that is a bit of a telltale something is up.
- The use of "*Kindly*" in an email always make me put it in the 
"*suspicious*" pile. 

- *Why was this email not flagged by a spam/phishing detector?* 
Actually it was detected and flagged because it mentioned "bitcoin" but the
"score" was not high enough to block it. My guess is that
ransomware is a thing and they usually ask for payment in that form.
Everything else in the email is just text, no suspicious links or 
attachments riddled with malware mail scanners look for.

- **History lesson:** This is the genesys of 
the ransomware email (without all the effort associated with it): it claims
it stole sensitive data -- in this case proof you have been watching porn --
hoping that will guilt you into paying not to have that exposed. 
This is technically the second stage of ransomware (making you pay not to
have data exposed), while the first one is obviously making you pay to
access the files they encrypted. 

- Let's read again what the email claimed to have recorded. 
Ok, it is a long and badly formatted email; let's instead scan through it.
While there has been cases of criminals, schools and exam proctoring sites
included, turning cameras 
and microphones on to see what a computer user is doing, 
chances are its claims are unfounded; they are just working the fear factor
here without actually having done anything to deliver it.
In principle this is the same as the phishing emails with receipts 
for unknown products and services we have talked about before.

- One of the things that show the claims made are fake is this email was 
sent to mailing list instead directly to a person.
Talk about being an unprofessional phisher!
Even if I was sending this to a ton of people hoping they will fall for it, 
I would have put the effort to make it look like it was sent to a single
person, not a mailing list.

- In previous posts we said the best defense against phishing emails is
not to click on links and/or download attachments of every email you receive.
In other words, if you give yourself time to stop and think, chances are 
you will realize it is suspicious. For a phishing email to be successful
it needs to compel you to react quickly and without thinking. 
In this case, it gives a deadline of 50 hours.

## Do you want me to have a conclusion?

1. If your computer has a built-in camera, get a camera cover for it.
1. A lot of the years-old phishing emails still work today.
1. That was a long phishing email. 
