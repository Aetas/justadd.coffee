---
layout: post
title:  "MSP432 Microcontroller Board"
date:   2018-04-23
excerpt: "Microcontroller PCB made for Senior Design"
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

## Senior Design Microcontroller Board
This PCB was designed as the main interface to all the sensors and drivers for my [senior design project]({{ site.url }}{% post_url  2017-10-01-Senior-Design %}). The board was designed to support a MSP432 microcontroller (MCU) with a footprint compatible with the mounting posts on a Raspberry Pi and support UART over USB to accept control and telemetry request commands.

The largest problem that arose was the two-layer restriction on the board that came from cost and design tools available (I was using the free Eagle 7.7 edition with only 2 layers available – I didn't know PADs/KiCAD/Altium/etc at that point). As such the board is pretty point-to-point in terms of layout with minimal considerations for return paths and inductive loops.

## Pictures
<figure>
	<a href="/images/sd_mcu_pcb/MSP432_MCU_sch.PNG"><img src="/images/sd_mcu_pcb/MSP432_MCU_sch.PNG"></a>
	<figcaption>Schematic of the MSP432 board.</figcaption>
</figure>

<figure>
	<a href="/images/sd_mcu_pcb/MSP432_MCU_brd.PNG"><img src="/images/sd_mcu_pcb/MSP432_MCU_brd.PNG"></a>
	<figcaption>Layout of the MSP432 board.</figcaption>
</figure>

<figure class="half">
	<a href="/images/sd_mcu_pcb/checking_paste.jpg"><img src="/images/sd_mcu_pcb/checking_paste.jpg"></a>
  <a href="/images/sd_mcu_pcb/checking_reflow_see_MCU_leads.jpg"><img src="/images/sd_mcu_pcb/checking_reflow_see_MCU_leads.jpg"></a>
	<figcaption>Pre and post flow inspection</figcaption>
</figure>

<figure>
	<a href="/images/sd_mcu_pcb/assembled.jpg"><img src="/images/sd_mcu_pcb/assembled.jpg"></a>
	<figcaption>S.</figcaption>
</figure>

<figure>
	<a href="/images/sd_mcu_pcb/bottom.jpg"><img src="/images/sd_mcu_pcb/bottom.jpg"></a>
	<figcaption>Schematic of the MSP432 board.</figcaption>
</figure>
