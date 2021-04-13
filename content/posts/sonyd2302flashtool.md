---
title: "Flashing SONY Xperia M2 Dual"
date: 2021-03-15T23:49:27+03:00
draft: false
---
If for anychance you brick your SONY Xperia M2 Dual and you cannot boot it,
there are chances that it needs to be flashed clean. This manual will describe
the process of a Linux machine.

## Requirements

* A good internet connection
* USB cable
* Memory
* Time and Patience

## System Preparation

First and foremost ensure that your system is updated.

```
sudo pacman -Syu
```

### Change to root user

```
sudo -i
```

### Then add the ruled

```
cd /etc/udev/rules.d

echo 'SUBSYSTEM=="usb", ACTION=="add", SYSFS{idVendor}=="0fce", SYSFS{idProduct}=="*", MODE="0777"' > 63-sonyxperia.rules
```

### Finally Reload udev rules
```
udevadm control --reload-rules
```

### Download Flashtool

Next grab the FlashTool app from [Flashtool](http://www.flashtool.net/downloads.php) and unzip it somewhere. 

### Install Java Dev Kit
```
pacman -S jdk-openjdk
```
### Download SONY Xperia Stock ROM

* [SONY Xperia M2 Dual Stock ROM](https://xperiastockrom.com/sony-xperia-m2-dual-d2302)

## Flashing

Next thing is to open the FlashTool GUI and begin flashing the device.

### Run as root
```
sudo -i
```
### Navigate to the FlashTool directory and run it
```
cd /etc/udev/rules.d
./FlashTool
```
If the flashing is successful, the logs will say so.

## References
* [Sourcey](https://sourcey.com/articles/flash-android-sony-xperia-on-linux)
