+++
title = "Steam Finally Respects Your Global Scaling Factor"
date = 2023-05-06T06:41:31Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam/global_scaling.webp"
tags = ["news", "software update", "steam", "beta"]
keywords = ["steam beta", "kde global scaling", "gnome global scaling", "org.gnome.desktop.interface/text-scaling-factor"]
description = "4K users will especially benefit."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
With the latest beta update to the Steam client, you no longer have to squint your eyes while looking at your game library on larger displays. Steam will now honor GNOME, KDE, and any other desktop environment that uses org.gnome.desktop.interface/text-scaling-factor for display scaling. If you adjust the global scaling factor for your display, all of the UI elements in Steam will also be adjusted.

This was a problem [since 2018](https://github.com/ValveSoftware/steam-for-linux/issues/5460), and now Valve has finally addressed this with yesterday's beta client update. GDK_SCALE has also been re-introduced "as a fallback mechanism to compute the window scaling factor." You can override the window scaling factor via the command line with `-forcedesktopscaling <float>`.

A few other fixes made it with yesterday's beta update as well; see the patch notes on [Steam](https://steamcommunity.com/groups/SteamClientBeta/announcements/detail/3705943193607193986).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
