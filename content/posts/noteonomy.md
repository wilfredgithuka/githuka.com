---
title: "GNP - Githuka Noteonomy Project - Index"
date: 2021-08-26T13:46:48+03:00
draft: false
---
## Introduction

A self-driving car, aka autonomous vehicle, connected and autonomous vehicle (CAV), full self-driving car or driverless car,
or robo-car or robotic car, is a vehicle that is capable of sensing its environment and moving safely with little or no human input.

Manufacturers have been announcing the arrival of autonomous vehicles since March 2017 with leading companies predicting that
2020 shall be the golden year for autonomous vehicles. Much of this was projections but not actual deliverables due to
challenges like legal provisions which would hinder this development.

![nissan-note](/img/gnp/note.jpg)

The Githuka Noteonomy Project is a longterm learning process about the interesting word of autonomous vehicle systems.
In this project am using a mini rc vehicles, software model vehicles and a real vehicle - Nissan Note E11 2008 as I start adding devices
in it towards converting it into a connected car. The Nissan Note E11 2008 Model is a 5 door mini MPV hatchback manufactured by Nissan Japan.

A connected car is a term use to describe a car that can interface with the Internet for exchange of information. It becomes
an IoT (Internet of Things) device. I plan to add devices such as a Raspberry Pi, CAN Bus reader, Car Wifi etc.

For a car that was made in 2008, it a big task since the Nissan did not envision such for the car to hold so much devices. The place to start this
project is power. Having a reliable power system is a good foundation for any device that shall be mounted. I plan to have a secondary power system
which will not interfere/drain the car's primary battery.

This project is divided into the following major categories:

* Noteonomy - These is the main project which focuses on the Nissan Note vehicle related project.

* NoteonomyRC - All projects that revolve around modeling and concepts on small RC vehicles.

* NoteonomyDoc - Project Documentation Service

## Nissan Note E11 Details

* Make: Nissan Note
* Model: DBA E11
* Engine: HR Type
* Engine Capacity: 1490 cc

### Brief Project Update

## Most Recent Updates

* [Carputer GUI & Cockpit]({{< ref "/posts/carputer_update">}})
* [Personalising Vehicle Service]({{< ref "/posts/service">}})
* [ECU - Engine Control Unit - What Lies Inside The This Device?]({{< ref "/posts/ecu.md">}})
* [Computer Vision & Deep Learning]({{< ref "/posts/computer-vision.md">}})
* [Driving Report 20210709]
* [Vehicle Status Dashboard Display - 0.91 inch OLED Display]
* [Carputer Power Testing Using the 150W DC-DC Boost Converter 10-32V to 12-35V]({{< ref "/posts/boost_power.md">}})
* [Installation & Review of MC-7023 Android Car Media Player]({{< ref "/posts/longonot.md">}})
* [70mai Dashcam Modding & RTPS Hack]({{< ref "/posts/morse.md" >}})
* [70mai Dashcam Review]
* [Revised Phone Charging Station](https://www.githuka.com/posts/note_phone_charging)
* Driving Report - 20201207
* X6 Generic Bluetooth Device Testing Report
* Safcom BigBox Serial Read Attempt Experiment Report
* SONY D302 Flashing
* A9G Pudding Device

## Project Structure

### Manual

This section deals with the official Nissan Note E11 manual. Its a very large
PDF document which forms the foundation of this project. I must say that Nissan
put alot of effort in this. However I find it hard to navigate so I have started to
split it into smaller manageable sections to increase efficiency.

This manual contains maintenance and repair procedures for the NISSAN
NOTE, model E11 series. In order to assure your safety and the efficient
functioning of the vehicle, this manual should be read thoroughly. It is
especially important that the PRECAUTIONS in the GI section be completely
understood before starting any repair task.

All information in this manual is based on the latest product information
at the time of publication. The right is reserved to make changes in
specifications and methods at any time without notice

The original manual is 68MB and can be downloaded here.

### Wireless Communication

This section is about all wireless Communication media that is available in,
around and outside the vehicle. The Nissan Note comes with various Wireless
Communication interfaces like the key fob and key-less starting. I have added
more wireless communication modes like Bluetooth and Wifi which require in-depth
understanding and documentation. In this section I have the following projects
which are currently underway:

* In-Vehicle Wifi Project
* hAP Wifi Router
* A9G Project
* Home-Car Wifi Build
* SONY Xperia In-Vehicle Wifi

### Carputer

The Carputer is by far the most difficult yet most rewarding project that I Have
been working on since I bought this car. All the other projects revolve around
this important component, the computer. Most modern cars have some sort of a
computer which controls the functions of the car. I want and need to take this
a notch higher and build a more powerful computer in the car.

My Carputer is running on Archlinux and is currently done at 70% What am working
now is system integration with the car's computer and power issues.

### Power System

Power is everything.

Power is nothing without control.

My car came with a single 12V Lead Acid Battery. With time this has become a bottle
neck to power more devices in the car, so am in the process of adding a dual Battery
system for the car. This will see the addition of another Deep Discharge Battery
which will power the peripherals leaving the main battery for starting the car only.

This dual battery power system will need its own wiring and cabling that meets
all safety aspects of a Nissan.

### Cameras & Computer Vision

Cameras enable the car to see more and react to visual data. Cameras are at the
heart of most modern vehicles and this is a crucial part of this project. What
the Cameras see is what will be relayed to the computer for processing and
backup. Implementing a full image processing pipeline is what I am aiming for.

So far I have got a great dashcam that is a starter for this project. Having the
dashcam stream the video feed to the Carputer is what is challenging me.

All these cameras will need power and here is where the Power System comes in,
is a whole mesh of connected devices on the move:-)

### Security

Security is quite a sensitive topic. Thats for another day.

## Safety Notices

While working on such a project can be interesting and a good learning process
I however want to stress upon the concept of safety. If you want to attempt what
you've read here, remember to consult the Official Nissan Manual.

Do not tamper with a system that you are not sure about. Consult a qualifies NISSAN
technician

### Electrical Safety

* The starting current of the starter can reach upto 120A DC. This is very dangerous.
* Do not shrt circuit the battery terminals.
* Do not leave the car battery at a lower voltage for too long.
* Have a secondary battery to power your peripherals. Leave the primary battery just for starting the engine.

## Projects Dowloads

* [Autonomous Car PPT](https://www.githuka.com/files/autonomous_car_ppt_pdf.pdf)
* [Noteonomous PPT](https://www.githuka.com/files/noteonomous.pdf)

## References
