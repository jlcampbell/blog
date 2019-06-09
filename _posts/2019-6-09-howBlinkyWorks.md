---
layout: post
title: How Blinky Works
---

I am learning embedded development on an MSP-430 Launchpad kit. Why? It seems really challenging, and after doing web development all day I want do to something else.

What follows is what I had to do to blink a light, and how it works.

Step 1: Download Code Composer Studio.
Step 2: Connect your board via usb to windows machine. It should be possible to use a Mac, but I had no luck.
Step 3: Open a new project, Select MSP430G2553. I luckily happened to find the "553" part in the quick start guide, because it wasn't anywhere on the board or the box, but it was absolutely neccessary to get it to work.
Step 4: Select blink from the starter projects.
Step 5: Confirm, and once the project loads, go to build - > "build all"
Step 6: Debug - the moment of truth. If you are lucky this will launch debug mode, and allow you to step through the starter code
