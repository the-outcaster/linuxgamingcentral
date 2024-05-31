+++
title = "HP Dev One - Slim, Sleek, and Fast"
date = 2022-06-12T12:38:36-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/hp_dev_one/hp_dev_one.jpg"
tags = ["hardware review", "hp", "pop!_os"]
keywords = ["hp dev one", "system76", "pop!_os"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Imagine a big computer manufacturer taking interest in a Linux-based distribution, such as Pop!_OS, and wanting to collaborate to put said operating system on their hardware.

That's exactly what HP did. They got in touch with System76, told them how much they liked their Pop!_OS distro, and wanted to tailor-make a notebook with this distro in mind. Thus the [HP Dev One](https://hpdevone.com) was born. No, this isn't a notebook designed specifically for Windows and then marketing comes along and says, "We support Linux too." This product was designed with Linux from the start. And what makes this an even more interesting case is instead of going with Ubuntu or Fedora, HP took note of the solid Pop!_OS distro. It's a good move; Pop!_OS is one of my favorite distros for its ease of use, speediness, and cutting-edge software packages.

Though this notebook is primarily aimed at developers (I'm only a script kiddie, with a basic knowledge of Python), you can do some lightweight gaming with it too. Plus, you're gonna love how fast this thing is, as well as it's incredible battery life, along with a solid, easy-to-type-on keyboard.

So here were the contents after opening up the brown cardboard box shipped by FedEx: the notebook itself, the HP 935 Creator wireless mouse, and the Launch keyboard by System76.

![hp dev one contents with accessories](/images/hp_dev_one/photos/box_contents.jpg)

If you'd like a full unboxing video, I recorded a video a few days back over on my [YouTube channel](https://youtu.be/44vldw-yRXA).

*Note: this review is NOT sponsored by either HP or System76. Opinions are of my own.*

# Specs and Price
The HP Dev One has the following:
- Ryzen 7 Pro 5850U with integrated Radeon graphics (8 cores, 16 threads, base clock of 1.9 GHz to a boost clock of 4.4 GHz)
- 16 GB DDR4 RAM clocked at 3,200 MHz (two SODIMM slots that are 8 GB each)
- 1 TB PCIe NVMe gen 3 2280
- 14", 1080p display (1,000 nits!)
- 720p webcam
- dual audio speakers, 2 multi-array mic
- 3 cell, 53 Wh Li-ion battery
- Wi-Fi 5, Bluetooth 5 (I'm kind of curious as to why they didn't go with Wi-Fi 6)

It comes in a mineral silver finish. HP claims the chassis is scratch-resistant. It is, for the most part (you probably can't see it in the photo; the scratches are very hard to notice). Their fingerprint-proof claim is legit though, albeit for the HP logo on the top. The notebook is also [TCO Certified](https://tcocertified.com/your-product/), if that means anything to you.

![hp dev one top](/images/hp_dev_one/photos/top.jpg)

The hinges open up to 170 degrees. You can pretty much lay this flat like a pancake. I've seen some notebooks that are capable of moving the hinge *all the way* around, making them act like a 2-in-1 device (notebook/tablet hybrid). It would've been cool if HP had done the same here, so that I could also make it act like an extra-large tablet, but 170 degrees is fair enough.

Dimensions of the notebook are 12.73 x 8.44 x 0.75 in (32.34 x 21.46 x 1.91 cm). It's incredibly light at just 3.24 lbs, thin enough that you could consider it an ultrabook, and super sleek while maintaining a 14" screen.

Ports include:
- Kensington lock, two USB 2.0 ports, headphone/mic jack combo (left side) *EDIT (6/13): the USB ports are actually SuperSpeed 5 Gbps.*
- barrel jack, HDMI port, two USB type C ports (right side)

![hp dev one left side](/images/hp_dev_one/photos/left_side.jpg)

![hp dev one right side](/images/hp_dev_one/photos/right_side.jpg)

It's kind of bare minimum, and I would've liked to see an Ethernet jack, but I think if HP added any more ports they would probably have to increase the thickness of the palm rest (it's barely thick enough to allow room for the USB A ports as it is). At any rate I do have a USB-C dock where I can connect in wired mode and allow more peripherals to be connected to the device.

Pre-installed with the Dev One is System76's [Pop!_OS 22.04](https://linuxgamingcentral.com/posts/news-pop-os-22-04-lts-released/) distribution. For those unaware, Pop!_OS uses Ubuntu as its base, but removes Snaps, has more up-to-date software, and (in my opinion) offers a much better desktop experience with things like autotiling and a quick access application launcher. It's one of the few times we have ever seen a big tech company embrace the open-source friendly nature of Linux, and I'm glad HP made the move.

The notebook is priced at **$1,099.** It's certainly set at a competitive price point; a Thinkpad on [Amazon](https://www.amazon.com/Lenovo-ThinkPad-1920x1080-Fingerprint-Reader/dp/B08FRR5PSK/) with identical hardware would cost you $300 more (plus, it's not as bright at only 400 nits, and slightly heavier). Currently, the hardware on the HP Dev One cannot be customized. You can upgrade the RAM and storage later on with off-the-shelf components if you want though.

# The Experience
Something that was a bit concerning was when I first turned the notebook on. The screen displayed an error, saying something along the lines of the fan is not properly working. I would've taken a picture, but the message only appears for a few seconds and I couldn't get my phone out in time. After that the notebook turned off. This happened again when I placed the notebook on top of a notebook sleeve. I think it's sensitive to what it's sitting on.

The second or third time I turned the notebook on, though, things went fine. I went through the initial setup of Pop!_OS, set my username, password, timezone, Wi-Fi, all that jazz. During the last step of the installation process, I was asked if I wanted to opt-in to HP analytics. This normally doesn't appear on installations of Pop!_OS on other hardware (there's also a EULA). Analytics will supposedly allow HP to better the product in some way. What that way is, I don't know just yet.

![hp dev one analytics option](/images/hp_dev_one/analytics_during_install.png)

At any rate you have the option of turning the analytics on or off, and you can also see at a glance the kind of data that will be sent to HP. For the sake of my review, I turned analytics on. Hopefully HP can make some good use out of it. If you change your mind you can opt-out any time by going to the Settings menu in Pop!_OS and going to the Privacy tab.

I won't go into detail about Pop!_OS itself; I'm sure plenty of you out there have heard about it and perhaps even tried it out yourself. I also won't get into the Launch keyboard that I was sent; I have already written a review on it on [Boiling Steam](https://boilingsteam.com/launch-hands-on-with-system76s-keyboard/). What I will say, though, is this: my next problem was I couldn't update the packages on my system. When I tried to update my software packages via the Pop!_Shop I would get this:

![hp dev one update error](/images/hp_dev_one/update_error.png)

Even after reboot I would still get this. I ended up having to remove the lock file. After that was done, I could update my packages successfully. A bit of a bad start if you ask me, but nothing too glaring.

HP worked with AMD behind the scenes for the optimized battery life and quick suspend/resume. I was told at the [HP Dev One reviewers' workshop](https://linuxgamingcentral.com/posts/hp-dev-one-conference-highlights/) that the quick suspend/resume has been upstreamed into the mainline kernel. I don't know if they also upstreamed the battery life features.

The Dev One ships with its own set of wallpapers, rather than using the stock set that Pop!_OS supplies. Here's the default:

![hp dev one default wallpaper](/images/hp_dev_one/default_wallpaper.jpg)

And here's the rest of the ones available, if you can see them:

![hp dev one wallpaper selection](/images/hp_dev_one/wallpaper_selection.jpg)

The screen is the brightest HP has ever shipped, and is capable of emitting 1,000 nits. I had taken two photos -- one with the screen at the lowest brightness, the other at the highest. I would have put them here so you could compare but after seeing them on the computer, the brightness was just the same (my phone's camera probably auto-adjusted the brightness). You'd just have to see for yourself in-person (or maybe someone else's review will cover it). Regardless, it is *very* impressive. The highest brightness might kill your battery though (and maybe your eyes too).

But stay away if you were looking for an anti-glare display; you can practically use the display like a mirror:

![hp dev one screen glare right side](/images/hp_dev_one/photos/glare_right_side.jpg)

![hp dev one screen glare left side](/images/hp_dev_one/photos/glare_left_side.jpg)

I dig what they did with the webcam; they actually added a *physical* shudder that you can slide to the right to hide it. I wasn't even aware about it until I was told at the dev conference. It's a nice thing to have. Software killswitches are useful too, but I have more confidence in knowing that I'm not being watched with a physical slider. There are Function keys for disabling the mic and for enabling/disabling airplane mode too. Good privacy options, combined with a privacy-friendly operating system!

The keyboard is very good. It has a nice touch as I press the keys (I think they're rubberdome). It's quiet too. There's a little nub in the center should you prefer that over the touchpad (maybe you won't need to buy a ThinkPad again?). The keyboard is spill-resistant from what I've heard, but I'm too nervous to test that myself. I'd like to keep this unit as long as I can. There's backlights for the keyboard so you can see what you're typing in the dark, but it's this standard white color. Would have been nice to see different color LEDs. I guess that's just the gamer aesthetic in me, and because this isn't for gamers I probably should have seen this coming.

Speaking of the touchpad, it has a decent size to it, and offers this satisfying "click" sound when tapping it. You can also use the buttons above the touchpad to act as your left- and right-mouse click buttons.

![hp dev one keyboard](/images/hp_dev_one/photos/keyboard.jpg)

The sound? It's great! It's plenty loud enough, and there's no saturation on the highest volume.

While I was wondering what the honest point of supplying the Launch keyboard was when the built-in keyboard of the notebook is good enough, I discovered that I can make use of the Launch by connecting the notebook to an external display. I can then shut the lid of the notebook off, connect the Launch to a USB port, and treat the Dev One like a desktop. So, the keyboard will come in handy should you want to dock the notebook.

![hp dev one docked](/images/hp_dev_one/photos/docked.jpg)

Unfortunately the BIOS is proprietary. Supposedly HP was close to incorporating System76's open-source Coreboot during the production of the notebook, but they ran out of time. What is nice, however, is the fact that firmware updates for the device are released via LVFS. Meaning all the firmware components in the notebook can be upgraded through Pop!_OS directly; no need to run Windows to upgrade the firmware.

# Support
HP has technicians who are dedicated specifically for helping those with the HP Dev One. And the neat thing is you can contact them directly under the Support tab in the Settings menu, without having to resort to a web browser. I have no need to contact them at the moment but it's definitely nice to see not only support from the team at System76, but also HP. I'm sure customers will made good use out of it.

![hp dev one support menu](/images/hp_dev_one/hp_support.png)

# The Mouse
In addition to getting the notebook itself, HP was kind enough to send over their 935 Creator wireless mouse. This is an optional accessory that you can get when purchasing the notebook and costs $80.

It's *super* comfy to hold. It's shaped perfectly to fit inside my large hand. It has hyperscrolling, which means the scroll wheel can scroll for a long time depending on how fast you move it, and you can turn this on or off with the button just below it. The scroll wheel can also move left or right; by default this moves to the left or to the right of a webpage. This is interesting, I have never seen a scroll wheel do this before!

If you take the cover off the bottom of the mouse, you'll notice a tiny USB dongle that's magnetized. If you take that out and put it into one of the USB ports of the notebook, you'll be able to use it wirelessly. But what's great is the mouse also supports Bluetooth. Meaning if you wanted to save yourself a USB port, you can put the dongle back and use the mouse wirelessly via Bluetooth. What's more, up to two devices can be paired with the mouse, and you can have a third computer use the USB dongle. So if you have three running computers, you don't have to unplug the receiver and put it into the computer you want to use, or disconnect the Bluetooth connection from one computer and have to re-pair with another. You can just press the pairing button on the mouse and it will switch modes. Then presto, your mouse is already working on the next computer. (This is a bit difficult to explain, but I hope I'm making sense.)

Battery life of the mouse is advertised for *three months*. I'm obviously not going to be testing that, as it would take *way* too long to get the review out, but I have reason to believe the claim. I've been using this notebook for a littles less than a week now with the mouse and it's *still* at 55% (it was 55% when it first shipped). You can charge the mouse with the supplied USB C cable. Charging the mouse from empty to full, at least according to the manual, is two hours. Speaking of the cable, if you *really* insisted on low latency with your mouse, you can go ahead and connect the mouse in wired mode. It's pretty neat. 

It also has three programmable buttons on the side; you can configure what they do with the [Mouse Configurator app](https://github.com/pop-os/mouse-configurator). By default they move up a webpage or back, and the middle button serves as a way to switch between two windows. I configured mine to skip, pause/play, and go back to previous tracks while listening to music, because there's no hotkeys available for this on the keyboard.

![hp 935 creator mouse configurator](/images/hp_dev_one/mouse_configurator.png)

With the configurator app you can also customize the DPI, so you can adjust it to a higher rate when gaming for example, or slow it down if it moves too fast. Left click, right click, scroll wheel click, scroll left and scroll right can also be customized to do different functions.

In addition to all of this, you can configure up to four profiles and switch between one over the other by simply going to the dropdown menu and selecting the profile you want. These profiles can be given a custom name too, to make profiles easier to distinguish.

One thing that I don't like about the app though is it needs root privileges in order to run. I will have to ask System76 why that is; they were the ones who wrote the program (and interestingly, it's mostly written in Rust). I would also like to have seen this app pre-installed with the notebook; this app has to be installed separately. I would think customers, at least those who order the mouse along with the notebook, would want to have the customization software available out-of-the-box.

Oh, and one other thing. HP may want to update the instructions in their booklet. Right now it says get the mouse app on Windows. There's an app for that on Linux, you know.

![hp 935 creator booklet](/images/hp_dev_one/photos/booklet.jpg)

# Battery Life
Would you believe it if I said this notebook lasted for **21 hours** on a single charge? You probably would if I told you I had the notebook on idle, at the lowest brightness, with the keyboard backlight off, Wi-Fi and Bluetooth off, and no peripherals connected. Still, that's how long this thing lasted under those circumstances. Were you to slightly increase the brightness and do your work with Wi-Fi on, you would still likely get a good 12 hours or more, just as HP said in the dev conference.

On the other hand if you're looking at local video playback, under the same circumstances as the first test I did, you're only going to get about **four hours**. Seeing as this notebook is aimed towards devs, however, chances are you're not going to use the device for video viewing.

HP claims the battery can charge up to 50% in just half an hour. When my notebook died, I plugged it in and set a timer for 30 minutes. After the 30 minutes were up, I turned the notebook back on and low and behold, it was at 51%. Their claim is indeed true! So you would have a full charge in just an hour. Keep in mind the notebook has to be *off* though; if it's running then it will obviously charge at a slower rate.

# Benchmarks
As a developer, you're going to care how quickly your code can compile. So I demonstrated this by measuring the time it would take to compile the Linux kernel. Phoronix Test Suite measured **123.96** seconds. This would rank around the 32nd percentile rank on [openbenchmarking.org](https://openbenchmarking.org/test/pts/build-linux-kernel-1.13.0) and compiles a couple of seconds faster than the Intel Core i7-5960X. So, not exactly the fastest processor out there, but for smaller projects I think you'll find the speed to be fine.

How about compression and decompression rates? I measured those too. 7-Zip compression is **55,310** MIPS. Decompression is **52,886** MIPS. Compression ranks at the 49th percentile on [openbenchmarking.org](https://openbenchmarking.org/test/pts/compress-7zip-1.8.0) and does just a little better than the Intel Core i7-10700, but slightly worse than the AMD Ryzen 5 5600G. Decompression would rank as the 53rd percentile, coming faster than the Ryzen 7 2700X but behind the Ryzen 7 4800H. Not bad!

# Gaming?
You might be surprised how well this thing handles 3D graphics, despite it coming with no discrete GPU. Here's *DiRT 5* at medium settings, downscaled to 720p, with FSR and GameMode enabled:

![hp dev one dirt 5 benchmark](/images/hp_dev_one/benchmarks/dirt5.jpg)

And *Shadow of the Tomb Raider* with the same settings:

![hp dev one sottr benchmark](/images/hp_dev_one/benchmarks/sottr.jpg)

I could *almost* get 60 FPS on *Splitgate* on high settings with 75% resolution scaling. I think you would be better off at medium settings with native resolution though. So I think it's safe to say you can do some light to moderate gaming on this machine. AAA games will have to be downscaled at 720p with medium settings, and even then you'll have to withstand an average of 30 FPS. But yeah, gaming is *kind of* an option here.

# Repairability
The bottom of the chassis consists of five Torx screws. You take those off, then pry the bottom open with some spudgers to get access to the guts of the system. The RAM and NVMe modules are covered by a metal shielding. When you take those off, you can now upgrade the storage and RAM. You can use up to two SODIMM memory chips, and the notebook supports a full 2280 NVMe drive. The battery is also tucked away inside here, which can be taken off by disconnecting a few molex connectors and unscrewing a few Philips screws.

![hp dev one bottom](/images/hp_dev_one/photos/bottom.jpg)

I would like to say getting access to the guts was easy, but it was honestly a bit tedious. For one thing, the screws are Torx. Why go with Torx when customers are more likely to have a Philips at hand? I used a T6 to unscrew the screws, but I think it was one size too large. It was the smallest Torx bit that I had. I was finally able to get them off after a lot of fiddling. I would like to see HP go for Philips or even Flathead screws should they decide to make a successor to this model. I would also like to see the battery on the *outside* of the chassis rather than inside, but that decision was probably made so the chassis can stay thin and on a diet.

![hp dev one guts](/images/hp_dev_one/photos/guts.jpg)

# Worth It?
Depends on what your use case scenario is. Developing, yes. Gaming, eh, not so much. Lightweight gaming is alright. The keyboard is very nice, the screen is super bright, the chassis is light and sleek, the battery is long-lasting, there's a physical shudder for the webcam, plenty of RAM, plenty of storage. It's also going to cost you a lot less than other notebooks with similar hardware. And you get one of the best Linux distributions pre-installed as a bonus.

If you're someone who travels often, you'll appreciate the light weight. If you're someone who's into web development, or maybe you're a writer, or maybe you just want a notebook so you can watch movies, yes, I would definitely recommend the HP Dev One. But as I said, gaming may not be to your liking here. And you might get a few initial hiccups when turning the system on for the first time or updating your system. Thumbs down for the Torx screws as well.

**TL;DR**

The good:
- light, sleek
- super bright display
- solid, quiet keyboard that comes with a nub
- *incredible* battery life
- physical shudder for webcam
- upgradable RAM and NVMe storage
- capable of lightweight gaming
- great price
- LVFS firmware updates
- Pop!_OS was a good choice for the pre-installed OS

The not-so-good:
- total opposite of anti-glare
- Torx screws for disassembly
- a few software hiccups when I first turned the notebook on
- lacking a lot of ports, including Ethernet
- powered by proprietary firmware rather than Coreboot

I wanted to give a shoutout to both HP and System76 for getting in touch with me and offering me this review unit. You guys are the best!

Interested in purchasing? Head over to the [official site](https://hpdevone.com)! No need to comb through an endless catalog of laptops; HP created a site specifically for the Dev One, so you can buy it right away. Big caveat here though: **the HP Dev One is available only in the US.** No word on if or when HP will ship internationally.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
