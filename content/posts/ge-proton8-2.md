+++
title = "GE-Proton8-2 Fixes Monster Hunter Rise, Shatterline, Conception Plus"
date = 2023-05-06T05:18:22Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/ge_proton/8-2.jpg"
tags = ["news", "software update", "ge-proton"]
keywords = ["proton", "ge-proton", "steam play", "dxvk", "vkd3d", "wine", "valve", "codeweavers", "gloriouseggroll", "proton-ge", "ge-proton8-2", "steam snap", "monster hunter rise", "shatterline", "conception plus"]
description = "Plus: if you're using the Steam Snap, installation instructions have been provided."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
GE-Proton8-2 mostly focuses on bug fixes and getting games to work again. Of course, in addition to this, the usual set of software tools -- Wine, DXVK, VKD3D-Proton, DXVK-NVAPI -- have been updated to the "latest git" or "bleeding edge".

*Monster Hunter: Rise* should no longer have any flickering issues, *Shatterline* now works again, a Protonfix was added for *Conception PLUS*, and a couple of other minor behind-the-scenes changes have made it in.

Interestingly enough the README for GE-Proton has been updated with instructions for adding said compatibility tool for the Snap version of Steam. Unsurprisingly, though, it's not officially supported by the developer:
> This unofficial build isn't supported by GloriousEggroll nor Valve and wasn't tested with all possible games and cases. It can behave differently from upstream builds. Use at your own risk.

But installation is pretty much the same as installing it via Flatpak or a native package; just download the latest GE-Proton release and extract it to `~/snap/steam/common/.steam/steam/compatibilitytools.d/`.

See the patch notes on [GitHub](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton8-2).

*Cover image credit: Capcom*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
