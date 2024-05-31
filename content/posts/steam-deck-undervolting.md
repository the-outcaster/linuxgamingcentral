+++
title = "Undervolting the Steam Deck: Is It Worth It?"
date = 2023-10-19T18:29:40Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/voltage_comparison/witchfire_voltage_comparison.jpg"
tags = ["guide", "steam deck", "undervolting"]
keywords = ["steam deck", "steam deck undervolting", "undervolting", "steamos preview 3.5.1", "steam deck firmware 118", "witchfire", "fraymakers"]
description = "Are there actually benefits to APU temps and battery life?"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Last week's SteamOS 3.5.1 preview update [added undervolting controls](https://store.steampowered.com/news/app/1675200/view/3747614808335925159) with the updated firmware via the BIOS. Undervolting the Deck was already possible with a tool like the [Smokeless UMAF BIOS flasher](https://github.com/DavidS95/Smokeless_UMAF), but now it's been made even easier. Simply access the Deck's BIOS by holding the Volume Up button when turning it on, going to Setup Utility, and adjusting the appropriate options under the "Advanced" tab. Of course, you'll currently need to be opted into the "Preview" branch on Steam in the System Settings tab in order to have access to these controls.

The following components can be undervolted, all the way down to -50mV:
- CPU
- GPU
- SoC

Supposedly, undervolting the Deck means [increased battery life](https://steamdeckhq.com/news/undervolting-and-overclocking-push-your-steam-deck-beyond-its-limits/), while still retaining the same performance. It also results in a [slightly cooler CPU and GPU temperature](https://www.youtube.com/watch?v=Roi6lvrcH-I). I tried to put this theory to the test by running a few games with the Deck at stock voltage, and at a lower voltage rate. I got mixed results. In some cases, the Deck *did* get a slightly longer-lasting battery. In other cases, however, the battery was even shorter.

![Undervoltage settings in Deck BIOS](/images/steam_deck/voltage_comparison/undervoltage_settings.jpg)

Note that, in most cases, you're not going to want to go all the way down to -50mV. I did so myself and discovered my games experienced random crashing. After the Deck rebooted, I started noticing visual artifacts in the Heroic Games Launcher. So, I bumped everything up to -40mV, and haven't noticed any issues so far.

In your case, you're going to just need to be patient and gradually lower each value by -10mV, until you actually start to notice the random game crashing or the visual artifacting. Each Deck is different, due to the ["silicon lottery."](https://steamdeckhq.com/news/undervolting-and-overclocking-push-your-steam-deck-beyond-its-limits/) So keep at it until you find the right values.

Note that, in the event your Deck will no longer boot, you can reset the CMOS to the default settings. With the Deck off, hold down the Volume Down button, the QAM button, and the power button. This should reset the voltage settings back to 0mV.

# Test Results
The first game I tested was [*Witchfire*](https://linuxgamingcentral.com/posts/witchfire-review/). Settings are as follows:
- 1152 x 720 resolution, upscaled with NIS set to a sharpness value of 5
- Medium graphics settings
- 50% brightness and audio volume
- Wi-Fi and Bluetooth off
- 12 W TDP
- 1200 MHz max GPU clock speed
- Proton 8.0-4
- refresh rate set to 40 Hz
- 8 GB swap with swap tendancy set to 50
- 4 GB UMA frame buffer size

On stock voltage the Deck lasted **two hours and 10 minutes.** In the same area in the game, with everything undervolted to -40mV, the game lasted ten minutes longer at **two hours and 20 minutes.** The GPU was one degree cooler, and the CPU two degrees cooler. Battery consumption is one watt less, and the fan speed is slightly slower by about 200 RPMs. So, in that case, the undervoltage was a winner.

(Note: you may want to open the image in a new tab to get a better glimpse of the stats.)

![Witchfire voltage comparison](/images/steam_deck/voltage_comparison/witchfire_voltage_comparison.jpg)

However, things were a little different when I tested [*Fraymakers*](https://linuxgamingcentral.com/posts/fraymakers-quick-thoughts/), a native 2D Linux title. Settings were as follows:
- native resolution
- 50% brightness and audio volume
- Wi-Fi and Bluetooth off
- 3 W TDP
- 200 MHz max GPU clock speed
- FPS set to 60
- 8 GB swap with swap tendancy set to 50
- 4 GB UMA frame buffer size

With stock voltage, the game lasted **six hours and 33 minutes.** With undervolting applied, the battery lasted **six hours and 21 minutes.** The CPU and GPU were significantly cooler by nearly ten degrees Celcius, but other than that the stats remained largely the same. A bit of a headscratcher there. I'll need to do some more testing with more games.

![Fraymakers voltage comparison](/images/steam_deck/voltage_comparison/fraymakers_voltage_comparison.jpg)

# Concluding Thoughts...So Far
My testing has been brief so far, but based on these two games, your mileage may vary. Your CPU and GPU temps will go down a bit, that's for sure. As far as battery life, however, that's going to depend on the game, and for AAA-quality games, it's not going to be much of an improvement anyway. Add to that the risk that your Deck may experience random crashing or visual artifacting if you undervolt it too much.

If you've done some testing yourself, definitely let me know in the comments your results. I'm curious to see how far the silicon lottery has taken you and whether or not you've actually seen any benefits.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
