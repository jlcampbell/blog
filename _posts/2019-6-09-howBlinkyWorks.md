---
layout: post
title: How Blinky Works
---

I am learning embedded development on an MSP-430 Launchpad kit.

What follows is what I had to do to blink a light, and how it works.

1. Download Code Composer Studio.
2. Connect your board via usb to windows machine. It should be possible to use a Mac, but I had no luck.
3. Open a new project, Select MSP430G2553. I luckily happened to find the "553" part in the quick start guide, because it wasn't anywhere on the board or the box, but it was absolutely neccessary to get it to work.
4. Select blink from the starter projects.
5. Confirm, and once the project loads, go to build - > "build all"
6. Debug - the moment of truth. If you are lucky this will launch debug mode, and allow you to step through the starter code
7. Set a breakpoint in your while loop. You can step over and continue to see the red light blink on the board

The code.
```
/**
 * blink.c
 */
void main(void)
{
	WDTCTL = WDTPW | WDTHOLD;		// stop watchdog timer
	P1DIR |= 0x01;					// configure P1.0 as output

	volatile unsigned int i;		// volatile to prevent optimization

	while(1)
	{
		P1OUT ^= 0x01;				// toggle P1.0
		for(i=10000; i>0; i--);     // delay
	}
}
```
Explaination:
Take a look at the memory explorer in debug mode.
`P1DIR |= 0x01;` sets the direction of port 1.0 to 0x01, which is hex for 1. The direction of 1 means the port will be Output.

![alt text]( "Logo Title Text 1")




