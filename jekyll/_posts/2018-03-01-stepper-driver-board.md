---
layout: post
title:  "Stepper Driver Socket Board"
date:   2018-03-01
excerpt: "Socketed support PCB for stepper motor drivers"
# image: "http://farm9.staticflickr.com/8426/7758832526_cc8f681e48_c.jpg"

categories:
  - Hardware
  - Senior Design
  - PCB
tag:
  - Stepper Motor
  - PCB
  - Hardware

published: true
---

## Stepper driver board
During my [senior design project]({{ site.url }}{% post_url  2017-10-01-Senior-Design %}) we used 3 stepper motors, 2 to drive the rail system under the payload table and one to move the payload securing plate.

After some proof of concept work, I made a PCB with sockets to mount 3 <a href="https://www.pololu.com/product/2133">Pololu drivers</a> for quick swaps and also mounting in the enclosure. The board could populate all 3 driver boards at once and run one board on it's own independent and isolated power supply with only a jumper. The idea behind this was to leave open the option of running the payload securement stepper motor at a higher voltage if needed for a better operating point while holding position. Additionally, each board had a switch array to select micro-stepping.

## Pictures
<figure>
	<a href="/images/sd_driver_pcb/driver_socket_board_sch.PNG"><img src="/images/sd_driver_pcb/driver_socket_board_sch.PNG"></a>
	<figcaption>Schematic of the driver board.</figcaption>
</figure>

<figure>
	<a href="/images/sd_driver_pcb/driver_socket_board_brd.PNG"><img src="/images/sd_driver_pcb/driver_socket_board_brd.PNG"></a>
	<figcaption>Layout of the driver board.</figcaption>
</figure>

<figure>
	<a href="/images/sd_driver_pcb/progression.jpg"><img src="/images/sd_driver_pcb/progression.jpg"></a>
	<figcaption>Progression of dev boards to PCBs</figcaption>
</figure>

<figure class="half">
	<a href="/images/sd_driver_pcb/assembled.jpg"><img src="/images/sd_driver_pcb/assembled.jpg"></a>
	<a href="/images/sd_driver_pcb/bottom.jpg"><img src="/images/sd_driver_pcb/bottom.jpg"></a>
	<figcaption>Finished assembly with drivers installed</figcaption>
</figure>
