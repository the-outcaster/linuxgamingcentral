+++
title = "Turn Your Steam Deck OLED Into a Buttery-Smooth 120 Hz Machine With This Script"
date = 2023-11-29T16:05:36Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck_oled/guides/refresh_rate_boost/cover.jpg"
tags = ["guide", "steam deck", "steam deck oled", "overclocking"]
keywords = ["steam deck", "steam deck oled", "steam deck oled 120 hz", "steam deck faster refresh rate"]
description = "LCD models are also compatible with this script to run at 70 Hz."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Not satisfied with the Deck OLED's 90 Hz refresh rate? Turns out, depending on the type of display it has, you can upgrade the refresh rate to 120 Hz by running a simple [script](https://git.spec.cat/Nyaaori/deck-refresh-rate-expander). Even LCD users can benefit from this script -- it will overclock the refresh rate on said displays to 70 Hz. It's actually been quite nice with *Overwatch 2*, at low settings with 1024 x 768 resolution. But primarily 2D games will benefit from this the most, since the Deck's APU generally isn't powerful enough to render more-demanding titles past 90 FPS.

# Disclaimer
This guide assumes that you're using SteamOS 3.5.7 stable. I have not tested this on the Preview branch. Please be advised, however, that **if you run this script without having the proper display, you can potentially ruin your display.** One user on [r/SteamDeck](https://www.reddit.com/r/SteamDeck/comments/185qpx5/comment/kb3mql8/?utm_source=share&utm_medium=web2x&context=3) reported that "everything becomes completely garbled at 100 Hz" on the Samsung display (you might be able to get away with 98 or 99 Hz though). I am not responsible if anyone gets their display messed up.

# Find Out the Panel Manufacturer
The Steam Deck OLED comes in one of two flavors with the display: it's either from BOE ([Beijing Oriental Electronics](https://en.wikipedia.org/wiki/BOE_Technology)) or Samsung. This script is compatible with BOE (which I have personally tested and confirmed on my own unit). If it's from Samsung, I would advise against using the script, at least for now.

To find out what display you're using, go to Desktop Mode and run the following command in the terminal:

`cat /sys/class/drm/card0-eDP-1/edid | hexdump -C`

Pay attention to the first row. Take note of the **third number** on the right-hand side of the row. This will tell you what display you have:
- 01: BOE LCD display
- 02: No longer used
- 03: Samsung OLED
- 04: BOE OLED

![Display type on Steam Deck OLED](/images/steam_deck_oled/guides/refresh_rate_boost/cat.jpg)

As you can see here, it says 04 on my end. I therefore have the BOE OLED screen and can safely run this script without issue.

# Download and Install the Script
From here, the instructions are fairly simple. While your terminal window is still open, run the following commands:

```
git clone https://git.spec.cat/Nyaaori/deck-refresh-rate-expander.git
cd deck-refresh-rate-expander
sudo bash install-rre.sh
```

That's it! Just go back to Game Mode and you should now be able to push the refresh rate up to 120 Hz (make sure the unified frame rate management is toggled on in Settings -> Display). No restart should be required.

One caveat to this, if you push the refresh rate anything past 109 Hz, the colors on the screen become more "dull." You can (maybe) see this demonstrated here with my crappy phone camera (I recommend opening the image up in a new tab):

![Gamma comparison at 90 Hz vs. 120 Hz with Fraymakers](/images/steam_deck_oled/guides/refresh_rate_boost/gamma_comparison.jpg)

Also keep in mind that obviously a higher refresh rate is going to come at the cost of increased battery consumption.

# What to do if the Script Breaks your Display
Don't lose all hope. There should be a couple of different options at your disposal. One is by re-formatting your SSD with the [Steam Deck recovery image](https://help.steampowered.com/en/faqs/view/1b71-edf2-eb6d-2bb3). Keep in mind you will lose all your data on the drive, so if you have anything valuable on it, back the files up first.

If you'd rather not do something so drastic, Nyaaori, author of the script, [recommends](https://www.reddit.com/r/SteamDeck/comments/185qpx5/comment/kb3n61r/?utm_source=share&utm_medium=web2x&context=3) setting the refresh rate down to 98 or 99 Hz. You may have to connect an external display if you can't see the screen at all. If that doesn't work, change the SteamOS branch. Yet, if *that* doesn't work, unlock the filesystem in Desktop Mode with `sudo steamos-readonly disable`, move `/usr/bin/gamescope.orig` back to `/usr/bin/gamescope`, then re-enable read-only mode with `sudo steamos-readonly enable`.

Now if only someone could get VRR running...

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
