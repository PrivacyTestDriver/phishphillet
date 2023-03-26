---
layout: post
title:  "The Nigerian Prince Likes to Phish"
author: mainphish
tags:
  - content
  - phish
categories: 
  - blog
---


Early this month I received yet another classic phishing email; 
this time it is a traditional *Nigerian Prince* one. 
This style of phishing email is identified by, like the others, its
unique pattern:

1. It always is supposed to be from someone, or that person's agent, who 
needs to transfer vasts amount of money and is asking you, specifically, to
help. 
   **Fun fact:** in the original email, you were supposed to be helping
a Nigerian Prince move his money out of his country, hence the name.

1. The carrot is that you are "sent" the sum of money and then take a 
rather sizeable commission from said sum. 

1. You are supposed to help by depositing a check or accept a funds transfer,
and then, after taking your commission, immediately transfer the rest of the 
money to another account. The hurry here is very important because they need 
to finish the deal before your bank can verify there are any funds. 

1. The trap is that they never really send any money. 
So, in a few days the bank will say the payment **you** received has no
funds, but by then you have already sent payment to the criminals, which 
means at best your account lost that much money, but it can also mean your
account is now overdrafted.

Banks *supposedly* have wizened up and came up with ways to stop that, which
is why this specific phishing attack is not as popular as it was before. 
That does not mean it has evolved in different attacks; I will wait until
I find one of them to talk about. For now, let's take a look at this email:

<pre>
From: Gerhardus Maria <vandekujohmaria@gmail.com>
Date: Tue, 7 Mar 2023 10:19:29 +0000
Subject: Good day
X-Mailing-List: kvm@vger.kernel.org

Hello Dear

How are you doing?I'm van der kuil Johannes gerhardus Maria. I am a
lawyer from the Netherlands who reside in Belgium and I am working on
the donation file of my client, Mr. Bartos Pierre Nationality of
Belgium.  I would like to know if you will accept my
client's donation Mr. Bartos Pierre?

Waiting to hear from you soon
</pre>

## How to know it is a phishing email

- The "*Hello Dear*" is always a dead giveaway something is afoot on this
email in my book. I have never met van der kuil Johannes gerhardus Maria
Juanita che ha rubato la mia Fiat cinquecento rossa con il volante che non 
funziona,
esq. So, I do not think that would be the appropriate greeting for a first
conversation.

- If you glance through the email, you will see it fits the "Nigerian 
Prince" phishing email format: some agent (lawyer) wants you to help 
move money (donation) somewhere.

- The bait is the sentence "*I would like to know if you will accept my
client's donation Mr. Bartos Pierre?*" They hope you will be curious enough
to email back and ask for more info. If you do, they will know you felt
for the lure even though you have not bitten the bait just yet. Their 
following emails will work on that.

- `kvm@vger.kernel.org` is a mailing list for a computer emulator; it makes
no sense someone would accidentally send an email about donations to it.

- This kind of attack does not rely on malicious links or attachments. All it
needs is someone greedy enough to reply to the email.

I thought on replying but then I got distracted with a laser pointer. 
And, that is a good attitude when you do not recognize an email: stop,
take a break, and then examine it. Remember even though this specific
phishing email did not push for a sense of urgency (they would do that later
to ensure you bite the bait), the last thing they want if for you to give
yourself time to think.

