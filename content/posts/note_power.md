---
title: "12V DC Power"
date: 2020-09-22T13:51:37+03:00
draft: false
---

## Introdution
The Nissan Note comes with a 12V 40mAH Lead Acid Car battery which is used
for starting the car's engine and also powering essential devices in the
car. This project is how I have added an extra car battery which will be
located at the back and power other devices.

Its not wise to use the primary battery since when its low its hard to start
the engine.

## Circuit

The circuit that am working on shall have an input of 12VDC from the secondary
battery and an output of 12V & 5V. The 12V from the battery will go through a
12VDC switch or 12VDCisolator and then a 12VDC Fuse for protection. Next a single
12V line will connect to a socket lighter and the other one to a 12V-5V stepdown
ciruit for other low voltage peripherals. Such loads can be:

* RaspberryPi
* Router
* Camera
* Phone Charger

The circuit is shown below:

![image](/images/schematic.png)

## Power Consumption for the Rpi

My secondary battery is a 12V 32Ah battery.Therefore, that 32AhX12V=384Wh

The Raspberry Pi draws about 500mAh when idle at 5V so the power output is 0.5X5=2.5W

Taking an ideal situation(which would be rare) 384/2.5 will give 153.6hours which is 6.4 Days

The Pi can run on the battery for 6 days without recharging, but this would mean draining the 
battery to complete depletion which is not good for a car battery.
## Tests

## Conclusion
