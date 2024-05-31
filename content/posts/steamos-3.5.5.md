+++
title = "SteamOS 3.5.5: The Biggest Steam Deck Update of the Year!"
date = 2023-11-17T04:25:49Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steamos/3.5.5/cover.jpg"
tags = ["news", "software update", "steam deck", "steamos", "stable"]
keywords = ["steamos 3.5.5", "steamos 3.5", "steam deck oled", "steam deck hdr", "steam deck vrr", "steam deck dock", "steam deck undervolting", "mesa", "arch linux"]
description = "Display color adjustments, HDR, VRR, undervolting controls, updated Arch base..."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Almost as soon as I wrote my previous post regarding the latest [Steam Deck client update](https://linuxgamingcentral.com/posts/steam-deck-client-update-11-16-2023/) I was eating my own words regarding the availability of SteamOS 3.5 as stable. It's available NOW, just in time for Deck OLED users, and, were I to cover every single change from the last SteamOS update, this post would stretch for a mile.

First, **the [color rendering has been adjusted to emulate the sRGB color range](https://linuxgamingcentral.com/posts/steamos-3.5-getting-improved-color-management/).** According to the patch notes, this will result "in a slightly warmer and more vibrant color appearance." You can tweak this back to the native color render, or boost the sRGB for more saturated colors. Guess we can say goodbye to the [vibrantDeck plugin](https://linuxgamingcentral.com/posts/vibrantdeck/). Color temperature can also be adjusted to a more cooler, blue hue or a warmer orange tint.

![Changing display colors](/images/steamos/3.5.5/display_colors.jpg)

**HDR and VRR can now be enabled via a toggle in the QAM, provided that the connected external display supports these options.** The official Steam Deck dock also gets updated firmware to support VRR. HDR visualization can be adjusted to waveform/color gamut, heatmap, heatmap extended, and heatmap classic.

![HDR visualization option](/images/steamos/3.5.5/hdr_visualization.jpg)

In the QAM, **scaling modes have been separated from the filtering options. Stretch and Zoom (Fill?) scaling modes are now available.** Got that game that only allows 16:9? Well, thankfully you can fill the black borders at the top and bottom of the screen with the Stretch option.

![New scaling modes and filters](/images/steamos/3.5.5/scaling_options.jpg)

It's not mentioned in the patch notes, but **the frame rate limiter and refresh rate sliders have been combined into one.** You can separate them again under Settings -> Display -> Advanced -> Enable Unified Frame Limit Management. Another thing not mentioned in the patch notes, is **a new scaling filter option has been added: NIS (NVIDIA Image Scaling).** The shaprness level can be adjusted anywhere from 0 to 10. Personally, I find it to be a little better than FSR, as the sharpness is more, well, *sharp*.

![Frame rate limit and refresh rate options combined](/images/steamos/3.5.5/frame_limit.jpg)

**Support for the Deck OLED has been added.**

**External media, such as MicroSD cards, are now automatically mounted as soon as they're connected. External media can also be formatted and/or managed directly through Steam's interface.**

![Format SD card option](/images/steamos/3.5.5/sdcard_format.jpg)

![Manage SD card storage](/images/steamos/3.5.5/sdcard_in_storage_settings.jpg)

Mesa has been updated to [23.1.3](https://linuxgamingcentral.com/posts/mesa-23.1/). Some games may get their **shader cache size reduced [by up to 60%](https://linuxgamingcentral.com/posts/steam-deck-getting-smaller-shader-cache/)** with this update. The `VK_EXT_graphics_pipeline_library` extension is now enabled by default, which, apparently, **[improves game load times and reduces graphical stutter](https://linuxgamingcentral.com/posts/shader-compilation-improved-with-mesa-23.1/).** The patch notes for the update also mention improved performance with *Starfield*, and fixed "viewmodel corruption" and "launch failures" in a few other titles.

With the updated firmware, version 118, **you can now [undervolt the CPU, GPU, and the SoC](https://linuxgamingcentral.com/posts/steam-deck-undervolting/) via the BIOS menu.** Based on my testing I've seen some marginal improvements as far as battery life with AAA titles, although indie games that aren't going to peg the Deck's APU are going to see an even shorter battery life.

![Steam Deck undervolting options in BIOS](/images/steam_deck/voltage_comparison/undervoltage_settings.jpg)

A critical bug was fixed: **there should no longer be "severe CPU performance issues" while SMT is enabled.**

And, thank God, **the Arch base has finally, *finally* been updated,** including the kernel itself. Kernel 5.13 is now dead and has been replaced with the more recent [6.1 LTS release](https://linuxgamingcentral.com/posts/kernel-6.1-released/). Particular improvements to this kernel update include bug fixes and performance improvements with ext4, huge Btrfs performance improvements, Wi-Fi 7 support, and better support for third-party Nintendo gamepads. KDE Plasma has also been updated to [5.27.5](https://kde.org/announcements/plasma/5/5.27.0//).

**EDIT (11-17-2023):** you should also be able to install [Nix packages](https://linuxgamingcentral.com/posts/steamos-getting-nix-support/)!

Some other minor improvements:
- Bluetooth connection stability, particularly when multiple gamepads are connected, has been improved, as well as improved sleep/resume speed
- Latency and stutter when there are multiple overlays on screen has been reduced, since "compositing is now avoided in additional scenarios." Latency in regards to applications rendering slower than the display's refresh rate have also been improved
- improved fade transitions between apps
- MangoHUD can now be customized via the `presets.conf` file found in `~/.config/MangoHud/`. The [MangoPeel plugin](https://github.com/Gawah/MangoPeel) can also be used to customize it via the QAM
- controller bindings and M+K bindings can be swapped by holding down Options in the "Linux hid-steam driver"

And other fixes:
- internal display backlight shouldn't always stay on
- touchscreen orientation when an external display is connected
- some games could appear stretched if their window size didn't match their swapchain size
- *Disgaea* no longer needs to be "tapped on" before input works
- physical dimensions being reported to games with the incorrect aspect ratio
- workaround for tearing causing heavy stuttering when MangoHUD was enabled -- tearing now "impossible in such situations"
- keyboard input should now work for *Overwatch 2*
- thumbstick touch sensors should no longer lose touch periodically

See the full patch notes on [Steam](https://store.steampowered.com/news/app/1675200/view/5484882897552407488).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
