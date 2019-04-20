---
layout: post
title:  "Freshman Projects Clock"
date:   2013-12-01
excerpt: "Clock made for the freshman projects class out of 74XXX series logic"
# image: "http://farm9.staticflickr.com/8426/7758832526_cc8f681e48_c.jpg"

categories:
  - Hardware
  - Digital Logic
tag:
  - Digital Logic
  - Hardware
  - Project

published: true
---
## Freshman Projects Clock

I did this project in 2013 for the introductory projects class in electrical engineering. It was implemented using a tuned 14-bit RC resonator/counter combo IC feeding into an array of 74XXX-series NAND/NOR logic that in turn went through decoders to prep the logic signals for the 7-segment drivers that displayed the time.

This was all placed in a hollowed out speaker enclosure and control panel to adjust the clock. Each button synchronously redirected the base clock into either the minutes or hours counter to allow for setting the time. The selector switch changes the tap on the 14-bit counter, making the clock run at either 4x or 8x speed to allow for testing of roll-over and other edge cases during development. As a side bonus it also allows for easier setting of the time.

On of the large problems with this clock was the wire density required to fit all the ICs on one board and how it was connected with hand-soldered wire. At the time I was quite proud of the wiring board but now I'm filled with a sort of fascinated horror while looking at it now.

The other difficulty with this board was dealing with all the roll-overs with special conditions. There was an AM/PM indicator so essentially full 24-hour tracking was required but the seconds and minutes had to roll over on 59 -> 60 but the hours needed to roll on 12. This was only difficult because during initial design I neglected to think of the control required for keeping the first hour panel at 0 for 9 hours until the 10th hour rolled over and it had to become 1. Then it had to become 0 again in ~3 hours which was more logic than most of the rest of the clock.

Another thing that was a fun challenge was being thrown into the deep end of multi-clock logic without knowing anything about it. As this was largely a fancy clock (signal) generator, I recall spending a long time getting all the counters to roll over on the correct edge. Everything needed to roll over on the change of a second but it had lots of conditions to watch as well. In an HDL this would have been very easy to implement but on the board (refer to the jumble of wires pictured below) it meant hunting down and splitting many wires that then had to be distilled down to one signal through combinational logic to make sure everything flipped when it should. I started by having everything flip on the change of 59 -> 0 seconds but it meant that on the 59th minute of every hour, the hour also changed every minute. Oops.

To solve I ended up creating a series of single-wire signals that indicated when each section of hh:mm:ss rolled over so I could mix them in a combination required to handle things like the many conditions of the hour rollovers.

Working with purely logic gates and counters was a satisfying experience but every time I think of remaking this project I can't help but think how it would have been faster, easier, and cheaper with a microcontroller or PLD (for fun and accuracy) on a tiny PCB board.

### Pictures

<figure class="half">
	<a href="/images/freshman_projects_clock/front_plate.jpg"><img src="/images/freshman_projects_clock/front_plate.jpg"></a>
  <a href="/images/freshman_projects_clock/front_plate_but_removed.jpg"><img src="/images/freshman_projects_clock/front_plate_but_removed.jpg"></a>
	<figcaption>Front of the finished clock (left), with the face plates removed (right)</figcaption>
</figure>

<figure>
	<a href="/images/freshman_projects_clock/functionally_correct.jpg"><img src="/images/freshman_projects_clock/functionally_correct.jpg"></a>
	<figcaption>Fist time functionally correct and working.</figcaption>
</figure>

<figure>
	<a href="/images/freshman_projects_clock/top_PTH.jpg"><img src="/images/freshman_projects_clock/top_PTH.jpg"></a>
	<figcaption>Initial state of the board before soldering.</figcaption>
</figure>

<figure class="half">
	<a href="/images/freshman_projects_clock/humble_beginnings.jpg"><img src="/images/freshman_projects_clock/humble_beginnings.jpg"></a>
  <a href="/images/freshman_projects_clock/nearly_there.jpg"><img src="/images/freshman_projects_clock/nearly_there.jpg"></a>
	<figcaption>Initial work (left), Starting to connect the LED panels (right)</figcaption>
</figure>
