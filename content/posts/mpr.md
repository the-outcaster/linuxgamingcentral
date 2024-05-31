+++
title = "Play Metroid Prime in Stunning HD with MPR (With Wine, for Now)"
date = 2022-04-13T14:27:44-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/mpr/cover.jpg"
tags = ["emulation", "metroid", "wine"]
keywords = ["emulation", "dolphin emulator", "metroid prime", "remake", "wine"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
I now have renewed interest in playing the original *Metroid Prime* for the GameCube. Why's that? Because there's this GORGEOUS HD mod that has finally been released after  *four* years in the making.

Just look at the screenshots yourself. The game still looks great nearly 20 years later, but now it got a fan-made upgrade in the visual department that makes it look like the game came out not even five years ago.

![MPR vs. space pirate](/images/mpr/2.jpg)

The project is called MPR (which, I assume, stands for "Metroid Prime Remastered"). It uses a modified version of [Ishiiruka Dolphin](https://forums.dolphin-emu.org/Thread-unofficial-ishiiruka-dolphin-custom-version) and also makes use of [PrimeHack](https://github.com/shiiion/dolphin). Meaning you can play the game with keyboard and mouse controls, in addition to gamepads, as well as adjust the field of view (FOV). MPR also allows you to customize the in-game HUD, from color to reticle to opacity to how simple or cluttered it is.

Note that for the time being, **you'll need to run MPR with Wine**, as it is currently not possible to build this fork of Dolphin/Ishiiruka on Linux. One of the developers told me in the [MPR Discord](https://discord.com/invite/qG6pgza) that "Linux is broken on Ishiiruka. I tried on Arch. Wxwidgets itself was failing to compile, it needs updating, and that's not a small task. It's the entire UI framework Ishiiruka is built around." But he did mention later on he "would like" to add Linux support in the future.

![MPR after scan cutscene](/images/mpr/3.jpg)

I found that I have the best experience creating a bottle with the [Bottles](https://usebottles.com/) application and leaving the default settings as is, particularly making sure **DXVK is enabled** (MPR uses Direct3D11 by default). There's going to be a lot of stutters (presumably shaders caching) but after that it's a decent experience. Some other things you may want to do, as brought out by the [Phaze 1 release video](https://youtu.be/L40JyicJoqI):
- enable bloom under the *Graphics -> PrimeHack GFX* tab for better visual quality, at the expense of more demanding performance
- Store EFB copies to Texture Only under the *Graphics -> Hacks* tab to ensure better performance (should already be checked by default)
- adjust the IshiirukaFX under the *Graphics -> Post-Processing* tab if you want the game to run better or worse depending on the effects you choose
- ensure Tessellation and Forced Lighting is enabled under the *Graphics -> Enhancements* tab (the second one)
- adjust the internal resolution to what you like under the *Graphics -> Enhancements* tab (the first one), if your rig can handle it

![MPR vs. parasite queen](/images/mpr/1.jpg)

The video didn't mention it but I also like to force 16:9 aspect ratio and use fullscreen by default in the *Graphics -> General* tab. That way I don't get the black bars on the sides of the screen.

You can either use version 1.00 of the *Metroid Prime* GC ISO, or any version of *Metroid Prime Trilogy*.

Get the initial release (Phaze 1) on [GitHub](https://github.com/AetherPrimus/MPR/releases). Note that you may want to **delete your existing Dolphin settings or create a portable text file in your install directory**; I found that without doing this, MPR wouldn't get the visual upgrade. So this step is important. Also note that the only remastered part of the game at the moment is the initial Frigate Orpheon stage. You can still play past that stage though and still enjoy Samus' remastered suit, dynamic and baked lights, and the adjustable HUD.

Very exciting! I can't wait for the next release.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
