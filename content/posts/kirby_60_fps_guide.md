+++
title = "Kirby and the Forgotten Land: Emulation Tips (60 FPS, dynamic resolution disabled, 4K/ultrawide support!)"
date = 2022-03-27T14:32:47-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/kirby_guide/cover.jpg"
tags = ["guide", "emulation"]
keywords = ["yuzu", "ryujinx", "emulation", "kirby", "nintendo switch"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
It's been said plenty enough: the Nintendo Switch is in dire need of a hardware upgrade. That's for sure. Fortunately, passionate programmers and modders out there have made playing Nintendo Switch games via emulation a much better experience. In the case with *Kirby and the Forgotten Land*, the framerate is capped to 30 FPS. In a modern day and age where we're used to ultra-fast speeds of 60, 144, or even higher framerates, that 30 FPS cap can be headache-inducing. The Switch also suffers from a maximum resolution of 1080p while docked -- monitors and TVs with a higher resolution will make the image look bad.

Ryujinx and Yuzu are examples of emulators that solve both problems. The image quality looks insanely good on 1440p/4K monitors thanks to upscaling support, and modders are able to add in 60 FPS patches for games that would otherwise play at 30 FPS. No longer do you have to suffer headaches with 30 FPS...as long as you've got the hardware.

Note that you may want to download this guide for offline use in the event the DCMA-hungry lords at Nintendo take this article down (I would be honored if they actually noticed).

{{< youtube "P3AIqJMoFbk" >}}

In the coming weeks I'm hoping to have a Switch emulation guide here on LGC, but in the meantime, you can refer to the guide on [Boiling Steam](https://boilingsteam.com/emulating-nintendo-switch-games-on-linux-2/) if you're new to Switch emulation and want to get started. Normally I would recommend Ryujinx, but for Kirby's case, I find that Yuzu handles the 60 FPS mod a lot better. The downside to Yuzu, however, is that it isn't quite as stable as Ryujinx (you might have noticed the crash at the end of the video above).

For hardware, I can't really give any specifics here. I would say have **at least 16 GB of RAM and a graphics hard with 4 GB of VRAM or more**. Even with my GTX Super 1660 there are busy areas that my computer can't quite handle well and the framerate can be as choppy as 10 FPS. Most other areas though can safely reach 60 FPS after the shaders have been cached.

Head over to the [Yuzu mods](https://github.com/yuzu-emu/yuzu/wiki/Switch-Mods#kirby-and-the-forgotten-land) and download whatever mods you want for the game. Mods include 32:9/21:9 aspect ratio support, [dynamic resolution](https://www.howtogeek.com/764408/what-is-dynamic-resolution-scaling-drs/) disabled, and 60 FPS support. There's a "full" 30 FPS mod that allows NPCs in the distance to render at 30 FPS (normally they're only 15 FPS). For 60 FPS options, there's a 60 FPS mod that still renders distant NPCs at a lower framerate, and a "full" 60 FPS mod that renders *everything* at 60 FPS, including objects from a far distance. I find that the regular 60 FPS mod plays a bit better on my hardware, but if you've got a *really* beefy rig, you could probably go all out with the "full" 60 FPS mod.

Once you have your copy of Kirby dumped and Yuzu is open, right-click the game and select "Open Mod Data Location".

![yuzu context menu](/images/kirby_guide/yuzu_context_menu.jpg)

Sometimes your file manager won't open. In this case you can navigate to `~/.local/share/yuzu/load/01004D300C5AE000/` (note: this folder may be different in your case; you can find where your mod folder location is by going to *Emulation -> Configure -> System -> Filesystem*). Simply extract your downloaded mods to this folder and you're done. If you want to enable or disable specific mods, just right-click the game in Yuzu, select "Properties," and check or uncheck the mods under the "Add-Ons" tab.

![yuzu mod checklist](/images/kirby_guide/mod_checklist.jpg)

Play the game and see how it fares on your hardware. There's going to be a lot of initial stutters; those are the shaders getting cached. After that the game should run relatively smoothly. You may want to use [GameMode](https://github.com/FeralInteractive/gamemode). You can also use the FSR filter in Yuzu and set the resolution lower than your monitor's native resolution. You can tinker around with other filters as well to see what works best with your setup. You're probably also going to want to set Vulkan as the graphics backend, especially if you're using AMD/Steam Deck (FSR only works on Vulkan anyway).

Be warned that **the game may randomly crash**, so if you're in the middle of a stage, you'll have no choice but to play through it again.

![yuzu kirby](/images/kirby_guide/in-game.jpg)

If you want to use the 60 FPS/ultrawide mod for Ryujinx, you can do so (check the pinned messages in the `#modding-cheats` channel on the [Ryujinx Discord](https://discord.gg/VkQYXAZ)), but on my rig I only got about 40 FPS max.

So here's the **TL;DR**:
1. If you're new to Switch emulation, follow [this guide](https://boilingsteam.com/emulating-nintendo-switch-games-on-linux-2/) to get yourself set up
2. Downloads the mods [here](https://github.com/yuzu-emu/yuzu/wiki/Switch-Mods#kirby-and-the-forgotten-land)
3. Extract the mods to your mod data location (by default it should be `~/.local/share/yuzu/load/01004D300C5AE000/`)
4. Run the game, tinker around with some graphical settings to get the best experience (may also want to use [GameMode](https://github.com/FeralInteractive/gamemode))
5. Be prepared for occasional crashing

There isn't just 60 FPS patches for *Kirby and the Forgotten Land*; there's plenty of other Switch games that also have 60 FPS mods. Check the [Yuzu mods](https://github.com/yuzu-emu/yuzu/wiki/Switch-Mods) page on GitHub and see if the game you want to emulate has it.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
