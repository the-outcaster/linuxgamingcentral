+++
title = "Sackboy: A Big Adventure to Optimization (Unlock DLSS for Non-RTX GPUs, Skip Intro Videos, Use Steam Network Services Instead of Epic Online Services)"
date = 2022-12-07T12:09:43-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/weekly_news/oct_22-28.jpg"
tags = ["guide", "sackboy"]
keywords = ["sackboy: a big adventure", "steam deck", "nvidia", "nvidia rtx", "dlss", "fsr 2.1", "epic online services"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
[*Sackboy: A Big Adventure*](https://store.steampowered.com/app/1599660/Sackboy_A_Big_Adventure/) is a great game. But unfortunately it's barred by a few annoyances, such as having to deal with the Epic Games login prompt when launching the game, even if you don't plan on using online multiplayer, and having to see the intro video every time the game is launched. We can save ourselves some time by fixing both of these. Also, your Deck, or your desktop that *doesn't* have a RTX GPU, can make use of FSR 2.1 in replacement of the game's built-in DLSS feature, providing a ~10% performance boost and having a sharper image quality over FSR 1.0. Let's get right to it!

# Skip Intro Videos
Super easy fix. Go to your game's installation directory (right-click the game in Steam -> Manage -> Browse local files). 

![Sackboy browse local files](/images/sackboy/optimization_guide/browse_local_files.png)

In your file manager, go to `GingerBread/Content/Movies/IntroSequence/`. Delete everything in there. Now you can save yourself some time when launching the game and go right to the title screen, while also saving 200+ MB of space. Alternatively, you can rename the files if you wish to keep them, but that will be a time-consuming process, since there's quite a few video files there. If you want to bring the video files back after deletion, you can verify the game files and they will be re-downloaded.

# Skip EOS Login Screen and Use Steam Network Services Instead
Download the mod from [GameBanana](https://gamebanana.com/mods/409300). Extract the pak file to `GingerBread/Content/Paks/`. That's literally it. You should no longer be asked to log into your Epic Games account upon launch. Furthermore, you can still play online multiplayer with this mod via Steam network services. A caveat that you have to keep in mind, however, is **you won't be able to play with others who own the game on the Epic Games Store.**

I tested an online multiplayer session with a friend and I can confirm I don't need to use EOS to play with him.

![Sackboy online multiplayer without EOS](/images/sackboy/optimization_guide/online_multiplayer.jpg)

# Use FSR 2.1 for a Performance Boost
We can use the [*CyberPunk 2077* DLSS unlocker mod](https://www.nexusmods.com/cyberpunk2077/mods/3001) and use it with *Sackboy*. Keep in mind you'll need to register for an account with Nexus Mods if you haven't already and be logged in to download the mod.

After downloading the mod extract `nvngx.dll` and `nvngx.ini` from `bin/x64/` to `GingerBread/Binaries/Win64/`. Next, install [Protontricks](https://github.com/Matoking/protontricks) ([Flatpak](https://flathub.org/apps/details/com.github.Matoking.protontricks) is available for Steam Deck users), run it, choose *Sackboy*, select the default wineprefix, and run regedit to import `EnableSignatureOverride.reg` from the mod you had extracted. No need to add `WINEDLLOVERRIDES="winmm.dll=n,b" %command%` for this.

![Enabling signature override](/images/sackboy/optimization_guide/import_reg_file.png)

You can check my [guide](https://linuxgamingcentral.com/posts/dlss-unlocker-for-various-games/) if you need a step-by-step process on how to do this.

Here's *Sackboy* without the DLSS unlocker:

![Sackboy without FSR 2.1](/images/sackboy/optimization_guide/without_fsr.jpg)

And here the game is with it on:

![Sackboy with FSR 2.1](/images/sackboy/optimization_guide/with_fsr.jpg)

On my desktop I'm seeing a ~10% performance boost.

You have to be careful what version of Proton you use. Proton Experimental and GE-Proton crashed the game when lowering the resolution while in fullscreen. The only version that worked for me was the stable [7.0-5](https://linuxgamingcentral.com/posts/proton-7.0-5/) release.

That's all, for now. As a side note, I'm really enjoying the game, so stay tuned for a review.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
