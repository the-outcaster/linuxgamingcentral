+++
title = "DXVK 1.10.3 Adds Halo Infinite Video Patch And Improves GPU Performance for Stray"
date = 2022-08-02T11:26:27-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/dxvk/1.10.3.jpg"
tags = ["news", "software update", "dxvk"]
keywords = ["dxvk", "proton", "halo infinite", "nfs 3", "ninja blade", "stray", "ys origin"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
DXVK has been updated to 1.10.3. New features in this update include the support for shared fences, which is needed for *Halo Infinite*'s videos to work. Fixes and workarounds have been added to *Need for Speed 3*, *Ninja Blade*, and *Ys Origin*. The insanely popular *Stray* has `d3d11.ignoreGraphicsBarriers` enabled "to work around some GPU-bound performance issues." Finally, a regression was fixed from the [previous release](https://linuxgamingcentral.com/posts/dxvk-1.10.2-released/) that caused rendering issues in certain D3D11 titles, including *Bioshock Infinite* and *Prey*.

See the release notes on [GitHub](https://github.com/doitsujin/dxvk/releases/tag/v1.10.3). Should you want to use this immediately, you can download the tarball and extract the x64 DLLs to:

`~/.local/share/Steam/steamapps/common/Proton - Experimental/files/lib64/wine/dxvk`

It would be a good idea to make a backup of Proton Experimental (or whatever version of Proton you want to update) before you do this.

*Cover image credit: taminggaming.com*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
