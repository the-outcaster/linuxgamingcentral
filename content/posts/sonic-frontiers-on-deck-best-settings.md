+++
title = "How to Get a Great Experience with Sonic Frontiers on Steam Deck"
date = 2022-11-08T17:01:04-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/frontiers.webp"
tags = ["guide", "steam deck", "sonic"]
keywords = ["steam deck", "sonic frontiers", "uma", "swap", "swappiness", "swap tendancy", "ge-proton", "trim", "cryoutilities", "gaming on linux", "steam deck hq", "dxvk", "dxvk async"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Worried about the "Unsupported" mark on the Steam store page for *Sonic Frontiers*? Bah, that's garbage. It runs out of the box with Proton 7.0-4 and GE-Proton. Though it's a somewhat barebones PC port, we have a few options at our disposal for the best optimized settings. I've got some [gameplay footage](https://www.youtube.com/watch?v=imX1MhjBxTM) running anywhere between 40-60 FPS, but there are spoilers there, so watch out for that.

After putting several hours into the game today on Deck, I've come across a few tweaks that I think you might like. GOL reported that the game [can't go beyond 30 FPS without light/shadow flickering](https://www.gamingonlinux.com/2022/11/sonic-frontiers-works-on-steam-deck-and-linux-desktop-although-it-has-issues/). I guess I'm one of the "lucky" few who managed to get the game past 30 FPS *without* the flickering. Even with the crappy Denuvo DRM slapped on top. Here's how I did it:
- set UMA frame buffer size to 4 GB
- set up 8 GB swap with 50 swappiness value
- using GE-Proton7-41
- resolution set to 1024 x 576
- windowed mode
- FSR filter set to 5
- refresh rate set to 40 Hz
- TDP limit set to 8 watts
- all graphics settings set to high, except shadows (set to low)

With these settings I get about **two-and-a-half hours of gameplay** on a full charge. Stays 40 FPS for the most part. Occasional dips to 38 or 39. I only tested briefly, but I could get away with **6 watts TDP at 30 FPS. Game didn't consume any more than 12 W. That would give you at least three hours of battery life.**

The game *can* technically reach 60 FPS at times, especially when playing the cyber space levels (presumably since there's far less data to load than a huge open-world map), but I don't recommend setting the framerate limit to this. Not unless you want to induce a migraine by observing the constant light flickering in-game.

![Stats for Sonic Frontiers running on Deck](/images/steam_deck/screenshots/frontiers_stats.jpeg)

Note that if you set the refresh rate to, say, 50 Hz, and the in-game framerate is lower than that, that's when the flickering happens. So it's important to **pick a framerate/refresh rate that's the same or lower than the average framerate that the game gets in your experience**. Setting it too high will cause said flickering.

While the game does list 1280 x 800 as a possible resolution, selecting it doesn't get rid of the black borders across the top and bottom of the screen. It's not possible to change the aspect ratio.

**Setting the shadows to low is a particularly important step.** Not only will this significantly reduce the flickering, but it will also give the game a *massive* framerate boost. Like, a 10-15 FPS boost. And it honestly doesn't look that much different than when it's set to High.

Now you're probably curious about those first two bullet points I listed. "UMA set to 4 GB? How do I do that?" "8 GB swap? How?" Well, I've got your back.

# Set UMA to 4 GB
I covered this in my [*Halo Infinite* guide](https://linuxgamingcentral.com/posts/halo-infinite-on-deck-guide/), but basically, you'll need to access your Deck's BIOS and from there, change the UMA frame buffer size. By default it's 1 GB. We want to increase it to 4 GB.

The UMA is part of the Steam Deck’s RAM that is shared with the integrated graphics on the APU and acts as a temporary frame buffer during graphic intensive operations, such as gaming. Increasing this will increase the performance of the game, at the cost of less RAM. With the Steam Deck off, hold the Volume+ button, then press the Power button. When you hear the chime, release the Volume+ button. Navigate to “Setup Utility” with the D-pad, then press A. Under the “Advanced” category, select the “UMA Frame buffer Size” option, press A, then select “4G”. Exit the BIOS, making sure that your change is saved. The Deck should restart.

![Increasing UMA size on Deck](/images/steam_deck/photos/steam_deck_uma_size.jpg)

# Increase Swap Size to 8 GB
When we increase the UMA frame buffer size, we're also decreasing the amount of RAM available to the Deck, since the RAM and VRAM is shared. So when the UMA is set to 4 GB, that takes 4 GB of RAM away, leaving us with only 12 GB of usable RAM. To have more memory available, we can use swap space, though it's not as fast as RAM. By default, the Deck has only 1 GB of swap space set up. We can increase the size of this with [CryoUtilities](https://github.com/CryoByte33/steam-deck-utilities). 

I won't get into what this script does now; that will be for a future article. But with it, we can increase swap size. Follow the instructions in the README to get set up. On the first step, you'll be asked how much swap space you want. Ideally you want to have 8 GB if you have the space. 16/32 GB is a little overkill. If you can't have 8 GB, try going with 4 GB.

![Changing swap size on Deck](/images/steam_deck/cryoutilities/set_swap_size.jpg)

Then, set the swappiness value to 50. Swapiness defines how likely the system will make use of the swap space. By default it's 100 (or it might be 60, if you're on the stable branch). At 100, the Deck will almost always use swap instead of RAM. At 1, the Deck will use the onboard RAM a lot more likely than the swap. We want to make this a balance of both, so set it to 50.

![Changing swappiness on Deck](/images/steam_deck/cryoutilities/swappiness.jpg)

The last step of the script will ask if you want to enable [TRIM](https://en.wikipedia.org/wiki/Trim_(computing)). I'd recommend doing so to extend the longevity of your SSD.

![Enabling TRIM on Deck](/images/steam_deck/cryoutilities/trim.jpg)

# Change In-game Settings
Other than those big steps you should now be ready to change the in-game settings. Lower the resolution, keep it in windowed mode so GE-Proton can make use of FSR (I noticed FSR is set to "OFF" in MangoHUD if the game is in fullscreen or borderless), then lower the refresh rate to 40 Hz. Make sure to turn shadows to low. Based on my testing so far I've been able to lower the TDP to 8 watts while keeping a smooth 40 FPS. You can turn it down to 6 W and set the maximum framerate to 30 FPS as well, depending on what you want to trade for battery life and performance.

GOL recommends using `DXVK_ASYNC` for faster shader compilation, but this increases shader size. You can use this with GE-Proton by adding this as a launch parameter:

`DXVK_ASYNC=1 %command%`

But note I have not personally tested this. I haven't had much stuttering in my experience, at least after the initial couple of minutes of being in-game.

[Steam Deck HQ](https://linuxgamingcentral.com/posts/interview-with-noah-from-steam-deck-hq/) will likely have a more detailed report in the next few days, so stay tuned for that. In the meantime you can always refer to this for the best settings. I also wrote a [review](https://linuxgamingcentral.com/posts/sonic-frontiers-review/) on the game.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
