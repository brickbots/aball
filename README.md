# aball
aball - A Buttonless trackball for all

![aball image](./photos/finished_single.jpeg "The aball")

## A trackball with no buttons?
I like keyboards, and my workflow is defintely *keyboard first*.  Tiling window manager, VIM, bash... pretty 
much all the keyboard I can get.  Yet, however hard I try, there is always some need for a pointing device.  
So this is my stab at a trackball for keyboard first workflows.

Why not a mouse?  Well, space... trackballs take up less space.  Which got me thinking, what is the minimum 
footprint for a usable trackball?  I managed to get it down to 60x80mm... you could go even smaller, but I 
wanted some sort of case on it and this particular size sits nicely next to my daily driver, the [Kyria](https://blog.splitkb.com/blog/introducing-the-kyria).

![aball beside Kyria](./photos/kyria_wide.jpeg "aball with Kyria")

In the quest to reduce size, I did away with any buttons.  I have plenty of buttons on my keyboard, and my 
left hand is capable of pressing them when I'm using the aball with my right hand.  Via a layer, I've 
mapped buttons on the home row to:
- F: Left Click
- D: Middle Click
- S: Right Click
- G: Scroll Up
- B: Scroll Down

Scroll up and down are not really needed, but they are pretty handy, even when not using the trackball.  

## Design Info / How it works
Aside from having no buttons and being as small as practical, I wanted the aball to be pretty easy to build and
potentially serve as a jumping off point for other designs.  So I kept these things in mind:

* Readily available parts
* Low cost
* Simple to assemble
* Majority 3d printed if desired
* Supports 38 and 34 mm balls

The design is pretty stripped back, here is a shot of the guts which are self supporting and can be used just as is:

![aball minimal implementation](./photos/aball_min.jpeg "aball minimal implementation")

The ball sits on a 3d printed frame which holds three roller bearings, and a microcontroller.  The ball moves on top of an optical mouse sensor 
which is connected to the microcontroller. To make the whole thing as close as possible to the desktop, the mouse sensor sticks out
of the bottom of the case, but only a bit and is off the desk due to the rubber feet on the bottom.

### Quick note on roller bearings

If you have not used a trackball with roller bearings before, I think you are in for a treat.  It takes a day or two of good use to 
break them in, but I find them *much* smoother and more enjoyable than static dot type bearings.  You can go cheap here, spending 
less than a dollar for all three of them and they will still be pretty good.  However, a nice set of high quality bearings for RC 
use are not that much more expensive and the quality is definitely higher.

### Firmware

The microcontroller runs firmware based on QMK (Quantum Mechanical Keyboard).  QMK is a fantastic
open source project for keyboard firmware, but it also includes pointing device support.  You can find
the firmware source for the aball here: 
[https://github.com/brickbots/qmk_firmware/tree/aball/keyboards/handwired/aball](https://github.com/brickbots/qmk_firmware/tree/aball/keyboards/handwired/aball)

The minimal implementation is pretty much what you see above and it can be put together for well under $40 if you already have a 3d printer.  From 
there you can either 3d print an enclosure, or use the files here to get some acrylic and metal laser cut for a different look.  I hope that other folks
will adapt these guts and come up with new and clever case options.  Maybe even add buttons on-board :-)

## How can I get one of these?

You can build one yourself!  This repo contains design files, build guides, and a parts list so you can build your own **aball** if you
so choose.  If you do, please drop me a note at rich@brickbots.com.  All information here is provided as-is
for your personal use and is released under a specific Creative Common license which lets you use them for 
non-commercial use.  Please see the included LICENSE file for details.

If you are ready to learn more, or even get started on your own aball, click below to keep exploring

* [Build Guide](./docs/bg_getting_started.md)
* [Parts list (BOM)](./docs/bom.md)

Thanks and email with any questions to suggestions!
