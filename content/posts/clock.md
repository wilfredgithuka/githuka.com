---
title: "Complete Computer Clock"
date: 2020-12-16T20:27:54+03:00
draft: false
---
This is the final set of components that will make up the complete computer clock. This
last section will add 3 AND gates and an OR gate together with 2 ineverters and 
a HALT signal to halt the clock when needed to.

![all](/img/8/clock.jpg)

### Components

* 74LS04 Hex Inverters
* 74LS08 AND Gates
* 74LS32 OR Gates

## Connection
The main objective behind this final step in building our clock is to combine
the previous: Astable pulse, Manual Pulse and Select pulse into one unified
system.

The output of the Astable signal which is PIN 3 of the 555 timer is connected to 
the one input of the 74LS04 AND gates. Here I have used the first AND gate whih is 
on PIN 1 and PIN 2. The second input to the same AND gate is from the select button 
which on the breadboard is the output of the 555 timer on PIN 3.

The second AND gate is the one on PIN 4 and PIN 5 with the output being on PIN 6 of the
same 74LS08. One of the input of this AND gate is from the Select switch but there is 
an inverter before it. This inversion function is provided by 74LS04's PIN 1 and PIN 2.
The second input of the AND gate is provided by the input signal from the Manual pulse.
This manual pulse is from the output of the 555 timer.

The output of the first and second AND gates are connected to an OR gate which is provided
by PIN 1 and PIN 2 of the 74LS32. 

I have also added a HALT signal that will always be low with an inverter which is then 
connected to the final AND gate that gives the output.

![detail](/img/8/clock_pc.jpg)

![all](/img/8/clock_all.jpg)

## Principle of Operation

This circuit has 4 inputs and 1 output. 3 inputs consist of output signals from the Astable pulse,
Manual pulse and Select switch pulse. The last input is from the HALT signal.

If the select is ON and the Astable signal is ON, the AND gate will have a 1 in its output. In the
second AND gate when the select is ON the inverter with invert this to a 0 which will be fed into
the AND gate. Irrespective of whether the Manual pulse is 1 or 0, the presence of the 0 on the other
terminal is make the AND gate give a 0. Only when the select is in OFF state that this AND gate can
give a 1 depending on also the state of the Manual pulse.

The output of the 2 AND gates is fed through an OR gate which is now fed into the final AND gate together
with the input of the HALT signal.

## Improvements & Mods

The clock circuit is by no means complete. I already see ways I can make it more efficient and
also more safer. The new LED that I added is not protected by a resistor, hence its high bright
light which is as a result of drawing alot of current.

This computer clock will be an integral part of the whole 8bit computer. The next section will be
making the Register and Arithmetic Logic Unit.

## Index

* [8bit Home](https://www.githuka.com/posts/8bit-home/)
* [---Clock Module]()
* [---555 Clock Signal Basics]()
* [---Monostable]()
* [---Bistable]()
* [---Complete Clock]()
* Arithmetic Logic Unit
* Random Access Memory(RAM) module
* Program Counter
* Output Register
* Bringing It All Together
