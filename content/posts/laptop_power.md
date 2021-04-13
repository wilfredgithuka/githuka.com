---
title: "Building A Linux Carputer - Power Sytem"
date: 2021-04-10T20:19:56+03:00
draft: false
---

Requirements

* Boot on power connection
* Have a backup battery
* Wake up on LAN/WoW
* Minimum power requirement during running and standby
* Sleep/Hibernate Mode
* SSH Server Running
* Headless operation


## Boot Steps
* Wake up on LAN/WoW
* Create a Wifi Network Static IP Address
* Start SSH Server
* 

Following the above requirements lets build a special purpose car computer.

Th first thing to do is to ensure that I can connect to it and print 
out the sytem details (KYD = Know Your Hardware). hwinfo is a powerful 
hardware detection tool come from openSUSE. This will be sufficient for
now. The output of hwinfo can be messy and overhelming so just sending
it to a file is enough

```
sudo hwinfo > hardwareinfo.txt
```
This old laptop is powered by a an AMD E-300 APU with Radeon HD Graphics
card. The AMD E-300 (codename Zacate) is a dual core processor for small 
notebooks and netbooks. It offers a relatively powerful integrated 
graphics card and a single channel DDR3-1066 memory controller. This CPU is
rated at 18W which is good for in-vehicle power requirements. It also has
a maximum temperature of 90 Degrees while it can achieve Core C1 and C6 states
of low power.

## Network Connection - Going Headless
I plan to run this computer headless inforder to reduce its power conumption since
the screen draws too much power. With SSH I can accomplish all that I need to do.
Before going headless I need to make sure that I can SSH into it as soon as the boot
sequence is complete.


## Power Consumption

The goal here is to reduce the power consumption to as minimal as possible.

This laptop is powered by a normal charger which takes in 240V (100-240V) AC and draws
1.8A at 50-60Hz. The output is 19V DC at 3.42A

Input: 240V AC

Output: 19V DC

The main challenge I forsee is to see how I can drop the 19V to 12V which is widely
available on the vehicle. Using the power formula, P=IV, the power drawn is 65W. By running
headless, without the screen I forsee I can drop the power consumption to 30W. Also by
shaving off the old harddrive for an SSD should drop further the power consumed. 

First I need to understand the power consumed by each device

Advanced Configuration and Power Interface (ACPI) is an open industry specification 
codeveloped by Hewlett-Packard, Intel, Microsoft, Phoenix, and Toshiba.ACPI establishes 
industry-standard interfaces, enabling OS-directed configuration, power
management, and thermal management of mobile, desktop, and server platforms.

The ACPI system allows only four possible C-States; C0, C1, C2, and C3

For Linux based OSs, the OS can request C-states, either using the ACPI idle driver (acpi_idle)
or through the use of the intel_idle driver.

To find out what idle driver Linux is using, one can issue:
```
cat /sys/devices/system/cpu/cpuidle/current_driver
```
This computer runs the acpi_idle




