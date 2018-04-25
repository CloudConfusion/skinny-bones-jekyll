---
layout: article
title: Be wary of Cloudflare's Always use HTTPS
date: '2017-09-27 22:25:54'
tags:
- cloudflare
- security
- website
- websites
- wordpress
---


Before I go any further, let me just say HUGE fan of CloudflareÔÇÖs free level of stuff.┬á TheyÔÇÖre a great bunch of people.

So I tried to come to this very blog to make a different post and what happened?  
 I get redirected to some shitty t-shirt site.  
 To clarify ÔÇô It was shitty in both website design and t-shirt design.


## ZOMFG IÔÇÖVE BEEN HACKED!

Why am I such a tit and not offsite backing up my blog? UGH , thoseÔÇª 4 articles will be gone forever.

One of them was actually good.


## I wasnÔÇÖt hacked

so like many people I have hooked up CloudflareÔÇÖs free SSL/DNS/CDN network to a v cheap bit of hosting. IÔÇÖm hosted (or was at the time of writing for this blog) with Inmotion.┬á TheyÔÇÖre ok. Their support tonight was excellent when I went all grumpy IT blogger on them.┬á On their end, I only pay for http, not an ssl cert and https (see where this is going?)

On my Cloudflare panel, I turned on Always use HTTPs, trying to be all security conscious.┬á OOOFT. bad move,┬á Cotton.

See I share space with multiple people over at Inmotion. So when my website was trying to force https, InmotionÔÇÖs back end went ÔÇ£you donÔÇÖt have that, ya cheap bampot, letÔÇÖs just move to the next one on the listÔÇØ and KABOOM. IÔÇÖm in crappy t-shirt website, wondering what happened to my beautiful Purple and Grey site.  
 I really have a grudge for that site. Like it was their fault or something. But it wasnÔÇÖt.

It was CloudflareÔÇÖs. Or InmotionÔÇÖs. Or the sun was in my eyes.

I am blameless.

┬á


