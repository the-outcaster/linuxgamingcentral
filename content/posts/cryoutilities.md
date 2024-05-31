+++
title = "Increase Steam Deck Performance with CryoUtilities"
date = 2022-12-05T11:04:37-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/cryoutilities/fh5.png"
tags = ["guide", "steam deck", "cryoutilities"]
keywords = ["steam deck", "cryoutilities"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
There's an incredible script that allows you to increase the Deck's performance by modifying the swap file size, changing the swappiness value, and/or enabling TRIM on the SSD. This is all thanks to [CryoByte33](https://www.youtube.com/@cryobyte33), a YouTuber who definitely knows his stuff when it comes to the Deck and increasing the performance of it wherever possible.

With his [script](https://github.com/CryoByte33/steam-deck-utilities), you can:
- increase or decrease swap file size
- change the swappiness (or swap tendancy) value
- enable or disable [TRIM](https://en.wikipedia.org/wiki/Trim_(computing)) -- basically extends the longevity of your SSD

# What are the Benefits of CryoUtilities?
By default, SteamOS uses 1 GB swap, and a value of 100 for swappiness. This means 1) if the Deck runs out of RAM, it only has 1 GB of swap to use, and 2) with a swappiness value of 100, the Deck will *always* prefer the swap over the physical RAM, giving the device a performance bottleneck since again, it only has 1 GB of swap space.

When we increase the swap file size, and change the swappiness value, we can potentially get FPS boosts depending on the game being played. [*Sonic Frontiers*](https://linuxgamingcentral.com/posts/sonic-frontiers-on-deck-best-settings/) is an example of a game that plays better with 8 GB swap with a swappiness of 50. My friend Matthew Anderson reported that *New World* "dramatically benefits" from a 16 GB swap file with swappiness of 1. He mentioned "the game flat out crashes in busy areas without the swap increased from the default 1 GB." Also apparently there are crashes after trying to login without the swap file increase.

But don't just take our word for it. CryoByte33 has plenty of videos going over the performance differences with specific games with the default settings, with 4 GB VRAM, with and without the swap file increase/swappiness changed:
- [*Horizon Zero Dawn*](https://www.youtube.com/watch?v=xx9sf47sB9o)
- [Nintendo Switch emulation](https://www.youtube.com/watch?v=0__el4VrTVY)
- [*Forza Horizon 5*](https://www.youtube.com/watch?v=pceOIAGYdbM)

You can also check [this](https://www.youtube.com/watch?v=od9_a1QQQns) video out for a detailed overview of what the CryoUtilities script does.

According to the [GitHub FAQ](https://github.com/CryoByte33/steam-deck-utilities#common-questions), "any game that uses a combined 16 GB for RAM and VRAM will likely benefit from the swap fix." Even emulating games from later generations like Nintendo Switch, PS3, and Wii U will see performance improvements. Changing the swap file size/tendancy *might* be reverted on SteamOS updates; it did for me when I updated to SteamOS 3.4. But the changes should survive with Deck client updates.

# How to Use
Go to Desktop Mode on your Deck. There's one of two ways to install. One way is by cloning the script repo:

```
git clone https://github.com/CryoByte33/steam-deck-utilities.git
cd steam-deck-utilities
chmod +x cryo_utilities.sh
./cryo_utilities.sh
```

Alternatively you can go to the [GitHub page](https://github.com/CryoByte33/steam-deck-utilities), right-click "this link" under the Install section, click "Save As...", save the file, then run it. This will add the script as a desktop icon that you can easily access, and you'll also have a update icon and a uninstall icon. 

Run it, and you'll have a nice interface for changing various settings.

First, after the disclaimer window, you'll be asked what to change the swap size to. Again, by default it's set to 1 GB. Cryo recommends 16 GB. I've been able to safely get away with 8 GB, so if you're running low on hard drive space, you can use this instead. But you might see even better performance with 16 GB, so go with that if you can.

![CryoUtilities set swap size](/images/steam_deck/cryoutilities/set_swap_size.jpg)

Give it a few minutes. Next, you'll be asked what the swap tendancy should be. By default, it should be 100. Cryo recommends setting the value to 1. You could set it to 50 to make the Deck balance the use of swap and RAM. Setting it to 1 will make the Deck always prefer the RAM over the swap. So you may want to experiment with this a little. But set it to 1 for now, per Cryo's recommendation.

![CryoUtilities set swappiness value](/images/steam_deck/cryoutilities/swappiness.jpg)

If you're on the SteamOS 3.4 preview, you won't need to proceed to the next step, since TRIM is already enabled by default with this build. If you're using the stable build of SteamOS, I definitely recommend enabling TRIM to extend your SSD's life span. Again, give it a few minutes. Reboot the Deck and you should be all set.

You might want to increase the UMA frame buffer size to 4 GB in conjunction with this script. To do so, go to your Deck's BIOS, and increase the UMA frame buffer size from the default 1 GB to 4 GB. As a reminder, to get access to the BIOS, hold the Volume+ button while turning the Deck on. Let go once you hear the chime. Go to "Setup Utility," then go to "Advanced". Now that you have more swap space, you won't have to worry about having less physical RAM with this change.

![Increasing VRAM size on Deck](/images/steam_deck/photos/steam_deck_uma_size.jpg)

# How to Revert to Default Settings
In the event you don't like your new settings for some reason, you can always revert back to the default values that SteamOS has set. Run the script again, and set the options to the following:
- swap size to 1 GB
- swappiness to 100
- disable TRIM

*Cover image credit: CryoByte33*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
