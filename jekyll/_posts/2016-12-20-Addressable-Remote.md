---
layout: post
title: "Addressable Remote"
description: "It all started with coffee. Naturally."
category: Electronics
tags: [electronics, project, circuit, wireless, remote, cPLD, arduino]
modified: # <-- update if modified

imagefeature: # will this work with nothing?
comments: false
share: true
published: false
---

This all started when the house started to get cold and I wished the coffee machine would get to temperature before I left my bed.  

So this project is in it's infancy for many reasons. The actual remote is easy but I want it to be general and expansible. Meaning it needs to have switches for addressing, power management, and possibly a display among other things. I also have to decide on a standard of communication (probably just UART but I'm doing this all for myself so it's more free). The decision is largely in the amount of commands allotted after address. The coffee machine is easy since it just turns on or off but in the future I might have it do a lot more.

I also have a few Sparkfun Bluetooth modules - which I'm intentionally avoiding due to what that would do to the cost of each receiver - but I might include it in a second version of the remote simply because it's so universal.  
I could also add a 'gold' BT module to the espresso machine and just connect to it with my phone. That's like a $30 job.

The main reason this project hasn't been completed already is because the espresso machine's electronics are sealed to water and air through various enclosures and sealants. So I have no idea what signal is being sent to turn it on. So I also have to either make a logic sniffer or buy one (Dangerous Prototypes has a rather nice one). Making one is only hard because I only have a DE0 dev board - which is easy to program but I've never made a loader for it or written to memory with it and I'd have to do both.  
The controls have 20-odd wires connecting them to the rest of the machine as well so it might be as simple as a logic high on one of them if it's just using cPLDs or equivalent.

The signal is a 434 MHz ASK signal because I don't need much data, the modules are extremely cheap, the frequency is high enough for small-ish antennas, ASK allows for easy shift-register reading on cPLD's or serial.reads on Arduino, and I have a pair lying around to begin with. Waste not, want not, etc.

The Arduino mini is a super easy solution to the remote, the issue coming from the number of pins needed to read and set addresses. I can also just use any old Atmel 328p (or similar) and program it with or without Arduino.  
An Altera MaxII cPLD is my real target though. Onboard flash memory, good for more writes than I'll need, runs off of 3.3V (the main reason for not using the newer Max's - they use 1.5 or whatever), an internal oscillator, and an awe-inspiring number of useable pins. The main issue is difficulty or programming them and attaching them to a board. The Bus Pirate boasts (super slow) JTAG programming and serial which might just have to do.

Antenna can run off of voltage up to 12V - which is likely what I'll want (testing the range of 9V to see if it convers the whole house would be a good thing to do) for maximum range. The MaxII runs off of 3.3 but I believe it can regulate 5V down. Either way, I'll have to regulate the antenna voltage down.
