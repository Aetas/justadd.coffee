---
layout: post
title: "Variable Power Supply"
description: "I find myself needing a power supply that does small and high voltage."
category: Electronics
tags: [electronics, project, power supply, circuit]
modified: # <-- update if modified

imagefeature: # will this work with nothing?
comments: false
share: true
published: false
---

I seem to find myself in need of power supplies that can do various logic levels and power levels. Things like 1.5V (which - admittedly - this supply can't quite reach) to 12V. At the moment the supply goes to nearly 30V because it's not much different but I might tone that down a bit to squeeze out more current or something. Though increasing current takes the most work since I would have to resize all my traces and re-pick parts that can handle ~5A.

The power supply is of the simple, brute-force type with a full-wave rectifier feeding a set of damping capacitors and a adjustable voltage regulator IC. The main difference is that the transformer is center-tapped with the middle taken as ground. This allows for the a positive and negative rail to be taken from the top and bottom leads on the secondary.

Voltage is controlled via fine and coarse rheostats with 3D-printed knobs.

The design is realized on PCB with 70 mil traces (over-sized for the start-up current) and through-hole components. I thought about SMD components but the large capacitors were through-hole anyhow and I can use the larger board size for better heat sinking. I'm using dedicated heat sinks on the regulators anyhow but they have pins that sink into the PCB anyhow so they should be quite effective.

LTSpice schematic is outlined, not specified.

Transformer characteristics will be measured once I get the supplies.

Case will probably be some generic electrical box. Might make a nicer box to contain the box (insert Emperor's New Groove gif) but I need some nice grounding and such.

I also fancy the idea of plug-n-play resistors for common voltages. Like a resistor set that makes exactly 3.3V, 5V, 9V, or 12V. Maybe a switch to go between rheostat and specific resistor values. Not sure at the moment since it will need to be mostly complete before testing.  
Actually, I think high-voltage regulators and a SP4T switch would be the most reliable and fail-resistant. It would have high current tolerance, too.
