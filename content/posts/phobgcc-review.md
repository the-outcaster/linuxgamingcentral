+++
title = "The GameCube Controller, Powered by Open-Source Firmware"
date = 2022-12-23T07:44:47-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/phobgcc/cover.jpg"
tags = ["hardware review", "accessory", "gamecube", "smash bros", "phobgcc"]
keywords = ["phobgcc", "gamecube controller", "smash bros.", "super smash bros. melee", "ssbm", "open-source firmware"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
If you follow me on [Mastodon](https://mastodon.social/@linuxgamingcentral), you're probably aware that I'm a bit of a *Super Smash Bros. Melee* fan. Someone in my Discord went so far as to call me a "Melee head." It makes sense; there's rarely a day that goes by without me playing a few singles or doubles matches. *Melee* is one of those games where it's not only played for fun; my mind feels sharper, more focused. So, to get a controller that's worth over $275, and dedicated specifically to this game, makes me excited. And honestly, it's kind of refreshing to talk about something that *doesn't* necessarily pertain to Linux or the Steam Deck -- even though I play the game on both platforms.

# History of Competitive GameCube Controllers, and the Solution that was Needed
When it comes to the competitive *Smash* scene, you won't ever see the top players use a controller other than the GameCube controller. When I say GameCube controller, I mean the *original* one manufactured by Nintendo, not some third-party knockoff. Despite the [huge amount of backlash Nintendo receives for their anti-consumer approach](https://www.ign.com/articles/smash-world-tour-players-speak-out-after-tournament-cancellation), their quality is top-notch when it comes to their hardware, at least when it comes to their GC controller. Third-party controllers tend to not have the same quality, and they are more likely to suffer from stick drift sooner (or peeled analog sticks...that's happened to me before).

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/melee/clip.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

But finding an OEM controller can be tough. Not only are they hard to find and expensive, but even if you do manage to get one, these controllers still suffer from wear and tear over time. The potentiometer for the sticks will wear, causing stick drift. Buttons may start to feel mushy rather than click-y. The springs in the triggers may not react the way that you're used to when pressing them down.

The [Goomwave](https://goomwave.com/) was made to address this situation. It's a motherboard that you can replace the vanilla PCB with. It's designed to fix the digital inconsistencies of control sticks, and allow for button re-mapping. While this worked, it was *very* expensive. The PCB itself costs $150, and, according to [Ixis - The Nerd Network](https://www.youtube.com/watch?v=8xsUyqoGXUs), top players had to keep spending "hundreds of dollars" every couple of months on a new PCB just to stay competitive. On top of this the Goomwave had "infamously long ordering lines." Matter of fact, if you go to the "Shop" page on the [official site](https://goomwave.com/shop/), you won't even be able to find anything.

![Goomwave empty shop](/images/phobgcc/empty_shop.png)

# Benefits of PhobGCC
Enter the [PhobGCC](https://linuxgamingcentral.com/posts/phobgcc-2.0.2/). It's an open-source PCB that has the following benefits:
- no potentiometer oddity degradation effect (PODE) -- it doesn't matter what kind of controller you use; the PS5 controller, the Xbox controller, the Switch Pro controller. They all use potentiometers, and what happens with those is that they will eventually wear over time, causing stick drift. Instead of using potentiometers, the PhobGCC uses Hall effect sensors and magnets. Since the sensor and magnet never touch, neither do they wear out. The result is you get a long, *long*-lasting controller that shouldn't ever suffer from stick drift
- no snapback -- if you short hop laser with Falco, for example, you might have noticed he may turn around while in the air, making him shoot in a direction opposite of what you intended. This is because of a small amount of recoil that occurs when flicking the control stick and returning it to its neutral position. This results in snapback, causing your input to be registered in the opposite direction. There's no snapback with the PhobGCC, ensuring that you're always lasering in the direction you intended
- consistent shield-dropping without universal controller fix ([UCF](http://www.20xx.me/ucf.html))
- [customizable](https://github.com/PhobGCC/PhobGCC-doc/blob/main/For_Users/Phob_Calibration_Guide_v0.27.md) stick calibration, button swapping, Z-jump re-mapping, snapback filtering, and rumble strength
- 1.0 cardinals -- based on the little research that I could find, this apparently gives players ["access to the widest array of motion/largest choice of inputs"](https://www.reddit.com/r/SSBM/comments/rqjmz6/discussion_normalization_of_maximum_cardinal/)
- discrete switches can be installed on the D-pad and/or face buttons

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/melee/snapback.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}
*Video credit: [n3zmodgod](https://www.youtube.com/watch?v=O4rigBTxgPM)*

![Smashscope](/images/phobgcc/FreezeSticks.png)
*Image credit: PhobGCC team*

The great thing about the PhobGCC is that because it's open-source, [you can make a controller yourself](https://github.com/PhobGCC/PhobGCC-doc/blob/main/For_Makers/Phob2_Ordering_Guide.md). What's even greater though, since I'm a journalist, is I get the benefit of receiving a review sample that someone else already made. I know, you're jealous.

# Getting the Controller and Getting it to Work on Linux
This controller is brought to you by Kyle, owner of [MayhemMods](https://www.etsy.com/shop/MayhemMods) on Etsy. It's an imported Japanese *Smash Ultimate* controller, and not only does it come with the PhobGCC; it also comes with modifications! Such as:
- cherry MX right trigger -- this allows for easier trigger presses. Makes wavedashing, techrolls, and L-cancelling a snap
- FIRES left trigger -- lubricated trigger with less resistance than OEM trigger, and offers increased stabilization and smoother gliding. Eliminates trigger jams and decreased wear on your finger. Supposedly the lubrication decreases spring noise, but it's still pretty loud in my experience. Not that it's a bad thing though
- paracord sleeved cable -- this allows the cable to be easily replaced without having to solder. Apparently it also reduces tangles

The package arrived in my mailbox precisely three weeks ago. Inside of the sleeve was the *Smash Ultimate* controller box. Even though the controller had already been opened up to be modified, it was in great shape when it came in and protected very well inside the box.

![PhobGCC box front](/images/phobgcc/box/1.jpg)

![PhobGCC box box](/images/phobgcc/box/2.jpg)

I specifically requested that Kyle send me a red paracord cable, and he did not disappoint. I personally think it's a nice color combination with the black shell.

Here's some teardown pics:

{{< gallery-slider dir="/images/phobgcc/teardown/" >}}

You may need to [add a rule to `rules.d`, install wii-u-gc-adapter, and then modprobe uinput](https://seanyeh.com/pages/mayflash_gamecube_adapter_linux_dolphin_steam/) in order to get your GC adapter to work on Linux. That's what I had to do on Fedora. These steps may not be necessary on Arch though.

The PCB is version [1.2.3](https://github.com/PhobGCC/PhobGCC-HW/releases/tag/v1.2.3). The firmware version is [0.27](https://github.com/PhobGCC/PhobGCC-SW/releases/tag/v0.27). It's not the new [2.0.2](https://linuxgamingcentral.com/posts/phobgcc-2.0.2/) board, but the arrival of the gamepad was good timing, as [ranked](https://linuxgamingcentral.com/posts/slippi-ranked-is-here/) just showed up less than two weeks ago. I'll admit I'm not the most competitive player out there, but I can assure you I'll definitely have the upper-hand now with this new controller.

![Battlebeaver pads](/images/phobgcc/battlebeaver_pads.jpg)

When using a Phob controller, you need to press B while *Melee* is running through Dolphin/Ishiiruka to activate the analog sticks. I had been pointed out that the [third-party GC adapter](https://www.amazon.com/gp/product/B08Q381716) that I was using before would not work with this controller, and that was indeed the case. I *could* technically use it by setting the adapter to PC mode and then configuring the buttons through Dolphin, but the best practice is to set the adapter in Wii U/Switch mode and selecting "GameCube Adapter for Wii U" in the controller configuration menu. And in order to do that, I had to order a Mayflash adapter. The nice thing about this is the buttons are automatically configured for you; typically any other gamepad requires manual configuration of the buttons.

# How the Controller Feels
So how has the experience been? **Very good.** Wavedashing with the right trigger is easier thanks to the cherry MX switch. Only a little pressure is needed to press the switch down -- this will definitely help in keeping my fingers from getting tendonitis. L-cancelling is also easier to land, allowing for quicker reactions after landing to the ground. Since the right trigger is digital input only, I still have the benefit of an analog trigger on the left. This is useful for light-shielding, and because the spring is trimmed and lubricated, this also makes finger-pressing not as painful after a while. 

Something that I don't really see anyone talk about is the control stick in regards to how much easier it is to rotate this in a circle when escaping out of a grab than with other gamepads. It's much easier to do that on this controller than it was on my DualSense, in a way that's hard to explain. I think I can also rotate the stick at a faster rate as well. Now it's not that difficult to escape an enemy's grab when my character is at low damage.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/melee/clip2.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

As far as latency is concerned, well, I don't have a high-speed camera to compare input lag on this controller to the DualSense or Xbox Series pad, but from the naked eye, this controller *does* seem to be a lot more responsive. It feels like my input is faster. Which, obviously for a fast-paced game like *Melee*, is essential.

And I mean, talk about the *nicest* modder you'll ever talk to. The face buttons admittedly felt a bit mushy in my opinion. I asked Kyle what I could do about that. He offered to send me [Battlebeaver pads](https://battlebeavercustoms.com/products/battle-beaver-gamecube-contact-pads) which offer more clicky-ness. Not only did he send that over, but he also sent a new triwing screwdriver so I could take the controller apart. (I had one before; it was just a little too small for the screws on the back of the gamepad.) After replacing the button pads, I can confirm the face buttons are more satisfying to press and more clicky!

# Overclocking
It is possible to [overclock the GC adapter](https://linuxgamingcentral.com/posts/overclocking-gc-adapter-guide/) on Linux desktop. By default, the controller polls at a rate of 125 Hz, or every eight milliseconds. You can increase the polling rate to 1,000 Hz, or every millisecond. This reduces input lag to make it more closely resemble console play, while also improving latency stability.

![GC adapter set to 1,000 Hz](/images/controller_overclocking/overclocked.png)

You can technically use the GC adapter with the Steam Deck via a USB-C dock, but you'll be locked to 125 Hz. There are [instructions](https://github.com/hannesmann/gcadapter-oc-kmod/blob/master/STEAMOS.md) for overclocking, but I do NOT recommend following these steps for the time being, as they do not work. Hopefully that guide will get updated at some point.

Oh, and apparently [it's better to connect your controller to port 2 on the Mayflash adapter](https://docs.google.com/document/d/1cQ3pbKZm_yUtcLK9ZIXyPzVbTJkvnfxKIyvuFMwzWe0/edit#heading=h.18skeoosa2vw), but no explaination is given as to why that is.

# PhobGCC - Is It Worth Your Time?
I have to admit, getting a controller as customized and expensive as this, all *for just one single game*, is a little overkill if you're not a competitive player (although I suppose you could also use it with *Nickelodeon All-Star Brawl*, *Slap City*, *Rivals of Aether*, *MultiVersus*, and other *Smash*-like games).

But if you want a controller that's basically going to last you a lifetime, without any wear or tear on the analog sticks, without needing to worry about stick drift over time, no accidental turning around in midair when performing a special move, consistent shield-dropping, customizable calibration, and *super* fast input, I'd say the PhobGCC is a solid choice. What's nice is that this controller in particular also has modified triggers for easier pressing and execution of certain techniques, and a paracord sleeve cable for a nice red touch, reduced tangles, and easy removal.

![PhobGCC](/images/phobgcc/box/3.jpg)

If you want to save yourself a little bit of money, you can [build your own controller](https://github.com/PhobGCC/PhobGCC-doc/blob/main/For_Makers/Phob2_Ordering_Guide.md) rather than getting a pre-built one, but you'll need some soldering skills and a lot of different parts to order.

**TL;DR**

The good:
- open-source PCB
- will last much longer than any controller that uses potentiometers; no stick drift
- no snapback
- consistent shield-drops without UCF
- just about *everything* can be customized, from button mappings to vibration strength to control stick sensitivity
- very, *very* responsive
- modified triggers for easier pressing and less wear on your fingers
- paracord sleeve cable for customized color, and less tangles
- the nicest modder you'll ever have the pleasure of talking to

The not-so-good:
- expensive
- admittedly niche, as it's mostly just for one game and aimed towards competitive players

The controller starts at **$275.** Depending on the mods you want to configure, it may cost extra. Check it out on [Etsy](https://www.etsy.com/listing/1257321101/phob-gamecube-controller-for-smash-bros?show_sold_out_detail=1&ref=nla_listing_details). It's currently out of stock but you can see Kyle's [other mods](https://www.etsy.com/shop/MayhemMods) in the meantime.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
