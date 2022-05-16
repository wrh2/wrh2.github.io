---
layout: post
title:  "My Embedded must haves at home"
date:   2021-05-15 17:00:00
categories: Embedded Systems
visible: 1
---

## Introduction

Since the onset of the COVID pandemic in the US, I like many others have been working from home a lot more. During that time, I've really dialed in my home setup, and I wanted to share with you my must haves for embedded development at home. Now, when I am talking about embedded development, I'm not just talking about plugging in an arduino or nucleo dev board to your PC via USB; I'm talking about testing, debugging, and developing on a PCB that may or may not have a microcontroller. For me, everything on this list is needed for a good embedded setup, but that may not be the case for you so I'm going to break this list down in to three categories: the essentials, the accessories, and nice to have.

### Disclaimer

Not all embedded development can be done at home. Your needs will vary based on the embedded system that you are working on. The items that I list here are suited for lower voltage applications (<30V), and lower current (<3A). I am also not sponsored by anyone so I'm not being paid to post links to any vendors/distributors, they are just meant to be a general reference/starting point. Everything I list, unless otherwise noted, is something I have had experience using in my home setup.

## The Essentials

These are the fundamental tools needed to do embedded development at home. Without these, you can't do more than read datasheets and simulate stuff on your computer!

### Solderless Breadboard

This is the basic building platform for you to quickly prototype circuits on. Think about it like a [LEGO baseplate](https://www.lego.com/en-us/product/gray-baseplate-10701) where you can just plug in legos to build what you want. With a solderless breadboard, you can take something like [this eval board for an IMU](https://www.digikey.com/short/mnfhrfz2) and plug it right in, allowing you to have access to the pins on the chip. I recommend going with something like the [full size solderless breadboard from SparkFun](https://www.sparkfun.com/products/12615). Many shapes and sizes are out there so look around to find one that meets all of your needs.

### Jumper wires

The next thing you'll need is jumper wires to connect stuff together on your solderless breadboard. I honestly can't ever get enough of these. They are available from many places but I tend to use ones fron Adafruit and SparkFun.

Here are their offerings on Digi-Key

[Adafruit jumpers](https://www.digikey.com/short/5w7hq0tw)

[SparkFun jumpers](https://www.digikey.com/short/0q0jrc5t)

I usually go with ones like [this](https://www.sparkfun.com/products/11026). I recommend having Male to Male (M/M), Male to Female (M/F), and Female to Female (F/F). But if you are balling on a budget, you can skip the M/F and you can make M/F with M/M and F/F if you need. Also, really helps if you can get a bag to keep them in. Plastic ziplock bags work just fine. Label them appropriately so they are easier to find and store.

### DC Power Supply

Your electronics are going to need power. Most PCBs in an embedded system take some sort of DC input. For powering low current stand alone DC stuff, I really like this [breadboard power supply](https://www.digikey.com/short/t30mjp8q). You can use a standard wall wart (6-12V) and get a selectable 3.3V or 5V rail on either side of your breadboard that supplies up to 700mA, which is great for initial power up on most prototype PCBs.

For higher current stuff, you'll need a programmable power supply. I've really enjoyed [Rigol's DP832A](https://www.rigolna.com/products/dc-power-loads/dp800/). It has 3 channels, 2 0-30V at 3A and 1 0-5V at 3A. My favorite part is the available interfaces for a host machine that allows me to remotely control it. The Rigol UltraPower software is free no frills software that allows me to log voltage and current over time in csv format which is also a nice plus. Visibility is always a big deal in embedded development. If you need something cheaper, with an extra channel but no interfaces for a host machine, then I recommend [FLIR Extech 382270](http://www.extech.com/products/382270). Whatever programmable power supply you buy, make sure to get some [extra leads](https://www.digikey.com/short/bhchdj41)!

### Soldering Station

At some point, you'll likely need to solder something. Could be that you need access to a point on your PCB that doesn't have a connection to a pin header. Could be that you need to modwire something due to an error or a design change. You might not solder often but when you do need it and you don't have it, you'll regret not having a soldering iron on hand.

I really like [Weller's WX2021](https://www.weller-tools.com/professional/USA/us/Professional/Soldering+technology/Soldering+stations/Soldering+stations/Sets/WX2021) 2 channel soldering station. [Digi-Key link](https://www.digikey.com/short/29j1nn4v).

As nice as it is, the WX2021 is an expensive higher end soldering station. You may not want to invest that much for a home setup. There are lots of good cheaper options out there such as [Hakko's FX-888D](https://www.hakko.com/english/products/hakko_fx888d.html). [Digi-key link](https://www.digikey.com/short/t45qbdrr).

Be sure to get some [solder](https://www.sparkfun.com/products/9325), [solder wick](https://www.sparkfun.com/products/9327), and [flux](https://www.sparkfun.com/products/9327).

## The Accessories

Now that we've covered the things that you absolutely need, these are the tools that you can sort of live without, but they really make life exponentially better as an embedded developer.

### Digital Multimeter (DMM)

Multimeter's are extremely handy for checking for shorts, measuring resistance, measuring voltage, and measuring current. I use mine almost every single day at work and because of that I think its worth it to invest in a good multimeter. No multimeter has a better reputation than [Fluke's 83V Multimeter](https://www.fluke.com/en-us/product/electrical-testing/digital-multimeters/fluke-83v). It's sturdy, reliable, and has a ton of functionality. Is it pricey? Yep. Is it worth the price? Definitely. On top of using it for work stuff, I use it around my house for electrical work.

If it is not in the budget right now, then you could get a [much cheaper hobbyist multimeter](https://www.sparkfun.com/products/12966) but I really recommend saving up to get a Fluke.

### Logic Analyzer

A huge part of embedded systems is how modules within the system communicate with each other and how they communicate with the outside world. To that end, you will spend lots of time debugging these communications. A logic analyzer gives you the ability to easily capture this information. I actually find it borderline essential and debated putting it in my essential section. You could live without it but do you really want to? No. I've personally been using [Saleae Logic Analyzers](https://www.saleae.com/) for about 8 years now and have nothing but good things to say about them. I really like that you can use it for both analog and digital signals. The lower end Logic 8 model gets the job done in most cases. If you need higher sample rates and want better analog sampling capability, then go with the higher end Pro models (8 or 16).

I've used cheaper options before such as [Digilent Digital Discovery™](https://www.sparkfun.com/products/17045) but wasn't a huge fan. The function generator was cool though. Of course, there are even [cheaper alternatives](https://www.sparkfun.com/products/18627) that are out there but I don't think they as good as what Saleae's Logic does (I haven't used that sparkfun logic analyzer btw).

## Nice to have

These things are nice to have laying around for various reasons.

### Circuit components

In embedded development, you only need circuit components handy during the prototyping phase, and sometimes you don't end up needing them at all because you aren't trying any new circuits. But occasionally, there arises a need to add a component to the design or try something new out. In that case it is useful to have the following:

* Resistors
* Capacitors
* Inductors
* Transistors
* Diodes (Clamps, LEDs, etc)

#### Bonus components

Only really cool people keep this stuff around ;)

* Logic gates (OR, AND, NOT)
    * You could build these out of transistors if you wanted but don't lol
* D-Flip-Flops
* Multiplexer/Demultiplexer
* 555 Timer
    * Probably the coolest thing ever

With these components you can build all sorts of useful analog, digital, combinational, and sequential circuits!

### PCBite Kit

I am a huge fan of the hands free probing solution available from Saleae called [PCBite Kit](https://usd.saleae.com/collections/accessories/products/pcbite-kit). The needle probes are awesome for probing tight spots on a PCB! The magnetic holders are really nifty as well for holding up a bare PCB.

### Tweezers

Another nice to have piece. Useful when you are soldering or handling surface mount components or just poking around a PCB.

I like [these](https://www.digikey.com/short/rh42vr8w) and [these](https://www.digikey.com/short/w4v5t7wr).

### Vise

Last but not least, a vise is great to have for your work bench. Comes in handy for soldering big time, and is really nice for just holding up bigger bare PCBs. Often times, I find myself using it for other stuff around the house too. I enjoy [this one](https://www.digikey.com/short/0mjbr334) from PanaVise.

## Conclusion

And there you have it, my embedded must haves for my home setup. I hope reading this has helped you get some ideas on how you can improve your home setup for embedded development!