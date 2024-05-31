+++
title = "GE-Proton7-43 Fixes Garbled Audio with Immortals: Fenyx Rising, Allows Hairworks on The Witcher 3"
date = 2022-12-19T00:09:43-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/ge_proton/7-43.jpg"
tags = ["news", "software update", "ge-proton"]
keywords = ["ge-proton", "proton-ge", "ge-proton7-43", "immortals: fenyx rising", "the witcher 3", "baldur's gate 3", "gears 5", "elder scrolls online", "fall guys", "dxvk", "vkd3d", "wine"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
*Immortals: Fenyx Rising* came to [Steam](https://store.steampowered.com/app/2221920/Immortals_Fenyx_Rising/) a few days ago. However, it has evidently faced quite a few [issues](https://www.gamingonlinux.com/2022/12/immortals-fenyx-rising-now-on-steam-but-quite-messy-on-steam-deck/) for both Steam Desk and Linux desktop users. Namely, the occasional pop-up of the Ubisoft Connect overlay, the keyboard and mouse configuration being applied by default when using a gamepad, garbled audio, and black line flickering on the grass rendering.

Fortunately, GE-Proton is here to once again save the day. Well, at least, *partly*. GE-Proton7-43 should fix "cutscene audio skips" and "garbled output." I haven't tested the game myself, so there's likely the overlay pop-up issues and black line flickering remaining. But it's a step in the right direction to making this game more playable.

*The Witcher 3* -- presumably in reference to the recent DX12 upgrade -- no longer crashes with hairworks enabled. So in theory all you would need to disable on NVIDIA is the AO.

For other game-specific fixes, the launcher for *Baldur's Gate 3* is skipped, and the game uses Vulkan by default. A fix was added for *Gears 5* in regards to the hang after pressing the Enter key on the logo screen. The game drive option for *Elder Scrolls Online* should now properly be applied. This fixes the installation, but keep in mind you'll still need to press the Space key on the black window. The Protonfix for *Fall Guys* was updated -- it no longer needs the .exe workaround.

Besides this, the usual set of software tools got updated to the latest git or bleeding edge. This would include DXVK, VKD3D, and Wine. Upstream Proton changes have also been imported.

See the patch notes and download the release on [GitHub](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-43).

*Cover image credit: Ubisoft*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
