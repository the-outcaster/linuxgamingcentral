+++
title = "Ryujinx Now on Flathub"
date = 2022-03-14T22:23:35-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "https://cdn.discordapp.com/attachments/410222607581839365/953096709712543764/unknown.png"
tags = ["ryujinx", "switch emulator"]
keywords = ["flatpak", "ryujinx"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
As the Steam Deck has seemed to launch a new foray of Flatpak-based applications, Ryujinx is the latest to join to crusade. The request was made on the project's [GitHub issue tracker](https://github.com/Ryujinx/Ryujinx/issues/1077) two years ago. Now it's finally available on [Flathub](https://flathub.org/apps/details/org.ryujinx.Ryujinx).

The announcement was posted just a few hours ago on their [Discord channel](https://discord.gg/VkQYXAZ). You can install Ryujinx on the Steam Deck now with the Discover app. Apparently there's at least 91 of you who have a Steam Deck and are part of the Ryujinx Discord, so go ahead and give it a shot! Just be careful if you're going to record: [the Big N may take it down](https://www.thegamer.com/nintendo-blocking-steam-deck-emulation-videos/).

On desktop you can install it with:

`flatpak install flathub org.ryujinx.Ryujinx`

Then run it with:

`flatpak run org.ryujinx.Ryujinx`

Note that, even if you already had your system firmware installed and had customized settings from a previous version of Ryujinx, you'll need to do this over again with the Flatpak version. You'll need to re-configure your controls, re-install game updates, re-import game saves, etc. You'll also need to re-initialize your product keys by putting them in `~/.switch/`. Configuration files will be found in `~/.var/app/org.ryujinx.Ryujinx/config/Ryujinx/`.

Flatpak version is running just fine on my desktop:

![hyrule warriors ryujinx flatpak](/images/ryujinx_flatpak/hw_aoc.jpg)

![kirby ryujinx flatpak](/images/ryujinx_flatpak/kirby.jpg)

Unfortunately [Vulkan](https://linuxgamingcentral.com/posts/ryujinx_feb_2022_recap/) isn't quite here yet; Vulkan will make a *huge* improvement for the Steam Deck in particular because of the AMD hardware inside. So we're going to have to deal with lots of shader compilation delays for now. But it's great to see Flatpak support!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
