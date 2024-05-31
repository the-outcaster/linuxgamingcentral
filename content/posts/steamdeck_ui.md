+++
title = "You Don't Need the Steam Deck to Use the New UI"
date = 2022-03-08T16:15:30-05:00
author = "Mark Dougherty"
authorTwitter = "" #do not include @
cover = ""
tags = ["steam deck", "deck ui"]
keywords = ["steam deck", "deck ui", "desktop"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
I'm sure most of you reading this post are aware of the new SteamOS 3.0 that's shipping by default with the Steam Deck, with that much-needed interface overhaul for Big Picture Mode (also, it's Valve's first product to hit the number 3). Well, thanks to Reddit user **GB_2_**, [it's possible to use the new Deck UI across any Windows or Linux desktop](https://www.reddit.com/r/SteamDeck/comments/t57l4t/how_to_get_the_steam_deck_ui_on_windowsany_linux/?utm_source=share&utm_medium=web2x&context=3). For Linux, all you literally have to do is:
1. Navigate to `~/.steam/steam/package`
2. Create a file named `beta` if it's not already there. Replace it's contents with `steampal_stable_9a24a2bf68596b860cb6710d9ea307a76c29a04d`
3. Save the file and close it. Launch Steam via the terminal with the `-gamepadui` argument

![great on deck](/images/deckui/great_on_deck.png)

Seems like it's a pretty similar process on Windows as well.

It's possible to do this on ChimeraOS as well; **alkazar82** added [instructions](https://www.reddit.com/r/SteamDeck/comments/t57l4t/comment/hz56te3/?utm_source=share&utm_medium=web2x&context=3) on that Reddit post. It's neat to see that UI for a living room TV. Combined with the Xbox 360-like sounds, it really does feel like a console.

[![chimeraos with deck ui living room TV](https://img.youtube.com/vi/ebldZ2uk-z4/0.jpg)](https://youtu.be/ebldZ2uk-z4 "ChimeraOS With Deck UI")

On my desktop with NVIDIA the Deck UI semi-works. It launches, with the nice Steam logo at boot time, but navigating across the menus is very laggy. Most of the games I tried launching just didn't work. The game would apparently be running but it just wouldn't display on the screen. Only successful game that I've tried was *Them's Fightin' Herds*. Not even *Portal 2* ran. And I have to force exit Steam through my system monitor when I want to close it. There's probably a reason why it's not officially available just yet.

![deck ui on gpd win 3](/images/deckui/gpd.jpg)

On my GPD Win 3, navigation across different menu items is very smooth, and *Hades* launched just fine. *Sonic Mania* hanged on the launching screen.

Some other screenshots on my desktop client:

![controller input screen](/images/deckui/controller_input.png)

![keyboard](/images/deckui/keyboard.png)

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
