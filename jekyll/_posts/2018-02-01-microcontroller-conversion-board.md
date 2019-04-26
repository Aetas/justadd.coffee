---
layout: post
title:  "MSP432 Conversion PCB"
date:   2018-02-01
excerpt: "Conversion PCB made to translate an MSP432 TI-Launchpad to a custom PCB"
# image: "http://farm9.staticflickr.com/8426/7758832526_cc8f681e48_c.jpg"

categories:
  - Hardware
  - Microcontroller
  - Senior Design
  - PCB
tag:
  - Microcontroller
  - MSP432
  - PCB
  - Hardware

published: true
---

## MSP432 Conversion PCB
Throughout my [senior design project]({{ site.url }}{% post_url  2017-10-01-Senior-Design %}) I needed to run tests with our microcontroller dev board (a TI MSP432 Launchpad in this case) but I needed the expanded functionality of our custom PCB while I was designing and testing in the meantime. To remedy this, I whipped up a translation board to translate the harness through.

The board had the normal bells and whistles like power indicators and disconnects in addition to 3 level shifters (3.3V <-> 5V), 3 voltage follower buffers, a LDO and 4 NPN BJTs for pushing high enough current into relays to switch them. This was all packaged into the same form-factor as the rest of the boards (matched to Raspberry Pi mounting holes.)

Looking back at the board design, I'm slightly horrified at the poor reference/return path control but then again there were nearly no performance requirements and the switching was likely measured in microseconds so it did not matter.

## Pictures
<figure>
	<a href="/images/sd_mcu_translate_pcb/dev_shield_sch.PNG"><img src="/images/sd_mcu_translate_pcb/dev_shield_sch.PNG"></a>
	<figcaption>Schematic of the translation schematic</figcaption>
</figure>

<figure>
	<a href="/images/sd_mcu_translate_pcb/dev_shield_brd.PNG"><img src="/images/sd_mcu_translate_pcb/dev_shield_brd.PNG"></a>
	<figcaption>Layout of the translation board</figcaption>
</figure>
