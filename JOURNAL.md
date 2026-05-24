---
title: PCBCard
author: Kwame
description: A small introductory business card made from PCB, goal is to include a small heart rate sensor or pulse ox for a uniqueness factor!
created_at: 2026-05-23T11:59:01-05:00
modified_at: 2026-05-24T04:54:14-05:00
---
# May 23rd, 2026

I wanted to build an interactive digital business card with 3 main features (maybe more later).

1. An **NFC tag** that automatically opens a link to my digital garden / e-portfolio when scanned by a phone.
2. A **sensor** to read a user's heart rate when they touch the card.
3. A cluster of **LEDs** that flash in sync with their pulse.

I'm extremely new to hardware design, so my main goal today was just getting the foundational stuff down. Here is what the schematic and layout looks like so far:
![[images/Screenshot 2026-05-23 at 15.53.26.png]]
![[images/Screenshot 2026-05-23 at 15.53.15.png]]

The absolute hardest part of today was sourcing the right NFC chip. Because the card needs to be slim and run on a tiny coin-cell battery.

I initially stumbled onto the _nRF5340-QKAA-R7_, which features integrated Bluetooth and NFC. However i came to realise that 1. it's a semiconductor and 2. it uses 94 very very very small pins, which would be impossible for me to solder.

Instead, I found a much simpler option, using the **ATtiny85 microcontroller** as the main brain, and as for the NFC functionality, I spent a lot of time digging through SnapEDA and settled on **NT3H2211W0FHKH**

Because it’s a dedicated tag, it features an I2C interface (`SDA` and `SCL`) that shares the exact same data wires as my heart rate sensor, saving valuable pins on the ATtiny85 (from what I understand).Another cool aspect is that it has a `VOUT` energy-harvesting pin and an `FD` (Field Detect) pin that signals the ATtiny85 the exact moment a smartphone interacts with the card's magnetic field (opens doors to some other ideas i could implement).

I plan to design the visual desgin in Affinity, export it, and import the line art directly into KiCad's silkscreen layer. I also want to wrap a custom 4-turn copper loop antenna around the entire outer edge of the card to act as the NFC receiver, while styling the internal copper traces to look like spider webs radiating out from the ATtiny85 brain.

**Time Spent:** ~2.75 hours

# May 24th, 2026

It's currently 4 am (Now like 4:50). I woke up motivated to to clean up my design, and I did just that. I found some tips from [this video](https://www.youtube.com/watch?v=S24RvYZWYUQ), and some other forum posts as I worked to clean up my schematic. Now it looks like this:

Much cleaner I'd say, now to move on to figuring how to add images & nice looking text & symbols.

**Time Spent:** ~45 minutes