+++
title = "Electromagnetic Sticks for Steam Deck: Should You Upgrade?"
date = 2023-09-27T13:55:59Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/accessories/gulikit_sticks/cover.jpg"
tags = ["hardware review", "accessory review", "steam deck", "gulikit", "analog sticks"]
keywords = ["gulikit steam deck sticks", "steam deck electromagnetic sticks", "gulikit", "steam deck", "electromagnetic analog sticks", "hall effect sensors"]
description = "Joysticks with hall-effect sensors...sounds like a good upgrade, right?"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Sooner or later, your controller, or your Steam Deck, will experience this phenomena called "stick drift." This is because the potentiometers on the sticks will wear over time. As they wear, stick drift becomes evident. You'll find that the camera is constantly moving around in a circle, or your character starts walking on their own.

There is a solution to this problem, although it's often more expensive. Sticks can use hall effect sensors instead of potentiometers. These sensors don't wear over time. The result is, you'll have long-lasting sticks that won't ever suffer from stick drift.

[Note: installation video available on [YouTube](https://youtu.be/QDP8ny2lAvA).]

Gulikit kindly sent over a pair of their [electromagnetic Steam Deck analog sticks](https://gulikit.com/productinfo/1026071.html) for my review. Their sticks are advertised as having hall effect sensors, which "fixes issues like joystick drift, blind spots, dead zones, no click, no centering, broken and loose sticks." For $30, you get both the left and right thumbstick. Sounds a lot less expensive than getting the vanilla sticks from iFixit for $20 a piece, right? And have the hall effect sensors to boot? Sounds like a great, inexpensive upgrade!

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/gulikit_sticks/contents.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

They sent me the second revision of their sticks. In the first edition, you had to solder the wire in if you wanted the touch-sensitive capabilities of the sticks. Thankfully, with the second edition, soldering is no longer required. Additionally, according to Gulikit, these sticks use "50% less power" than the original version.

# Package Contents
The box that I got was bare minimum: a small box containing the two sticks, surrounded by a layer of plastic, and nothing else. No instruction manual provided. Just how I like it. Almost nobody reads the instruction manual these days; it just wastes paper.

Aside from the way the stick is assembled underneath the thumbstick cap, the Gulikit sticks look and feel exactly the same as the vanilla thumbsticks.

(Note: the gray and yellow stickers on top of each stick aren't included; they were part of my [DeckCube project](https://linuxgamingcentral.com/posts/deckcube/).)

# Type A, or Type B?
The Gulikit sticks have a switch on the PCB. This allows you to seamlessly swap between Type A or Type B. The reason for this, is because the Steam Deck ships with two separate controller IDs. If you go into Settings -> System -> Scroll down to the About section, you'll find your Steam Deck controller ID. If the first four letters start with "MEDA", you have Type A sticks. If it starts with "MHDA", then they're type B. In my case, I have Type A. So I would flip the switch on the back of the sticks to "A".

![Steam Deck controller ID](/images/steam_deck/accessories/gulikit_sticks/controller_id.jpg)

Setting the right mode is important because, according to Gulikit's website:
> Each Steam Deck is installed with one of two different models of thumbsticks, Type A or Type B. Although nearly identical, **capacitive touch capability relies on the correct type to be installed.**

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/gulikit_sticks/switch.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

# Installation & Calibration
Installing the Gulikit sticks (at least, as far as the second edition ones are concerned) is exactly the same as if you were replacing your old sticks with a new set. Just take the back eight screws off the Steam Deck, pry the shell open, unscrew the three screws holding each stick in with a Phillips screwdriver, remove the ribbon cable, take the stick out, and put the new stick in. Repeat these steps in reverse. Make sure you have the MicroSD card removed prior to taking the shell off, if there is one inside. If you're feeling extra cautious, you may also want to discharge the battery below 25% to avoid a mess should you accidentally puncture it.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/gulikit_sticks/installation.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

One extra step is required after installation, however. You're going to want to **calibrate the sticks**, because chances are, the sticks are going to be misaligned. To do so, you'll need to go into Desktop Mode, open up a terminal, and run `thumbstick_cal`. The terminal will walk you through the process of re-calibrating the sticks. Steam will close, and you will be prompted to keep the sticks center in place. After pressing A, the terminal will prompt you to rotate each thumbstick twice by a full 360 degrees. Press the A button again. Then you're all set. Your sticks should be much more center now.

Go back into Game Mode, go to Settings -> Controller -> Calibration & Advanced Settings -> Open. Here you can test both the left stick and the right stick, and adjust their deadzones if you desire.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/gulikit_sticks/calibration.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

# Some Issues
**UPDATE (10/2/2023): After replacing the ribbon cable to the sticks, the sticks now function properly. Right stick touch works, and the left stick registers "up" all the way now. More details [here](https://linuxgamingcentral.com/posts/psa-you-can-use-10-pin-cable-for-steam-deck-sticks/).**

I ran into a few issues after replacing the vanilla sticks. Particularly with the left stick. I noticed just a few minutes after calibration, pressing up on the stick only partially moved the "needle" upwards. So, say for example I'm playing *Crisis Core Final Fantasy VII Reunion*. When I press the left thumbstick all the way up to make the character move forward, he just walks. He doesn't run. For some reason, the stick just doesn't want to register the fact that I'm pushing the stick all the way up. Strangely enough I wasn't having these issues with the right thumbstick.

Here's another problem. Think there's touch capability with these sticks? Not in my case, even after setting the sticks to the right mode. The left stick touch works, but for the strangest reason, the right stick touch doesn't.

I will admit this may be my fault though. After having replaced the sticks in my Steam Deck dozens of times, I think the ribbon cables may be a bit damaged. I can't think of any other reason why the left stick touch works but the right stick doesn't. According to [r/SteamDeck](https://www.reddit.com/r/SteamDeck/comments/zmr1nf/can_i_buy_new_ribbon_cables_for_the_steam_deck/), the ribbon cables the thumbsticks use are 10-pin ZIF with 0.5 mm pitch. I have ordered a few cables. Once I replace them, I will update this review if I observe any changes.

# It's Worth the Upgrade
The Gulikit sticks work just fine after getting a new set of ribbon cables. Originally I was having a hard time with the left stick since it wouldn't go "up" all the way, but that problem has been fixed since I got the new ribbon cable. The new cable also solves the problem that I had with the right stick touch not working.

So, all-in-all, it's definitely worth getting once your vanilla sticks start drifting. It's going to be less expensive than getting new sticks from iFixit, they look and feel exactly the same, and yet, since they're using hall-effect sensors, they have the added benefit of not suffering from the dreaded stick drift.

Only question that remains now is, how long will these sticks last in, say, a year or two from now. Will I encounter any issues with these sticks at that point? It's hard to say at the moment.

**TL;DR**

The good:
- easy installation; no soldering needed
- supposedly uses 50% less power than the first edition
- look and feel exactly like the original sticks
- less expensive than the original sticks
- no stick drift with hall effect sensors

The not-so-good:
- none so far!

*Thanks to Gulikit for sending these over for review.*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
