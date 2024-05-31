+++
title = "PhobGCC 2.0.2 Makes Firmware Updating Easier, Connection to C-Stick More Reliable"
date = 2022-12-22T22:54:24-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/phobgcc/2.0.0.jpg"
tags = ["news", "software update", "firmware update", "gamecube controller", "smash bros", "phobgcc"]
keywords = ["phobgcc", "phobgcc 2.0.2", "open-source firmware", "phob controller", "gamecube controller", "super smash bros. melee", "ssbm", "melee"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
PhobGCC. Chances are you've probably never heard of it. Allow [GitHub](https://github.com/PhobGCC/PhobGCC-doc) to explain what it is:
> The PhobGCC is a replacement motherboard for Gamecube controllers that reads stick position using magnets and Hall effect sensors instead of potentiometers that can wear out. It offers an advanced digital snapback filter that doesn't reduce responsiveness and actually improves responsiveness in *Melee*. It also features gate calibration, swappable buttons, and facilitates installation of discrete switches on the D-pad and face buttons.

Basically, it's an open-source PCB for the GameCube pad. It's mostly aimed toward competitive *Smash* players, since it makes "a high-performance, customizable, long-lasting controller." I'll get into more details about it in tomorrow's review.

Since the design is open-source, you can freely [print and customize the PCB yourself](https://github.com/PhobGCC/PhobGCC-doc/blob/main/For_Makers/Phob2_Ordering_Guide.md) (although it seems *very* complicated...good thing I have a pre-built one), and it comes with updates. Today, version 2.0.2 of the board released. Here are the new features:
- RP2040 microcontroller chip directly soldered on for consistent availability
- Easier firmware updating; simply hold the button while plugging in USB and drag-and-drop a firmware file
- PhobVision composite video output for guided calibration and graphical configuration with written explanations
- SMD-mounted Hall Effect sensors for consistent placement
- Low-noise discrete ADCs for Hall Effect sensor measurement
- Digital communication with the C-stick daughterboard for a more reliable connection
- Reoriented C-stick daughterboard connection to reduce strain on wires
- All pads have been revised for easier soldering, with oval footprints and thermal relief between pads and fill
- Main stickbox now is oriented the same as in an OEM controller
- Separate Z button pads for shell-mounted mouseclick Z and reverse Z
- Extra USB connections for use with Model U daughterboard to provide USB-C GCC cable support and flashing without opening the case
- Four extra GPIO pins exposed for miscellaneous other uses

See the patch notes on [GitHub](https://github.com/PhobGCC/PhobGCCv2-HW/releases/tag/v2.0.2).

*Cover image credit: PhobGCC team*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
