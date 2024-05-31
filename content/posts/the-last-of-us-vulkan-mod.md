+++
title = "The Last of Us Mod Fixes Stuttering and Improves Performance"
date = 2023-04-05T14:52:58Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/ge_proton/7-54.jpg"
tags = ["news", "the last of us", "modding"]
keywords = ["the last of us", "the last of us performance fix", "the last of us vulkan mod"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
I know I'm recycling that meme-y "The last of my VRAM" image a little too much, but there's potentially some hope for those of you looking to get better performance, even though the past couple of updates to the game [haven't done much](https://www.youtube.com/watch?v=HgW3neI_3sk).

On my [Discord](https://discord.gg/bTgCcWC4dm) I've been made aware of a [mod](https://www.nexusmods.com/thelastofuspart1/mods/21?tab=description) for *The Last of Us*. The description of the mod is as follows:
> Run the game in Vulkan using DXVK -- helps with crashes, performance, and stuttering.

Now, of course, I have to add the caveat that **I have not personally tested this mod**, as I don't own the game, so I can't confirm whether the mod does indeed improve performance. I've been told that in some tests, "it lowers RAM consumption by a lot and reduces/removes stutter while having a 10-30% performance decrease." (I think they meant "*increase*" rather than "decrease.")

To use the mod, download the version appropriate to your GPU vendor, and extract the zip file contents to the game's installation folder. Obviously, Deck users are going to want to download the AMD version. If you want to enable HDR, open the `dxvk.conf` file and change the `dxgi.enableHDR` parameter from `false` to `true`.

There's a few warnings that the modder describes:
1. The game will rebuild shaders and it will crash many times while doing this, will also **lose DLSS [and] use FSR instead.**
2. **Listen Mode doesn't work when using Vulkan**; maybe degraded performance for some users.
3. **Seems to not work with all AMD GPUs**, NVIDIA seems fine for RTX 20-series and above.

Get the mod over on [Nexus Mods](https://www.nexusmods.com/thelastofuspart1/mods/21?tab=description). Note that you will need to have a Nexus account and be signed in to download.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
