+++
title = "GE-Proton7-24 Released, Adds Ultrawide Support with FSR"
date = 2022-06-30T09:34:37-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/ge_proton/ultrawide.jpg"
tags = ["news", "software update", "ge proton"]
keywords = ["ge proton", "proton", "wine", "glorious eggroll"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
GloriousEggroll seems to be on a...*glorious* streak with plenty of updates coming to GE-Proton in just a matter of days. Since GE-Proton7-22 (or 7-21?) we've been able to get [*Halo Infinite* multiplayer to run out-of-the-box on NVIDIA](https://linuxgamingcentral.com/posts/halo-infinite-now-runs-with-ge-proton/), and it will work on AMD with GE's [Mesa patch](https://copr-dist-git.fedorainfracloud.org/cgit/gloriouseggroll/mesa-aco/mesa.git/tree/dgc_testing.patch?h=f36&id=f51580996713f185ea8edfba9a294ce643fce5c2). GE-Proton7-23 came a day later to make games easier to work with FSR. And yesterday we got yet another update that fixes the *Death Stranding* crash and adds FSR support on ultrawide monitors.

You can see in the cover photo that the 32:9 aspect ratio was applied to a 4K monitor with 3413x960 resolution. Going to be very helpful for those of you who are using ultrawide! To apply FSR, all you need to add to Steam launch parameters is `WINE_FULLSCREEN_FSR=1 WINE_FULLSCREEN_FSR_MODE=ultra %command%`. "ultra" can be changed to performance, balanced, or quality.

See the full patch notes on [GitHub](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-24). And check out the [guide on getting GE-Proton on your system or Steam Deck](https://linuxgamingcentral.com/posts/proton_ge_tutorial/) if you need a refresher.

*Cover image credit: GloriousEggroll*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
