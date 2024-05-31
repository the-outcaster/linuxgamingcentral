+++
title = "GE-Proton7-12 Out Now, Enables GameMode By Default"
date = 2022-04-04T00:41:09-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/ge_proton/cover.webp"
tags = ["software update", "ge proton"]
keywords = ["ge proton", "new world", "gamemode"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
GE-Proton7-11 was [released](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-11) yesterday. This now automatically enables [GameMode](https://github.com/FeralInteractive/gamemode) for any game run through this version. A user no longer needs to add `gamemoderun %command%` to their Steam launch options.

The release also comes with the usual updates to [`dxvk`](https://github.com/doitsujin/dxvk), [`vkd3d-proton`](https://github.com/HansKristian-Work/vkd3d-proton), and [`dxvk-nvapi`](https://github.com/jp7677/dxvk-nvapi); they're using the latest commits. Proton Experimental (bleeding edge wine build) has also been updated. Build-specific updates have been added from upstream Proton. Not too long after the release, a [hotfix](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-12) was added that allows *New World* to be run, since the EAC .so library was apparently added.

Check out [LGC's guide on installing GE-Proton (formerly Proton GE)](https://linuxgamingcentral.com/posts/proton_ge_tutorial/) if you want to find an easy way to update your version of GE Proton. If you want to use GE's custom version of Wine, you can use the recently released [Wine-GE-Proton7-8](https://github.com/GloriousEggroll/wine-ge-custom/releases/tag/GE-Proton7-8).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
