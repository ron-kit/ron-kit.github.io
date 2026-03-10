---
image: "images/boxbot.jpeg"
title: "Copper Dome"
date: 2026-01-28T11:56:37-08:00
---


At the [BoxBots](https://boxbots.devpost.com/) hackathon, we were challenged to make a robot that could do something cool using only cardboard for building materials.

Over the course of 36 hours, [Yufeng](https://x.com/yufeng_liu15), [Daniel](https://x.com/bskdany) and I made **Copper Dome** - an arm mounted, ~auto targeting~,  ~completely safe~ rocket launcher.

# How and why

I have never done a hackathon before, as I am not big on software, and the premise of most of them is "code for 48 hours". When my co-intern and friend Yufeng told me about this hardware one though, I knew I had to join him.

The challenge started Friday evening, but in Waterloo, so we took the day off for travel. It was a 9 hour one way trip involving a rideshare, go train, and shuttle bus (even longer coming back since there was a snowstorm), but we arrived unscathed, if a little late.

Once our team was assembled we began plotting, and quickly found a shared interest in rockets. Daniel proposed the insane sounding but very funny idea of a missile launcher and we were immediately on board. We went to buy some teeny tiny A-class rocket motors and started prototyping.

{{<image src="camera.png">}}

The original idea was very ambitious. One of the organizers/sponsors was a fan of Iron Man, and had a correspondingly themed prize bracket, so naturally we wanted to integrate JARVIS into the launcher for voice activated aiming and firing. Alas, due to a combination of my hacking inexperience and the limited availability of electronics, I couldn't get any of the cameras to transmit data that the Arduino could see. Perhaps we can make this a reality at a later date.

As the only hardware/mechanical guy I had to connect all the circuits and components together, and design the cardboard frame, which took a surprising amount of thought to make it comfortable for the user (even though it ended up being myself). 

{{<sidebyside left="images/pensive.jpeg" right="images/sleepy.jpeg">}}

After lots of iteration and rescoping, we had a product, complete with a rocket mount, servo aimer, power system, and arduino program to control it all. 

# In operation

Yours truly operating the device:

{{<video src="rocket.mp4">}}

Plans to commercialize are underway.