+++
title = "Steam Deck - Battery Saving Tips"
date = 2023-02-03T15:51:00Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/guides/powertools/cover.jpg"
tags = ["guide", "steam deck", "battery", "decky loader", "powertools"]
keywords = ["powertools steam deck", "powertools", "powertools steam deck plugin", "steam deck battery saver"]
description = "Tired of the Deck's poor battery life? There are ways to work around that."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Yesterday I put out a [video](https://www.youtube.com/watch?v=U7l4xMG-tmk) going over the many ways to keep your Deck staying on as long as possible. Below is the transcript -- slightly modified, of course -- if you prefer your guides in text format.

Let's face it: battery life on the Steam Deck, without changing any of the power settings, is short. But we have a lot of tools at our disposal so that we can get the most out of it.

While disabling Wi-Fi and decreasing brightness are a few ways to get more juice, we can also limit the thermal design power (or [TDP](https://en.wikipedia.org/wiki/Thermal_design_power)), keep the GPU and CPU speed from going higher than necessary, make use of FSR to decrease the resolution while retaining much of the same graphics quality, limit the framerate, park CPU threads that we don't need, and even force RAM into low-power mode.

# Install Decky Loader and the PowerTools Plugin
So, the first thing we'll need to do is install [Decky Loader](https://github.com/SteamDeckHomebrew/decky-loader). Decky Loader is a homebrew plugin launcher for the Steam Deck. With it, we can install plugins such as PowerTools to increase the number of ways in which we can preserve battery life. Installation of Decky Loader is very simple; just head to the GitHub page with your web browser in Desktop Mode, and click the Download button.

![Decky Loader GitHub page](/images/steam_deck/guides/powertools/decky_loader_github_page.webp)

After that is installed, go back to Game Mode. You should have an additional icon in the Quick Access Menu that looks like a plug. Navigate to it, then select the shop icon on the top-right. From there, look for PowerTools and select "Install". [PowerTools](https://github.com/NGnius/PowerTools) will allow us to enable or disable simultaneous multithreading (or [SMT](https://en.wikipedia.org/wiki/Simultaneous_multithreading)), park CPU threads, limit the CPU frequency, and downclock the system's memory.

![Decky Loader](/images/steam_deck/guides/powertools/decky_loader.jpeg)

# Lower Resolution, if Possible
Launch a game. In this guide, I will be demonstrating [*Spongebob: Cosmic Shake*](https://linuxgamingcentral.com/posts/spongebob-cosmic-shake-review/). In the game's video settings, lower the resolution if possible. Note that some resolutions may not rescale themselves to fit the entire screen. So I will set the resolution to 1152 x 720. **Turning vsync on** will also help.

![Lowering in-game resolution](/images/steam_deck/guides/powertools/resolution.jpeg)

# Use FSR Filtering
Open the QAM. Under the Performance tab, **set the overlay level to 4**, so we can keep an eye on GPU/CPU frequency, whether FSR is enabled or not, and the line graph. Enable Advanced View if you don't already have that selected. Toggle "use per-game profile" so that we can customize the performance settings for each individual game.

Scroll down to the scaling filter option. **Set the filter to FSR.** Adjust the FSR sharpness as needed. I personally prefer 3 to get a good balance between sharp, but not *too* sharp. FSR should display "ON" in the performance overlay. If it doesn't, go back to the game's video settings and change the screen mode, and lower the resolution if there's one that's lower than 1280 x 800, or 1280 x 720.

![Turning scaling filter to FSR](/images/steam_deck/guides/powertools/fsr_filter.jpeg)

# Adjust Framerate/Refresh Rate, TDP, and GPU Clock Frequency
If you can withstand 30 FPS, you can set this as the framerate limit. I personally find 30 FPS too headache-inducing, so I prefer to **set the refresh rate to 40 Hz.** 40 Hz, or FPS, to me, is the perfect compromise between 30 and 60 FPS, between having a relatively smooth framerate while keeping the power usage down.

**Toggle the TDP limit.** From here you can use the slider to decrease the number of watts used. Gradually lower the TDP, one watt at a time, and carefully observe the framerate and graph on the performance overlay. If the framerate remains at a consistent 40 FPS (or 30, if you chose this), and the line graph is mostly flat, you can keep decreasing the TDP until the framerate and line graph starts to dip. If it dips too frequently, increase the TDP until you can find the right balance. Keep in mind you may need to keep adjusting this number depending on what's going on in the game. If there's a lot of objects or NPCs, the framerate may dip, so you'll want to set a more forgiving TDP limit.

![Adjusting TDP and GPU speed](/images/steam_deck/guides/powertools/tdp_and_gpu_freq.jpeg)

Take a look at the GPU clock frequency and carefully observe the number. Now **toggle manual GPU clock control** for more fine-tuned adjustment. Lower the slider until it's right around the number that you saw before. If you want, you can go down a little further than this, but you may experience stutter. Again, this depends on what's happening on screen. Use the framerate and line graph as a guide, just like with setting the TDP. Make sure the framerate remains a consistent 40 FPS and the line graph mostly stays flat. Occassional dips in either shouldn't be too much of a problem, but **if the dipping is constant, increase the GPU frequency**.

# PowerTools - Adjust the Number of CPU Threads, CPU Frequency, etc.
With PowerTools, we can fine-tune the battery life *even further*. Go to Decky Loader from the QAM, and from there, select PowerTools. **If you're playing an older game, or if you're playing an emulated game, disabling SMT can be quite useful** as far as performance benefits. However, the number of CPU threads available will be halved, so you may not want to disable this for modern AAA titles.

Just like with adjusting the TDP and GPU clock frequency, **gradually decrease the number of CPU threads**, while carefully observing the framerate and line graph. Again, make sure the framerate remains consistent, and the line graph stays mostly flat. With *Spongebob* I can technically set the number of threads to three, but there are some areas where the game stutters, so using four threads allows for a more consistent framerate.

![Adjusting the number of CPU threads and CPU frequency](/images/steam_deck/guides/powertools/powertools_settings.jpeg)

Observe the CPU clock frequency. **Toggle frequency limits**, and set the maximum speed to a number that's around the number that you saw before. In the case of Spongebob, I can set the max speed to 2,700 Hz and still get a consistent framerate. I can set the max speed even lower, but again, there will be certain areas in the game where the framerate can suffer, so I'll try to use a more forgiving speed to accomodate the more "busy" in-game scenes. Keep playing around with this number while observing the framerate and line graph, until you get a -- yup, you guessed it -- *consistent framerate*.

Finally, **provided that your framerate won't tank, you can toggle downclock memory**. This will force the Steam Deck's RAM into a low-power state. If the framerate is significantly lowered, however, it may be best to keep this toggle off.

# Play the Game and Make Adjustments as Needed
Play the game for a little bit. If there's too many frame dips, keep adjusting the various settings I mentioned in this guide until you get the right balance. Once you've settled with the right numbers, you can decrease the performance overlay level so your screen isn't so cluttered. **PowerTools settings will be reset if you restart your Steam Deck**, so if you want to save your settings across reboots, toggle persistent to on.

![In-game with Spongebob Cosmic Shake](/images/steam_deck/guides/powertools/in-game.jpeg)

One caveat with PowerTools is **the settings will be used globally and not on a per-game basis**. So you will need to keep adjusting the settings with each game that you play. Also, the "Default" button to restore the default settings doesn't seem to work, so keep that in mind.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
