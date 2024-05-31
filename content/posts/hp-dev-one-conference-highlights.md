+++
title = "HP Dev One - Reviewers' Workshop Highlights"
date = 2022-06-09T15:23:33-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/hp_dev_one/cover.webp"
tags = ["hp dev one", "highlights", "hardware"]
keywords = ["hp dev one", "pop!_os", "system76", "hp"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Yesterday I got invited to a Zoom press conference by HP and System76 in regards to HP's Dev One laptop. Here were some of the key points I picked up on. I wasn't sure if I was allowed to post the link to the recording directly, so I will omit it for now until I get the OK from HP. *Edit: it's a no.*

# General
- the goal of HP collaborating with System76 was to make Linux more widespread. Clayton Billion from HP said Pop!_OS in particular is "polished and rich"
- HP claims this is the best notebook for developers (it may be aimed for devs primarily but I've discovered it can do some light-to-medium-weight gaming)
- the Dev One is only available in the US. HP doesn't have a timeline as to when they will ship the laptop internationally (although review units have already been sent outside of the US. Liam from GamingOnLinux got one)

# Hardware
- super bright display (1,000 nits!) that's 14". It's the brightest screen HP has ever shipped
- decent battery life (I haven't tested this thoroughly enough yet but so far their claim is true). 53 Wh. Charges fairly quickly with the suppled AC adapter. HP claims it can last up to 12 hours, and the laptop can get to a 50% charge in just half-an-hour. When the laptop is in suspend it apparently only uses 0.3W (meaning it will last a *long* time)
- keyboard has backlights, is spill-resistant (someone in the call said it survived a night of martinis), and the Windows key that's typically put on other keyboards has been replaced with a Super key. It's also quiet
- stereo speakers (by my testing so far they're pretty decent and can be loud)
- chassis is scratch- and fingerprint-resistant. Small footprint and only weighs 3 lbs. 170 degree hinge
- webcam (720p) has a physical shudder which hides it
- the processor (Ryzen 7 PRO 5850U) allows for seamless multi-tasking
- laptop has 2 SODIMM slots. By default each one has a 8 GB DDR4 chip clocked at 3200 MHz. Can be upgraded to have a total of 64 GB
- The PCIe NVMe drive is gen 3 and can support a full-size 2280 (1 TB is supplied by default). Speed transfer is 3 GB/s. Allows files to be saved quickly
- laptop is relatively easy to take apart (there are 5 torx screws on the bottom. Kind of wish they went with Philips). You can upgrade the RAM and storage by taking off the shielding to the components

# Software
- HP collaborated with AMD closely so suspend and resume features could work properly out-of-the-box, and also so the battery life could last as long as it does. The suspend and resume functionality has upstreamed into the kernel
- can send support tickets to HP directly from Pop!_OS. There are a few devs from HP who have been trained specifically to support the Dev One
- all of the hot keys/Function keys work out-of-the-box (sometimes if you get a laptop and put Linux on it, some of the Function keys may not work)
- you can optionally opt-in to analytics so HP can improve the product (you will be asked this when you're first setting up the computer). You can opt-out at any time by going into the Settings menu under the Privacy tab
![hp dev one analytics](/images/hp_dev_one/analytics.png)
- firmware updates are released through LVFS. Updates are done behind-the-scenes and are all handled by Pop!_OS (you don't need to dualboot with Windows in order to update certain firmware)
- all updates come directly from the Pop!_OS repos
- autotiling was put into Pop!_OS in 2020 as a result of many devs and customers using i3
- with the Pop!_Shop you have thousands of apps at your fingertips, plus you have the ability to install them as a Flatpak is they're available
- the HP 935 Creator wireless mouse (the mouse that came with my review unit) has customizable buttons (you can program them to do different things) with the Mouse Configurator software app. Up to four different profiles can be customized. For some reason the app requires root access (I should ask S76 why that is). Battery supposedly lasts up to three months on a full charge. Can either use the mouse through Bluetooth or with the supplied USB dongle. The app is installed separately
![hp dev one mouse configurator](/images/hp_dev_one/mouse_configurator.png)
- the laptop was going to ship with Coreboot (S76's open-source firmware) but the team ran out of time. It will likely be available in the next-gen product though

Towards the end I had asked if they have ever planned on adding a discrete GPU to the unit. Nope. It was always planned to have a powerful CPU. They did strike a good balance between processing power and battery life.

If you're interested in buying one, head over to the [official site](https://hpdevone.com). The laptop itself is $1,099. Optional accessories include the mouse ($80) and the Launch keyboard ($285). I will have a review of the laptop posted soon, so stay tuned for that! Also I did an [unboxing video](https://youtu.be/44vldw-yRXA) a few days ago if you want to see what I got.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
