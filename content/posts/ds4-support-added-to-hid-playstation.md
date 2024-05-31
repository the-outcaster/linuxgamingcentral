+++
title = "Official DualShock 4 Support Coming to Kernel 6.2"
date = 2022-11-14T09:15:57-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/playstation/ds4.jpg"
tags = ["news", "playstation", "sony", "controller", "dualshock 4"]
keywords = ["sony", "playstation", "dualshock 4", "linux"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
While the DS4 has technically been supported via "hid-sony" since way back to kernel 3.15, Sony is adding *official* support to said gamepad by adding backward compatibility to their "hid-playstation" driver, which already has [support for the DualSense/DualSense Edge](https://linuxgamingcentral.com/posts/dualsense-edge-support-coming-to-linux/). The [patch](https://git.kernel.org/pub/scm/linux/kernel/git/hid/hid.git/commit/?h=for-next&id=68e149347be7f72ac5cc1d0239917157dc78b4b6) is confirmed to be merged with the upcoming 6.2 kernel.

The patch will add support for:
- USB/Bluetooth connectivity
- touchpad
- battery status
- vibration
- accelerometer/gyro
- LED brightness

![Patch notes for DS4 support](/images/playstation/ds4_hid_playstation.webp)

Thanks to [Phoronix](https://www.phoronix.com/news/Sony-DualShock4-PlayStation-Drv), as always, for reporting on this.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
