+++
title = "ASUS ROG Ally to Get Sound Support with Kernel 6.5"
date = 2023-06-22T19:40:25Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/asus_rog_ally/linux/ubuntu_on_ally.webp"
tags = ["news", "asus rog ally"]
keywords = ["asus rog ally", "asus rog ally on linux", "asus rog ally sound on linux support"]
description = "Thanks to Matthew Anderson for quickly releasing this patch!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
The ASUS ROG Ally seems to have [fairly decent out-of-the-box Linux support](https://linuxgamingcentral.com/posts/can-the-ally-use-linux/), albeit for missing Wi-Fi. However, one detail that Phoronix omitted was the audio support. There currently isn't any audio support for the Ally.

Well, leave it up to my buddy Matthew Anderson -- one of the ChimeraOS developers -- to quickly address this problem by means of a [patch](https://git.kernel.org/pub/scm/linux/kernel/git/tiwai/sound.git/commit/?h=for-next&id=724418b84e6248cd27599607b7e5fac365b8e3f5). In addition to the patch itself, this will also need "a patched ACPI table" or firmware from ASUS:
> This requires a patched ACPI table or a firmware from ASUS to work because the system does not come with the _DSD field for the CSC3551.

This patch has already been approved for the upcoming 6.5 kernel. Great to see more Linux support for other competing handhelds out there.

In other news, Phoronix just put out a [benchmark](https://www.phoronix.com/review/rog-ally-windows-linux) comparing the performace of the Ally with Windows 11 and Ubuntu 23.04. Spoiler: Ubuntu actually does a bit better than Windows 11 in most cases, but slightly worse than Windows 11 "Turbo".

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
