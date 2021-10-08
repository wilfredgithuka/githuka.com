---
title: "Carputer GUI & Cockpit"
date: 2021-08-28T19:36:51+03:00
draft: false
---
Today I made some progress in making the Carputer more efficient and
easy to work with. After solving some prevalent power issues, I finally
got it running again. The power switch is still done by briefly shorting
two wires, which is not a safe way to start a computer. The battery is still
intact. Currently I power it via my desktop power supply mimicking a car battery.
You can read about this connnection in this earlier post.

![terminal](/img/gnp/terminal.jpg)

I have been toying around with different server GUI apps to control the carputer
via a web interface. My ideal installation would be the Carputer shall be in the
boot, out of harms way and it shall be controlled wirelessly via a web interface right
inside the browser.

## Cockpit

The easy-to-use, integrated, glanceable, and open web-based interface for your servers. 
Cockpit is a web-based graphical interface for servers, intended for everyone. Thanks to Cockpit 
intentionally using system APIs and commands, a whole team of admins can manage a system in the 
way they prefer, including the command line and utilities right alongside Cockpit.

### Installation

Install the cockpit application

```
sudo pacman -S cockpit
```
Start the cockpit service

```
sudo systemctl enable --now cockpit.socket
```

Open the browser and point it to: 

```
http://192.168.100.xx
```

### Running

Use your system user account and password to log in. See the guide for more info.

After installing Cockpit itself, consider installing additional applications in Cockpit.

Cockpit runs preety smooth with minimal system resources. With the additional applications,
its quite a handly tool for system overview management. What is remaining is once the battery
has charged, I plan to test it out in the car and see how the interface behaves.

### Appearance

Here is cockpit running without the additional applications.

![cockpit](/img/gnp/cockpit.jpg)

