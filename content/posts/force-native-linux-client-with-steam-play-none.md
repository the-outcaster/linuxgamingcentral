+++
title = "Force Native Linux Clients with Steam Play None"
date = 2022-12-29T16:54:05Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/protonup-qt/2.7.7/cover.png"
tags = ["guide", "protonup-qt", "steam play none", "native"]
keywords = ["steam-play-none", "steam play none", "native linux client", "native linux game", "steam deck", "protonup-qt", "crosscode", "flashout 3", "unity engine", "steam play", "proton"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Though this is rare, there *might* be a game or two in your Steam library which -- even though it may have a native Linux version -- will force the use of Proton when you run it. For instance, when running [*CrossCode*](https://store.steampowered.com/app/368340/CrossCode/), your Steam Deck (or Linux desktop) will prefer Proton over the native version, because Steam apparently thinks Proton is better.

Maybe you don't want to use Proton and play the game as is, *natively*. While you can technically use the Steam Linux Runtime to use the native client (if it's available), there may be issues with using that. So we've got another tool at our disposal: [Steam Play None](https://github.com/Scrumplex/Steam-Play-None). This ensures you're playing the native Linux version *as is*.

Getting it is simple. Just make sure you're running ProtonUp-Qt [2.7.7](https://linuxgamingcentral.com/posts/protonup-qt-2.7.7/) or later, run the application, and check off "Enable advanced mode" from the About menu. From there click "Add version" from the main menu, and select "Steam-Play-None" as the compatibility tool from the dropdown menu. Click "Install" and let the application do its thing.

![Downloading Steam-Play-None with ProtonUp-Qt](/images/protonup-qt/2.7.7/steam-play-none.png)

Alternatively you can install it the old-fashioned way by downloading the tarball and extracting it to the `compatibilitytools.d/` directory:

```
wget https://github.com/Scrumplex/Steam-Play-None/archive/refs/heads/main.tar.gz
tar -xzf main.tar.gz -C ~/.steam/steam/compatibilitytools.d/
```

Restart the Steam client if it's already open. Right-click the game you want to force the native client with, go to "Properties...", go to the "Compatibility" tab, check off the box to force a specific tool, and select "Steam-Play-None" from the dropdown menu.

![Forcing Steam-Play-None on Ex-Zodiac](/images/guides/steam-play-none/forcing_spn.png)

That's literally all you have to do. Now you can enjoy your game natively (provided that there is a Linux client available, obviously).

Note that most of the games I've tested, including [*Them's Fightin' Herds*](https://store.steampowered.com/app/574980/Thems_Fightin_Herds/) and [*Ex-Zodiac*](https://store.steampowered.com/app/1249480/ExZodiac/), are already using the Linux client as is. So it's very unlikely that you will have a game that forces Proton. Additionally -- not that I'm favoring Proton over native -- but Unity Linux exports *suck*, hard. Depending on the version of the engine used, Linux versions of games made with Unity aren't going to run anywhere near as fast as using Proton. [*Flashout 3*](https://linuxgamingcentral.com/posts/flashout-3-review/) is an example where the Proton version runs about 1.5x faster.

Before anyone points out to me, "Well, there's actually this Unity game that runs the same as Proton or even better..." I acknowledge that *may* be the case. Unity might have gotten better over the years with their Linux export plugins, which is why I mentioned it depends on the version of the engine the developer used when they exported the game.

At any rate, you now have an option of using native over Proton.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
