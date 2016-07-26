---
layout: post
title: "Converting a 50Mhz Oscilloscope to 100MHz"
description: "Yeah.... I'll update this later"
category: Electronics
tags: [website, web development, general, musing]
modified: #2016-06-19 <-- update if modified

imagefeature: # will this work with nothing?
comments: false
share: true
published: false
---

# It's funny...

I call it renovating but it was brand new when I did the renovations.  
What I mean is that Rigol did something brilliant and rather offensive to every electronics geek that has ever heard of it.

What do I mean by that? Well you see, the <product line> oscilloscopes all came with the exact same guts. Why are there <3> versions then?  
That's where it's clever and offensive. They wanted to have clear breaks between product levels to encourage buying -such and such- for -this and that reason-. But developing 3 different oscilloscopes for the entry-level low-mid range product is a rather expensive and finnicky (how the fuck is that spelled?). Not to mention if you work with the same internals for the majority of your products you see back, the service becomes significantly cheaper and higher quality. So I can't **honestly** blame them for doing it.  
I think if there was ever a time where they patched out the ability to upgrade a 50MHz to a 100MHz scope via the normal methods, there would be hell to pay in backlash.  
The funny thing is that they don't even really have different prices. I mean, the 100MHz scope is the same price as the 50, the difference being the interface. It just so happens that I prefer the 50MHz interface to the 100 as it is closer to what we have in the CU circuit lab and I am familiar with it at a glace.

Have I put enough filler? Probs.

Use DSER option, not DSFR option. DSFR is the same but supports 500 uV/div, which the 1054's hardware doesn't support.

Sneaky sons a bitches actually include 36 hours of trial time of the upgraded software to make the product look better than it is. Realistically, you won't be able to send it back in time after 36 hours of using it.
