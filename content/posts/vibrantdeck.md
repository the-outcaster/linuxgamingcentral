+++
title = "Forget about Steam Deck OLED; Use VibrantDeck Instead"
date = 2023-03-15T18:51:01Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/plugins/vibrantdeck/cover.jpg"
tags = ["steam deck", "steam deck plugin", "vibrantdeck"]
keywords = ["vibrantdeck", "steam deck oled", "steam deck", "steam deck screen saturation"]
description = "Great plugin to use if you aren't already using it!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
**EDIT (11-30-2023): this plugin has basically become outdated since [SteamOS 3.5.5](https://linuxgamingcentral.com/posts/steamos-3.5.5/). Controlling the saturation is now possible directly through Steam itself.**

So Pierre-Loup Griffais -- according to PCGamer -- says Valve [has thought about making an OLED model of the Deck](https://www.pcgamer.com/valve-likes-the-idea-of-an-oled-steam-deck-too-but-says-it-isnt-as-simple-as-it-sounds/), but the idea of putting one in is a bit more cumbersome than it sounds.

Well, even if Valve did make one eventually, there's a fast, easy, and inexpensive solution in the meantime. [vibrantDeck](https://github.com/libvibrant/vibrantDeck). This is a Steam Deck plugin that allows the user to adjust screen saturation. The term that you'll hear a lot of people use is "pop" -- this is the case when it comes to the color quality on the screen when this plugin is enabled. The plugin is open-source and very easy to install and use.

![vibrantDeck](/images/steam_deck/plugins/vibrantdeck/vibrantdeck.jpeg)

I would assume most Deck users at this point have [Decky Loader](https://github.com/SteamDeckHomebrew/decky-loader) installed. If that's not the case, go to Desktop Mode on Deck, direct your web browser to the Decky Loader GitHub page, and click the Download button. After that's installed you can use the little shopping icon on the top-right of the QAM in Game Mode and install vibrantDeck from there.

At that point, go to vibrantDeck from the QAM, and set the toggle to "Enable color settings". Colors on the screen should already look much better. By default the saturation quality is set to 200. Often this is a good number to start with, but some games might benefit even further by setting it to 300. 400 is the max -- I don't recommend that; the screen is way too saturated at that point. You can adjust the slider to your liking.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/vibrantdeck/vibrantdeck.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

In addition to saturation quality, you can further tweak the colors by adjusting the RGB gamma. Each slider is set to 100 by default. I don't really recommend adjusting these sliders, unless you want a more specific shade of color applied to the screen. You can have even more fine-tuned tweaking by enabling the Linear Gamma Gain toggle.

A great thing is, like Steam's performance settings, you can set the saturation levels on a per-game basis. So, if you want a saturation level of 100 for one game, and 300 for another, go for it. If you want one game to look more green than the other, the power is in your fingertips.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
