+++
title = "GE-Proton8-5 Removes Gears 5 Workaround, Fixes Two Games"
date = 2023-07-02T16:36:26Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/ge_proton/8-5.jpg"
tags = ["news", "software update", "ge-proton"]
keywords = ["proton", "ge-proton", "steam play", "dxvk", "vkd3d", "wine", "valve", "codeweavers", "gloriouseggroll", "proton-ge", "ge-proton8-5", "gears 5", "two worlds", "apb reloaded"]
description = "Looks like a few open-source speech-recognition toolkits have also been imported."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
*Gears 5* no longer needs any workarounds with today's update to GE-Proton. It works with EAC. However, if you previously played the game with a different version of GE-Proton, you'll need to remove a couple of EAC-related folders inside the game's install directory, then verify the integrity of the game files to play it again.

Protonfixes have been added for two games: *Two Worlds*, and *APB Reloaded*. As usual, DXVK, VKD3D-Proton, and Wine have been updated. Wine staging patches have been rebased, steam_helper updates have been imported from upstream, and modules from [kaldi](https://www.kaldi-asr.org/doc/about.html), [OpenFst](https://www.openfst.org/twiki/bin/view/FST/WebHome), and [Vosk-API](https://github.com/alphacep/vosk-api) have been imported from upstream.

See the patch notes on [GitHub](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton8-5).

*Cover image credit: The Coalition/Xbox Game Studios*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
