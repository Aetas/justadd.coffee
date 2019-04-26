---
layout: post
title:  "Small Sensor PCBs"
date:   2018-01-01
excerpt: "PCBs designed for Senior Design to support sensors"
# image: "http://farm9.staticflickr.com/8426/7758832526_cc8f681e48_c.jpg"

categories:
  - Hardware
  - Senior Design
  - PCB
tag:
  - Sensors
  - PCB
  - Hardware
  - Hall Effect

published: true
---
{:toc}

## Sensor Boards for Senior Design
For my senior [design project]({{ site.url }}{% post_url  2017-10-01-Senior-Design %}) we had to make an automated proof-of-concept airlock for Lockheed Martin for them to use in their Lunar Orbital Platform Gateway habitat mockup. While I won't delve into the project here, I will go over the sensor boards I designed to assist in automating the airlock.

## Hall-Effect Sensor
There were 5 hall-effect sensors in the airlock for position sensing -- 1 for each of the two doors and 3 used in the sliding rail system that the ferries the payload plate to either side.
The 3 hall-effects were used for position sensing purposes and served as the controls for the motion loop, allowing for a concise way of tracking position through a state machine abstracted out in code.

The PCBs were used mainly as plug-and-play boards with pull-up resistors, debouncing cap, power indicator LED, and quick disconnects for both power and the LED for both testing as well as low-power consumption mode.

<figure>
	<a href="/images/sd_sensor_pcbs/Hall_Effect_sch.PNG"><img src="/images/sd_sensor_pcbs/Hall_Effect_sch.PNG"></a>
	<figcaption>Schematic of the hall-effect sensor board</figcaption>
</figure>

<figure>
	<a href="/images/sd_sensor_pcbs/Hall_Effect_brd.PNG"><img src="/images/sd_sensor_pcbs/Hall_Effect_brd.PNG"></a>
	<figcaption>Layout of the hall-effect sensor board</figcaption>
</figure>

<figure>
	<a href="/images/sd_sensor_pcbs/board_top_bottom.jpg"><img src="/images/sd_sensor_pcbs/board_top_bottom.jpg"></a>
	<figcaption>Printed and un-assembled picture of the hall-effect sensor board</figcaption>
</figure>

## Pressure Sensor
In the beginning of this project we were left with the impression that we would need to pull partial-vacuum on the airlock as a design spec so I drew up a quick board to support a pressure sensor to digitally read out psi to the microcontroller.
This board had a switch to go between SPI and I2C as desired as well as disconnect jumpers and power indicators.
There is no picture of the finished board because the problem of drawing even 1 psi difference on the enclosure quickly blew the design over our funds and wildly complicated the design through requiring air-tight fittings and seals all without addressing the core design target -- automation.

<figure>
	<a href="/images/sd_sensor_pcbs/Pressure_Sense_sch.PNG"><img src="/images/sd_sensor_pcbs/Pressure_Sense_sch.PNG"></a>
	<figcaption>Schematic of the pressure sensor board</figcaption>
</figure>

<figure>
	<a href="/images/sd_sensor_pcbs/Pressure_Sense_brd.PNG"><img src="/images/sd_sensor_pcbs/Pressure_Sense_brd.PNG"></a>
	<figcaption>Layout of the pressure sensor board</figcaption>
</figure>

## Capacitive Sensors
The detect the payload on the sliding table I looked into the dos and don'ts of making a capacitive touch sensor board -- which as it turns out can be quite the art. So instead of sinking all the costs of iterative design and test, I just went with the exceedingly cheap (by comparison) <a href="https://www.sparkfun.com/products/12041">Sparkfun Capacitive Touch Breakout</a> board.
One of the main values from this board is that there is a pad to bring out a wire to an external pad (the IC calibrates on startup) so I connected it to isolated copper pads that we sunk into the table in 3 spots. Once we got proper contact and isolation these worked extremely well and more reliably than I would have expected of a nearly electrically-floating disk of copper.
