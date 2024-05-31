+++
title = "ASUS ROG Ally: Can it Linux?"
date = 2023-06-15T18:54:24Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/asus_rog_ally/linux/cover.webp"
tags = ["news", "asus rog ally"]
keywords = ["asus rog ally", "linux on asus rog ally", "chimeraos", "ubuntu 23.04"]
description = "Seems like it works well with Linux, outside of missing Wi-Fi and fingerprint support."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Phoronix recently reported on [Ubuntu 23.04 compatibility with the ROG Ally](https://www.phoronix.com/review/asus-rog-ally-linux). The gist of it is: most features worked out of the box. But Wi-Fi wasn't working.

Unlike the Deck, you can't access the BIOS with the handheld itself. You'll need to attach a keyboard. "From there it's akin to the standard ASUS BIOS configuration area." Secure Boot is enabled by default, but it can be disabled from here.

When booting from the USB flash drive, the touchscreen support worked, as well as the graphics acceleration and Bluetooth. The built-in controls are able to make use of the Xpad kernel driver. Michael was able to monitor the SoC temperature and control the fan speed with asus_custom_fan_curve. However, the Wi-Fi doesn't work OOTB -- Michael had to use Ethernet via a USB-C dock to workaround this. It does look like there's [a patch](https://lore.kernel.org/lkml/20230614063252.1650824-1-kai.heng.feng@canonical.com/T/) that's in the works, but it probably won't show up in the mainline kernel until 6.5. The fingerprint sensor also didn't work.

![ChimeraOS on ROG Ally](/images/asus_rog_ally/linux/chimeraos.webp)
*Image credit: ETA Prime*

A few weeks ago ETA Prime [checked out ChimeraOS with it](https://www.youtube.com/watch?v=6r8t90fW7Kg) and mentioned that the audio didn't work out of the gate. He mentioned that Wi-Fi worked, but only "half of the time." It wasn't possible to adjust TDP via the Quick Access Menu; that can only be done through the BIOS. Otherwise, he mentioned "it's actually working really well for kind of just the first install."

Still, some pretty exciting news if you're looking to run Linux on this handheld. It seems like, outside of some minor quirks, everything works as intended.

*Cover image credit: Phoronix*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
