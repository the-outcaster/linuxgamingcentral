+++
title = "Rumble Support for Xbox Gamepads - Patch Submitted for Review (Again)"
date = 2023-03-09T14:40:40Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/xbox_controller/cover.jpeg"
tags = ["news", "xbox", "gamepad", "kernel patch"]
keywords = ["xbox controller", "xbox rumble", "xbox linux patch"]
description = "This patch adds rumble support to the Xbox One, Series X|S, and Elite Series 2 pads."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Back in October, Google engineer Siarhei Vishniakou submitted a [Linux patch that adds rumble support to the latest Xbox gamepads](https://linuxgamingcentral.com/posts/xbox-series-controllers-rumble-support/), since a firmware update to the controller broke this feature. Vishniakou explains what happened:
> In 2021, Microsoft released a firmware update for this controller. As part of this update, the HID descriptor of the device changed. The product ID was also changed from `0x02fd` to `0x0b20`. On this controller, rumble was supported via
`hid-microsoft`, which matched against the old product ID (`0x02fd`). As a result, the firmware update broke rumble support on this controller.

Evidently, the October patch never made it into the kernel. This patch has come back from the grave and is labeled as "v2". Vishniakou mentions "adding [the] new product ID is sufficient" to bring the rumble back after the FW update.

So this patch will enable rumble support for the following gamepads, in Bluetooth mode and USB:
- wireless Xbox One pad, model 1708, with both the old and new FW
- Series X|S, model 1914
- Elite Series 2, with both the old and new FW

[Bastien Nocera](https://twitter.com/hadessuk), developer at Red Hat, reviewed the patch and commented that it "looks good" although we don't know when it will be approved and merged into the kernel. Hopefully this patch can make it into kernel 6.4.

See the [patch](https://lore.kernel.org/lkml/20230307213536.2299487-1-svv@google.com/) for more details.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
