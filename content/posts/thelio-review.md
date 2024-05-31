+++
title = "A Look at the Thelio Desktop by System76"
date = 2022-11-25T02:04:26-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/system76/thelio_review/cover.jpg"
tags = ["hardware review", "thelio", "system76", "desktop"]
keywords = ["thelio", "system76", "nvidia", "intel", "rtx 3060", "i5-13600k"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
The Thelio by System76 is an impressive-looking desktop. It comes in a black finish, mostly rectangular in shape, and is very mimimalistic in design.

A few months ago, the Thelio went through a [redesign](https://linuxgamingcentral.com/posts/system76-unveils-new-thelio/). Instead of the accent going around part of the front and the entire right side, it is now just a small sliver at the front. It's also user-replaceable; users can take it out and replace with a different design if they so choose. The right side of the chassis has now been replaced with an etching of the Rocky Mountains, just like the left side. The design makes sense; the chassis was designed in Denver, Colorado after all.

![Thelio front](/images/system76/thelio_review/front.jpg)

When the initial batch of Thelios went out to reviewers, I was like, "Why didn't I get one?" But Adam Balla -- media relations manager at System76 -- told me that I'm actually the first person to be reviewing the Thelio with the new [Raptor Lake processor](https://linuxgamingcentral.com/posts/thelio-by-system76-gets-ryzen-7000-and-13th-gen-intel-cpus/). Don't I feel special?

# Package Contents
The package, when it came to my door, was somewhat barebones. The box that it came in was *enormous*.

![Thelio box](/images/system76/thelio_review/box.jpg)

Inside of that box was the System76-designed box for the Thelio, protected by four corner pieces of foam. The desktop itself is protected by a top and bottom layer of foam. Taking that out reveals the Thelio, a power cord, an instruction manual for swapping out the accent, and a welcome card. The welcome card says:

> Greetings from Thelio! Thanks for joining us on our mission into the world of open hardware. If you're new to Linux, there are a ton of open-source software applications you can download for free in the Pop!_Shop or Ubuntu Software Center. Our support team is ready to help out if you have any questions. The links on the right are a good place to start! Have fun and enjoy your journey!

![Thelio top with welcome message](/images/system76/thelio_review/top.jpg)

Other than that, that's it. I'm surprised they didn't give me any HDMI or DisplayPort cables. Neither did they send any additional accents; just the walnut version.

# I/O, Specs, and Price
I have the *base* Thelio model. There's several different versions depending on your needs. The base Thelio has the following I/O, from top to bottom:
- CMOS button
- HDMI 2.1
- DisplayPort 1.4a
- four USB 3.2 Gen 1 ports
- two USB 3.2 Gen 2 ports
- 2.5-Gigabit Ethernet
- Wi-Fi 6E + Bluetooth 5.2
- two USB type-C ports with Thunderbolt 4
- two Mini DisplayPorts
- mic in, line out, line in

The GPU (the RTX 3060, in my case) has:
- HDMI 2.1
- three DisplayPorts 1.4a

![Thelio back ports](/images/system76/thelio_review/ports-back.webp)

On the front, there's the System76 logo at the bottom, the accent to the right of that, and a power button towards the top-left. The power button has a white LED; it's solid when the system is on, and slowly cycles back and forth to a dark gray to white when it's asleep. The left and right panels have "THELIO" text printed on them, along with a sketching of the Rocky Mountains.

The base Thelio measures 32.7cm x 20.7cm x 29.1cm (~13" x 8" x 11"). It's small enough where you could comfortably sit it on your desk, rather than on the floor. A pretty neat design is the vent on the back of the case has the shape of our solar system. The bottom of the chassis has a rubber foot for each corner and a venting hole for the giant fan.

Typically when I request a review unit from System76, I'm able to choose what parts I want. Not so the case with the Thelio. The parts that came in my build are as follows:
- i5-13600K -- 14 cores, 20 threads, max speed of 5.1 GHz
- PNY RTX 3060 -- 12 GB VRAM and 3,584 CUDA Cores
- Kingston 32 GB DDR5 (2x 16 GB, clocked at 5,600 MHZ)
- Samsung 980 Pro 1 TB PCIe Gen 4 NVMe (sequential read and write speed of 7k/5k MB/s respectively)
- [MSI MEG Z690I UNIFY](https://www.msi.com/Motherboard/MEG-Z690I-UNIFY/Specification) Mini-ITX motherboard
- [Thelio I/O](https://github.com/system76/thelio-io) daughterboard running [open-source firmware](https://github.com/system76/thelio-io-firmware) -- this is what powers any additional 2.5" hard drives that you may want to install
- 650 W PSU ([FSP Dagger Pro](https://www.fspgroupusa.com/ecommerce/daggerpro650w.html))

![Thelio side panel](/images/system76/thelio_review/side.jpg)

Now this is the part where you're probably rolling your eyes. "Yet another Intel/NVIDIA combo?" Yes, sadly. I'm honestly tired of getting Linux hardware that's powered by proprietary graphics drivers. If we come across a problem, the community can't come up with a fix. We're at the mercy of the company to fix it. *Sonic Frontiers* is a great example of a game that suffers from [terrible framerates](https://github.com/ValveSoftware/Proton/issues/6303) on NVIDIA due to the DRM. On AMD? Works just fine. The best discrete AMD GPU that you can get with the Thelio is the 6600. I'm seriously hoping System76 will be able to obtain more AMD GPUs, and more powerful ones at that. The 6900 XT/XTX launches next month; wonder if they could get those once they're out? Even a 6700 XT would be good enough.

The motherboard only has support for one GPU. Max clearance is 278.175mm (~11"), but recommended clearance is a little less at 268.175mm. It comes in a Mini-ITX form factor and runs System76's non-open firmware. It uses the 1700 socket and the Intel Z690 chipset, compatibile with Alder Lake and Raptor Lake processors.

When selecting the parts for your Thelio, you can choose either Intel 12th- or 13th-gen or AMD Ryzen 5000 series for the processor. If you choose to go with Intel, you have the option of upgrading the RAM from DDR4 to DDR5. You also have the option of adding PCIe Gen 3 storage. GPUs range from the 1030 all the way to the RTX A4000. As I said before, AMD GPUs are lacking here. The only ones available at the time of writing this is the 6500 XT and the 6600.

![Thelio bottom](/images/system76/thelio_review/bottom.jpg)

**The base price for the Thelio, at the time of writing this, is $949.** This would come with the 12th-gen Intel G7400, 8 GB of DDR4, 128 GB of storage (presumably PCIe Gen 3), and a 450 W power supply. **The most expensive option with a Ryzen processor would cost $7,485** and would have the Ryzen 9 5950X, 64 GB DDR4, 16 TB of PCIe Gen 4 storage, an additional 20 TB of traditional HDD, the RTX A400, and a 650 W power supply. **The most expensive Intel option would be $9,196** would have the i7-13700K, 64 GB DDR5, 16 TB of PCIe Gen 4 storage, 8 TB of PCIe Gen 3, 20 TB HDD, the RTX A2000, and a 650 W power supply.

My configuration came to **$2,229.**

# Repairability
Getting access to the parts inside the Thelio require unscrewing four Philips screws on the back, located on the outermost corners, then lifting the chassis up. This is different than most desktop cases; they require removing two screws and sliding the side panel off. System76 has a detailed [overview](https://tech-docs.system76.com/models/thelio-b4/internal-overview.html) of each individual component inside the chassis. 

![Thelio chassis off](/images/system76/thelio_review/chassis_off.jpg)

Not only this, but they give [instructions](https://tech-docs.system76.com/models/thelio-b4/repairs.html) on how to remove or replace these components. For instance, if you wanted to add a 2.5" hard drive, you would take the two screws out of the drive bay cover, take one of the black plastic rings provided and four screws, insert the screws into the drive, then slide the drive into the daughterboard. Pretty neat that the screws are already provided for you right inside the chassis. 

![Thelio drive bay](/images/system76/thelio_review/drive_bay.jpg)

If you wanted to replace the GPU, you would take out the two screws holding the PCIe bracket in place, unscrew four screws holding the side GPU brace, then take the GPU out by removing the power connector, followed by the clip that's on the PCIe connection. It's really amazing for them to document this. They have labels for all of the pictures to make it easy to follow as well.

Here's *most* of the components taken out:

![Thelio parts](/images/system76/thelio_review/all_parts.jpg)

Wasn't very difficult to take it apart, but if you plan on upgrading the processor, know that it's going to be a bit of a pain. You're going to have to take a lot of stuff out -- the GPU brace, the CPU fan, and the *massive* heatsink. Replacing the RAM is also going to be a pain if you don't take the GPU out first. Other than that I think the system is very well-designed as far as upgradability.

# The Experience
As with any review unit that System76 sends to me, Pop!_OS 22.04 comes pre-loaded as the operating system. I'm not going to get into detail regarding Pop!_OS itself; there's plenty of those kind of reviews out there. But I will say this -- similar to Matthew's review of the [HP Dev One](https://linuxgamingcentral.com/posts/hp-dev-one-review-by-chimeraos-dev/), I don't like the way Pop!_OS handles AppImages. If you want to run an AppImage, you have to right-click it and select "Run as program". You can't simply double-click it and expect it to run. I don't enjoy this inconvenience.

![Pop!_OS AppImage quirk](/images/system76/thelio_review/appimage_quirk.png)

There's also that weird thing going on with the Pop!_Shop. Sometimes you don't know whether you're installing the Flatpak version of an app or the native .deb package. Sometimes there will be an option to choose between the two packages, sometimes there won't. I'd like to see a more streamlined approach here, especially for newcomers to Linux who want their software to "just work."

![Pop!_OS Pop!_Shop app installation quirk](/images/system76/thelio_review/pop_shop_quirk.jpg)

That aside, and aside from the fact that I'm using a NVIDIA graphics card, my gaming experience has been quite pleasant. I recently picked up [*Gotham Knights*](https://store.steampowered.com/app/1496790/Gotham_Knights/) while it was on sale, and I've been enjoying it on the Thelio. After the game is done compiling shaders, I can get a comfortable 90-120 FPS on the highest graphics settings at 1080p, upscaled to 1440p with DLSS. Framerate varies depending on where the character is in-game. Inside of buildings, the framerate goes up, which is to be expected since there's a lot less going on than a big open-world map.

The general consensus I can say, with an i5-13600K and a RTX 3060, is you can expect *at least* 60 FPS at 1440p, regardless of how demanding the game is. Intel really did [step up their game with Raptor Lake](https://www.phoronix.com/review/intel-core-i5-13600k/2). When paired with a 6800 XT, the i5-13600K scores an average of 341 FPS with *Dirt Rally 2.0* at 2560 x 1080 resolution, high settings. With an RTX 3060, with the same game and graphics preset, it gets 154 FPS at 1920 x 1080. 4K might be pushing this system to the limit. But thanks to the 3060 being able to make use of DLSS, you should still get a fairly comfortable experience downscaling at 1440p or even 1080p.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/system76/thelio/gotham_knights_gameplay.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

You can see some games in action on [YouTube](https://youtu.be/S1ftRzGg7JE).

The fan inside the system stays fairly quiet well throughout the time I was using it. It gets a little more audible when gaming, but it's not terribly loud.

When I first got the Thelio, I didn't follow the instructions for taking the accent out properly. So when I took it out, I used too much force. I wasn't able to put it back on! So I started panicking. Fortunately, Adam was pretty cool about it. He just sent another accent over, and I was able to successfully replace it after taking the pems out. I won't be taking out again for the sake of demonstration, out of fear I may damage it again. But here you can see System76 properly do it.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/system76/thelio/replacing_accent.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

# Benchmarks
Not going to lie, Phoronix Test Suite failed on a lot of tests I tried with it. *Shadow of the Tomb Raider* kept bringing up the Feral window before launch, the scores when benchmarking *F1 2020* largely stayed the same regardless of the graphics preset, and the kernel compilation test simply wouldn't run at all. It has been a bit frustrating. The only tests that I was able to run successfully was *Dirt Rally 2.0* and Blender. Every other benchmark had to be recorded manually. At any rate, here are the results.

Unless otherwise specified, games are running at 1920 x 1080 and upscaled to 1440p with either DLSS or FSR 1.0, while using GE-Proton7-41 with GameMode enabled.

*Dirt 5* is looking good with an average framerate of 80 FPS on the highest preset.

![Dirt 5 benchmark on Thelio](/images/system76/thelio_review/benchmarks/dirt5.png)

*Horizon Zero Dawn* gets just a little over 100 FPS on average on the highest preset.

![Horizon Zero Dawn benchmark on Thelio](/images/system76/thelio_review/benchmarks/hzd.png)

*Shadow of the Tomb Raider* was benchmarked with the native Linux version, using the game's built-in FSR feature. There are a lot of numbers supplied with each benchmark, so for simplicity's sake, I will just be referring to the "GPU" framerate rather than "CPU Game" or "CPU Framerate". 125 FPS on average on the highest preset.

![Shadow of the Tomb Raider benchmark on Thelio](/images/system76/thelio_review/benchmarks/sottr.png)

*Dirt Rally 2.0* was benchmarked via PTS at both 1080p and 1440p resolutions. Results can also be read [online](https://openbenchmarking.org/result/2211146-NE-DIRTRALLY89). (Thanks to [alkazar](https://linuxgamingcentral.com/posts/interview_with_chimeraos_dev/) from the ChimeraOS team for giving me a Steam key for the game!)

![Dirt Rally 2.0 benchmark on Thelio](/images/system76/thelio_review/benchmarks/dirt_rally2.png)

Benchmarking Blender 3.3, with the BMW27 scene and using just the CPU for computation, resulted in [91.06 seconds](https://openbenchmarking.org/result/2211244-NE-BLENDERCP90). This would rank around the 33rd percentile rank on [openbenchmarking.org](https://openbenchmarking.org/test/pts/blender&eval=c02551fabd58b2f2e3b6100a646fb7e50cd679a5#metrics). It does slightly better than the Xeon Gold 6346, but worse than the i7-12700K.

![Blender CPU benchmark on Thelio (BMW27)](/images/system76/thelio_review/benchmarks/blender.png)

# It's a Nice Desktop, Barred by NVIDIA
I know for a fact System76 has been asked several times if they ever have any plans on selling just the case for the Thelio itself. They've always said no. But I can theorize why that is. It's probably because of how well it's designed. I'm honestly surprised they haven't put a patent on it. It's very simplistic in design, yet it also looks beautiful. The way the chassis goes upwards when getting access to the components is also clever. The wooden accent is a nice bonus that gives the desktop a clean-looking aesthetic.

I wouldn't exactly say the Thelio is a "gaming powerhouse" with the components that I have, but it's definitely going to handle 1080p and 1440p gaming just fine. 1440p should get at least 60 FPS on the highest preset of any game, and you should be getting at least 90 at 1080p. 4K *might* be pushing the CPU and GPU to their limits. So yeah, if you're looking to game, the Thelio is a great choice. And I definitely want to see more AMD GPU options from System76 in the future, because *that's* the vendor where you're going to get the best Linux gaming experience.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/system76/thelio/hzd_gameplay.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

**TL;DR**

The good:
- brilliantly-designed chassis that's simple, yet aesthetically pleasing
- replaceable front accent
- can handle just about any AAA game that you throw at it at 1080p and 1440p
- relatively quiet, even while gaming
- most of the individual components are easy to replace, and there's also step-by-step instructions on S76's website

The not-so-good:
- Pop!_OS has it's quirks, such as the way it handles AppImages and how software gets installed from the Pop!_Shop
- it's using Intel/NVIDIA, and AMD GPU options are lacking
- no HDMI/DisplayPort cables or additional accents are supplied in the package (accents come at an additional charge, but I'm surprised I didn't get more than just one for review)

Get your Thelio at [System76's website](https://system76.com/desktops).

*Review Thelio sent courtesy of System76. Opinions are of my own.*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
