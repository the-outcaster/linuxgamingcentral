+++
title = "I Switched From NVIDIA to AMD. Here's What Happened"
date = 2023-01-16T16:06:33Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/interviews/ben_romer_canonical/amd_vs_nvidia.jpg"
tags = ["impressions", "amd", "nvidia", "comparison"]
keywords = ["nvidia geforce gtx 1660 super", "1660 super", "amd 6700 xt", "nvidia", "amd", "linux", "fedora", "nobara project"]
description = "Moving from a 1660 Super to a 6700 XT...has it been a bed of roses?"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
NVIDIA. The green giant is just about in every electronic you can think of. It's in your Switch. In your [handheld](https://en.wikipedia.org/wiki/Nvidia_Shield_Portable). In your [tablet](https://en.wikipedia.org/wiki/Nvidia_Shield_Tablet). In your [console](https://en.wikipedia.org/wiki/Nvidia_Shield_TV). Every review unit that I've received from System76, whether it be a [desktop](https://linuxgamingcentral.com/posts/thelio-review/) or [laptop](https://linuxgamingcentral.com/posts/oryx-pro-by-system76-review/), was powered by discrete NVIDIA graphics. Heck, I wouldn't be surprised if Tegra ends up in a *phone* someday.

The funny thing is, despite how proliferant NVIDIA is in devices, the company doesn't really care about Linux users. Their Nouveau driver, while open-source, is complete garbage. Chances are if you're on Linux and you want decent gaming performance, there's a 98% chance you're using their proprietary graphics driver stack. We're starting to see a spark of hope with the new open-source [NVK](https://linuxgamingcentral.com/posts/nvk-making-progress/) driver, created by some of the Collabora and Red Hat developers, but that's going to need quite some time in order for users to make the switch. Intel is actually making some [great progress](https://www.phoronix.com/review/linux62-intel-radeon) with their discrete ARC cards starting with kernel 6.2 and Mesa 23, so that might become another option in the future besides AMD.

I've been a long time NVIDIA user and I grew tired of it. I finally executed my move to AMD. The weapon of choice? The [XFX Speedster SWFT 309 Radeon RX 6700 XT](https://www.xfxforce.com/shop/xfx-speedster-swft309-amd-radeon-tm-rx-6700xt-core-gaming-graphics-card-with-12gb-gddr6-hdmi-3xdp-amd-rdna-tm-2-). No, I'm not popular enough to get samples of the latest and greatest cards (*cough* ~~lucky-ass bastard~~ [Phoronix](https://www.phoronix.com/review/rx7900xt-rx7900xtx-linux) *cough*). But I did wait patiently enough so that I could get a good deal on a used card. Got it for $290 a few weeks ago. Some of you poor lads told me that you've spent *twice* that amount on the same card just a few months ago while GPU prices were through the roof. Patience has its rewards (although, ironically, I tend to view myself as very *impatient*).

![XFX 6700 XT](/images/6700xt/gpu.jpg)

In brief overview, this 6700 XT in particular has the following:
- base speed of 2,321 MHz; boost clock up to 2,581 MHz
- 12 GB GDDR6 VRAM
- memory clock speed of 16 GBPS
- uses RDNA 2, similar to the technology used in the Deck's APU
- three DisplayPorts (version 1.4)
- one HDMI 2.1

It requires two 8-pin PCIe connectors...so if you plan on getting one of these, make sure your PSU has this. Ideally you also want your PSU to be 650 W or higher.

It was quite a big upgrade compared to the 1660 Super that I was using for about three years. Just observe the difference in size:

![1660 Super vs. 6700 XT size comparison](/images/6700xt/size_comparison.jpg)

Heh, it barely fits inside my Micro ATX case:

![6700 XT inside mATX case](/images/6700xt/inside_case.jpg)

And yeah, in case you were wondering about the PSU in this picture, I *did* upgrade to a 750 W later on.

So, what has it been like switching from the 1660 Super to the 6700 XT? You think it's just been a bed of roses? Well, actually, it has been. For the most part, anyway.

# No Proprietary Driver
I think the biggest relief that came from switching to AMD is the fact that I no longer have to put up with proprietary drivers. Don't get me wrong -- the NVIDIA driver is pretty decent for what it's worth. But because it's proprietary, as I've said many times before, everyone is at the mercy of the green giant whenever there's a bug or a security loophole. There's no one to wait for other than NVIDIA to patch these, and for all NVIDIA could care, they could take their sweet time doing so.

It's not just that though. Distro maintainers have the burden of trying to get in touch with NVIDIA to include their drivers in their distro to otherwise avoid legal issues. With Mesa, I don't have to worry about that. I can install just about *any* distro and have the Mesa drivers included out-of-the-box, no questions asked.

What about upgrading the distro? On [Nobara Project](https://linuxgamingcentral.com/posts/nobara-project-impressions/), you have to remove the NVIDIA drivers entirely before upgrading. No need to do that on AMD.

![Notes for upgrading to Nobara 37](/images/6700xt/upgrading_nobara.png)

I don't know if it's just me, but it seems like the NVIDIA drivers take up your entire system. In other words, your distro's life will depend on those drivers after they've been installed. If you decide to uninstall them for whatever reason, then reboot, you will be greeted with a terminal window, with no graphical environment whatsoever because there's nothing else to back up the display server. I've had scenarios like that happen, and at that point my distro has pretty much been destroyed, even after re-installing the drivers. Only choice I have at that point is to back up my data then re-install the entire distro.

# Open-Source Drivers...Funded by Valve
AMD and Intel's graphics drivers are powered by the Mesa graphics drivers, which are open-source. And, if you think the developers aren't getting paid, they *are*, and they're certainly not slacking off. Last month, when [The Verge interviewed Valve's Lawrence Yang and Pierre-Loup Griffais](https://linuxgamingcentral.com/posts/valve-doesnt-consider-6800u-handhelds-as-competition/), they had mentioned that the company is paying *over 100* developers to work on Mesa, Proton, and Vulkan. That work isn't just going towards the Steam Deck: it's going toward everything that uses Mesa, including desktop AMD GPUs, CPUs, Intel CPUs/GPUs, and even NVK. So pretty much *everyone* will benefit, except NVIDIA. Drivers are constantly getting updated with bug fixes, new features, and more.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/6700xt/ccr.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

Bonus: because the drivers are [open-source](https://gitlab.freedesktop.org/mesa/mesa/), you are free to contribute if you know C/C++. Found a bug? Know how to fix it? Submit a pull request!

# No Vendor Lock-In
Unlike NVIDIA, AMD doesn't try to lock you in to their GPUs in order to use certain features. AMD's FSR feature is available across all GPU vendors.

Even though the community has come up with workarounds for using technologies like [DLSS](https://linuxgamingcentral.com/posts/dlss-unlocker-for-various-games/) and [GameStream](https://linuxgamingcentral.com/posts/setting-up-nvidia-gamestream-on-deck/) outside of NVIDIA GPUs, the fact that NVIDIA tries to make this a lock-in feature in the first place disgusts me.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/6700xt/crash4.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

# No Ads When Installing Drivers
Okay, this is more so a Windows issue than it is Linux. But last time I used Windows, I could *not* use GeForce Experience without [the need to have an account and logged in](https://www.pcworld.com/article/416353/nvidias-faster-better-geforce-experience-30-launches-with-mandatory-registration.html). Prior to this, no login was required. But NVIDIA decided that you need an account now for convenience' sake. So now you're forced to install a specific driver version in order to avoid having to log in.

![GeForce Experience login](/images/6700xt/gfe_login.png)
*Image credit: PCWorld*

Not only that, but when you do install the NVIDIA driver on Windows, you have ads while it's installing.

On Linux, this isn't necessarily a problem, as you will likely be installing the driver via the terminal or some sort of GUI. But still, this bugs me. Why see ads when you've already paid handsomely for a new GPU?

# Better Game Compatibility
I can only think of one example, but it's an example regardless. *Sonic Frontiers* plays *much* better on AMD on Linux in contrast to NVIDIA. The framerate is much higher, gameplay is more smooth, and there's little to no crashing. Originally I had suspected that it was due to the Denuvo DRM that was bottlenecking the GPU, but apparently it's due to the texture format. Someone had left a comment on the [Proton GitHub issue tracker](https://github.com/ValveSoftware/Proton/issues/6303#issuecomment-1345411130):
> There's a texture format it absolutely chokes on causing the slow down. The lead DXVK dev has said he can fix it on the DXVK side but it would take quite a bit of work. And since it shouldn't even be DXVK's job to fix we kinda just have to hope NVIDIA sees and fixes their driver.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/6700xt/frontiers_clip.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

Seems like [NVIDIA is aware of the issue](https://forums.developer.nvidia.com/t/driver-bug-unplayable-performance-in-sonic-frontiers/234873/3), but the fix "is in progress." So no ETA just yet.

# Wayland: Better Performance and Security
NVIDIA relies on X.Org for displaying graphics on Linux. X11 server development pace has just hit [a two-decade low](https://www.phoronix.com/news/XServer-2022-Development-Pace). I'm going to call this out: X.Org is abandonware at this point. No new features are being developed for it; it's just all maintainence now.

NVIDIA tries to work around this by using XWayland, which, according to the [Arch Wiki](https://wiki.archlinux.org/title/Wayland#XWayland), is "an X server that runs under Wayland and provides compatibility for native X11 applications that are yet to provide Wayland support." But notice:
- XWayland uses X as the display server, so it doesn't have Wayland's security features
- apparently there's "degraded performance" with XWayland on NVIDIA compared to X11
- some applications may not work on XWayland due to it not being fully backward-compatible with X11

![Wayland vs. X.Org](/images/6700xt/wayland_vs_xorg.png)
*Image credit: Phoronix*

AMD adapts to newer technologies such as Wayland to offer ["better performance, code maintainability, and security."](https://en.wikipedia.org/wiki/Wayland_(protocol)#Differences_between_Wayland_and_X) Wayland still has a ways to go before it becomes a "true" successor to X11, but even now, it has become quite mature. In fact, [games run via Wayland perform only slightly worse compared to X.Org](https://www.phoronix.com/review/nvidia-510-wayland/2). Since Phoronix benchmarked this almost a year ago, for all we know Wayland could do even better now!

# Disadvantages
Of course, there is *always* the flip side of the coin. It's not all advantageous when switching to AMD on Linux. One issue in particular is regards to some games that are a little...crash-y. As I had alluded to in my [Nobara impressions](https://linuxgamingcentral.com/posts/nobara-project-impressions/) article, *Crisis Core* remake crashes at random. There's a variety of factors that come into play, but I have a feeling it has to do with having the latest mesa-git Vulkan drivers. I should try downgrading to the latest stable Vulkan drivers and see if that makes a difference.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/6700xt/sackboy.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

# Other Notes
I was going to make the comment that on AMD, you can't use GPU encoding while video editing. Turns out you *can*, at least on Nobara Project. With Shotcut, I was able to export a 1080p/60 FPS, 25-second clip with GPU encoding enabled. Took 10 seconds. On the other hand, exporting the same clip *without* GPU encoding took 21 seconds. The file size difference is pretty big; the GPU encoded video is 79.8 MB. The clip without GPU encoding is just 34.9 MB. Still, it appears I can export videos faster with GPU encoding enabled. I wonder if Nobara has [AV1](https://www.phoronix.com/news/VP9-AV1-Vulkan-2023) enabled. Because I'm pretty sure GPU encoding on AMD actually takes *longer* than just using the CPU.

![Exporting a video with Shotcut - GPU encoding vs. CPU encoding](/images/6700xt/shotcut.webp)

If you were looking for some benchmarks, well, I'm sorry to disappoint: I don't have them here. But I will say upgrading to the 6700 XT was a *huge* jump from the 1660 Super. I'm clocking well over 120 FPS on *Crisis Core* remake on the highest settings, at 1080p resolution upscaled to 1440p with FSR. *High on Life* gets around 90 FPS on the highest settings at 1080p, upscaled with FSR. I'm wondering if the performance is bottlenecked a bit with my older CPU, which is a i7-9700K.

According to CoreCtrl, the max power wattage of the card is 186 W...is this normal? I think the card is supposed to use a higher wattage than that...although I have not been able to confirm this. The product page for the card doesn't mention the power consumption it uses.

![CoreCtrl - GPU only using 186 W max](/images/6700xt/corectrl.png)

# AMD is the Way to Go on Linux
Intel ARC, as I had alluded to earlier, is making better and better progress as the kernel and the Mesa graphics driver stack continues to mature (the A770 is roughly the equivalent of a 6600). NVK, in a few years' time, might actually make open-source gaming on NVIDIA possible. But for now, if you're a Linux gamer, I strongly suggest going with AMD, for the reasons I've listed above (why do you think Valve went with AMD for the Deck?).

**TL;DR**

The good:
- open-source graphics drivers that are actively maintained, contributed, and funded
- issues with graphics drivers can be worked on as soon as possible since they're open-source
- no need to install graphics drivers post-installation of a distro
- better game compatibility
- better security with the adoption of Wayland as the display server
- a nice boost in performance compared to the 1660 Super
- AMD doesn't try to lock you in to their GPUs for certain features, such as FSR

The not-so-good:
- some games tend to crash for X, Y, or Z reason; likely due to bleeding-edge Mesa drivers

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
