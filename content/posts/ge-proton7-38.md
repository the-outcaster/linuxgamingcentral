+++
title = "GE-Proton7-38 Adds Fix for UNCHARTED: The Lost Legacy, Overwatch 2 Shader Compilation Patch"
date = 2022-10-24T22:05:57-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/persona_5_strikers/cover.avif"
tags = ["news", "software update", "ge-proton"]
keywords = ["proton", "ge-proton", "uncharted", "persona", "overwatch", "overwatch 2", "nvapi", "dlss", "dxvk", "vkd3d", "wine"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Today's update to GE-Proton adds a Protonfix for [*UNCHARTED: Legacy of Thieves Collection*](https://store.steampowered.com/app/1659420/UNCHARTED_Legacy_of_Thieves_Collection/) on systems that have more than 16 CPU cores. *The Lost Legacy* game in this collection has also received a `tll.exe amd_ags_x64` override to allow the game to run. A save file fix was added for [*Persona 5 Strikers*](https://store.steampowered.com/app/1382330/Persona_5_Strikers/), and a shader compilation patch was added for *Overwatch 2* (although apparently it's for other games; *Overwatch 2* isn't available on Steam and the use of GE-Proton outside of said client is not recommended).

The list of NVAPI/DLSS-enabled titles has been [updated](https://github.com/GloriousEggroll/proton-ge-custom/blob/df646c0db71a0548b1a8dd501dbd9821cde8ab88/proton#L1232). DXVK and VKD3D have been updated to the latest git (I assume the latter is in reference to vkd3d-proton, not the vanilla vkd3d that Wine uses), Wine has been updated to the latest bleeding edge, and Wine-Staging has been rebased. Finally, the Protonfix for [*Shatterline*](https://store.steampowered.com/app/2087030/Shatterline/) has been removed, as it is no longer needed.

See the patch notes on [GitHub](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-38). As always, you can make use of LGC's [guide](https://linuxgamingcentral.com/posts/proton_ge_tutorial/) for easily obtaining the latest version of GE-Proton on your system.

*Cover image credit: ATLUS*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
