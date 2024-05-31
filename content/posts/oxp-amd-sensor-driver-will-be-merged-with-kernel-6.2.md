+++
title = "Sensor Driver for AMD-Based OneXPlayer Will Be Merged with Kernel 6.2"
date = 2022-11-13T09:53:18-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/onexplayer_mini/cover.webp"
tags = ["news", "driver", "onexplayer"]
keywords = ["onexplayer", "amd", "kernel driver", "sensor driver"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Some good news for those of you who have a OneXPlayer (at least, if you own the AMD variant). The [sensor driver](https://git.kernel.org/pub/scm/linux/kernel/git/groeck/linux-staging.git/commit/?h=hwmon-next&id=fc11f6a2ced634f7f8c57d7454fea4133ec7d8ce) for monitoring and controlling the fan speed will now be merged with kernel 6.2. This is thanks in no small part to **Joaquín Ignacio Aramendía** (Samsagax), one of the [ChimeraOS contributors](https://linuxgamingcentral.com/posts/chimeraos-36/). Previously, you had [to build the driver from source](https://linuxgamingcentral.com/posts/kernel-module-for-onexplayer-now-available/), but in a few months' time, once kernel 6.2 becomes stable, this will no longer be a requirement. Intel owners won't be able to reap the benefits of this "since Intel have different EC registers and values to read/write."

Per the desription from [Phoronix](https://www.phoronix.com/news/OneXPlayer-Linux-Platform-Drv):
> This driver that can be built with the "OXP_DEVICE" Kconfig switch enables controlling the fan interfacing with the embedded controller (EC) of the device. Via standard HWMON sysfs interfaces, the fan can then be controlled by users on Linux or via various applets and other user-space software.

Thanks to the community, devices like the OneXPlayer get much better Linux support, even though the manufacturer only developed the product with Windows in mind. At the cheapest price at [$1,200](https://onexplayerstore.com/products/onexplayer-mini-amd%C2%AE-ryzen%C2%AE-6800u-1920-1201?variant=41916329590964) with 16 GB of DDR5 and 512 GB NVMe, the OXP Mini isn't exactly cheap. It does come with a 6800U though, so that's something.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
