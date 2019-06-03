---
layout: post
title: Embedded Engineering: My first stab at blink on MSP-EXP430G2
---

Today I tried to connect my mac to my MSP-EXP430G2 launch pad kit (from texas instruments).

I was following instructions from here: https://embedded.fm/blog/2016/4/25/ese101-blinky-and-breakpoints

I downloaded and set up Code Composer studio, and opened up the blink starter project. Everything built fine. But when I plugged the board in and got to the debug stage, i got this error:

```
Error initializing emulator:
No USB FET was found
```

Even though I got this board in the last 6 months, apparently only the new 430- F series launchpad kits work with mac.

I will try with windows tomorrow!
