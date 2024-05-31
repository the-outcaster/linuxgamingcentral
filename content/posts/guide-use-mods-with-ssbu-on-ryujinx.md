+++
title = "How to Use Smash Ultimate Mods with Ryujinx"
date = 2022-05-05T11:12:06-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/guides/ryujinx_arcropolis/cover.jpg"
tags = ["guide", "smash bros", "ryujinx", "emulation"]
keywords = ["smash bros", "ryujinx", "emulation", "linux"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
As of Ryujinx version 1.1.112, users can now seamlessly [load mods on *Super Smash Bros. Ultimate*](https://linuxgamingcentral.com/posts/news-arcropolis-added-to-ryujinx/) with the use of ARCropolis/Skyline. Here's how to do it.

*Note: this tutorial is based off of the guide from [GameBanana](https://gamebanana.com/tuts/14311), but specifically tailored to Linux users.*

**TL:DR**

1. Get yourself set up with emulating Switch games on Linux with this [guide](https://boilingsteam.com/emulating-nintendo-switch-games-on-linux-2/) if you haven't already
2. Download [Ryujinx](https://ryujinx.org/downloads) and run it for the first time
3. Download [ARCropolis](https://github.com/Raytwo/ARCropolis/releases/), extract zip to `%RYU_DIR%/sdcard/`
4. Download [Skyline](https://github.com/skyline-dev/skyline/releases), extract to `%RYU_DIR%/sdcard/atmosphere/contents/01006A800016E000/`
5. Download any mod (plenty of them over on [GameBanana](https://gamebanana.com/games/6498)), extract them to `%RYU_DIR%/sdcard/ultimate/mods/`
6. Launch the game. It should pick up the mods

Head over to the [guide](https://boilingsteam.com/emulating-nintendo-switch-games-on-linux-2/) on Boiling Steam to get yourself up and running with emulating Nintendo Switch games on Linux if you don't already have that set up. You'll need the launch editon Switch, as well as a legal copy of *Smash Ultimate*. (I'm still planning on writing a guide here, but I'm waiting for my Steam Deck to arrive before I do that.)

You're going to want to download Ryujinx if you haven't already. You can download a portable build directly from [Ryujinx's website](https://ryujinx.org/download). You can also get it from the [AUR](https://aur.archlinux.org/packages/ryujinx-git) if you're on Arch, use the [Pine-jinx](https://github.com/edisionnano/Pine-jinx) script installer, or install the Flatpak version from [Flathub](https://flathub.org/apps/details/org.ryujinx.Ryujinx) if you're on the Steam Deck. Just keep in mind the file structure will be a little different if you're using the Flatpak. For this guide, I'll be using the portable build.

If you're using AMD or Intel hardware you might want to go with the WIP [Vulkan build](https://github.com/Ryujinx/Ryujinx/pull/2518#issuecomment-890255424) instead of the vanilla build (the Vulkan build has been updated to add support for ARCropolis/Skyline).

If you've never launched Ryujinx before on your machine, run it once so our folders can get set up (you'll also need your `prod.keys` file in `%RYU_DIR%/system`, and have your Switch system firmware installed. That's all covered in the guide on Boiling Steam). There should be a `Ryujinx` folder inside your `.config` directory. So your file structure would look like this:

`~/.config/Ryujinx/` (AKA `%RYU_DIR%`)

Next, download the latest zip files of [ARCropolis](https://github.com/Raytwo/ARCropolis/releases/) and [Skyline](https://github.com/skyline-dev/skyline/releases). These plugins are necessary in order to load mods on *Smash*. Extract the contents of `release.zip` to `%RYU_DIR%/sdcard/`. Extract `skyline.zip` to `%RYU_DIR%/sdcard/atmosphere/contents/01006A800016E000/`.

Inside of `sdcard/` should be an `ultimate` folder. Inside `ultimate`, create a new directory called `mods`. Now you can download whatever mod you want and extract its contents to this folder. There's *tons* of mods over on [GameBanana](https://gamebanana.com/games/6498), from character skins to custom voices to custom menus and a whole lot more. So let's say I wanted to give Ike a red and black recolor. I would download [said mod](https://gamebanana.com/mods/338940) and extract the zip file to `sdcard/ultimate/mods/`. In the end my mod structure would look like:

`%RYU_DIR%/sdcard/ultimate/mods/Black and Red Ike V2`

Nothing else is required to load the mod. Simply launch the game with Ryujinx and the mod should now show up:

![ike ssbu recolor](/images/guides/ryujinx_arcropolis/ike_color_mod.jpg)

But keep in mind the game has over 10k shaders to load, so you're probably going to want to sit back, enjoy a cup of coffee, or go for a bike ride, because loading the game for the first time is going to take a while.

If you're looking for a more competitive version of *Smash Ultimate*, I highly recommend trying out [HewDraw Remix](https://github.com/HDR-Development/HDR-Releases/releases). It's basically *Brawl's* Project M for *Ultimate*. Download the `ryujinx-package.zip` from the releases page, then extract the zip directly into the `%RYU_DIR%`. Overwrite files if necessary. You can still use custom textures and sound effects with this if you like.

If you're using the Flatpak version of Ryujinx, simply replace `%RYU_DIR%` with `~/.var/app/org.ryujinx.Ryujinx/config/Ryujinx`. Product keys go in `~/.switch`.

That's it! This will make loading and testing mods much more convenient.

Interested seeing this in action? Check the video out on [YouTube](https://youtu.be/WXLeKT9DsKs).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
