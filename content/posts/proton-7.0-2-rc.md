+++
title = "Proton 7.0-2 Available As a Release Candidate"
date = 2022-04-08T13:48:57-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = ""
tags = ["proton update", "news"]
keywords = ["proton"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
A few days ago, Valve released [Proton 7.0-2rc](https://github.com/ValveSoftware/Proton/issues/5749). This new release brings quite a few new playable games, including *One Piece: Pirate Warriors 4*, *Metal Slug 2* and *3*, *Dragon Quest Builders 2*, *Guilty Gear Isuka*, *King of Fighters XIII*, and a few others. There's also a *ton* of bug fixes, ranging from Unity games crashing when certain peripherals were connected to the computer, certain games getting better Steam Deck compatibility, multiplayer in *UNO*, video playback, crashes, audio missing in cutscenes, launcher fixes, and a whole lot more. 

Finally, the usual set of upgrades have happened with `dxvk`, `vkd3d-proton`, and `dxvk-nvapi`. `dxvk` was upgraded to [1.10.1](https://github.com/doitsujin/dxvk/releases/tag/v1.10.1), `vkd3d-proton` was upgraded to [2.6](https://github.com/HansKristian-Work/vkd3d-proton/releases/tag/v2.6), and `dxvk-nvapi` was upgraded to [0.5.3](https://github.com/jp7677/dxvk-nvapi/releases/tag/v0.5.3).

Keep in mind that, as the GitHub post mentions, the changelog is "tentative," has not been verified by the QA team, and can change before the stable release.

See the full patch notes on [GitHub](https://github.com/ValveSoftware/Proton/issues/5749). On that issue you can also let the Proton development team know of any problems that you come across with this new release candidate.

If you want to give this new version of Proton a shot ahead of it's official release, you can right-click Proton 7.0 in your Steam library (make sure "TOOLS" is checked in the dropdown menu from the top-left), click "Properties..." and under the *Betas* tab, select `proton-7.0-2-rc` from the dropdown menu. Any game that uses Proton 7.0 will now use this new RC after it updates.

![selecting proton-7.0-2-rc from steam](/images/proton_rc/upgrading_to_proton_rc.jpg)

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
