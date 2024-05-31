+++
title = "Want To Upgrade Your Steam Deck's Resolution? You'll Need to Reflash Your BIOS"
date = 2023-07-17T14:14:18Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/weekly_news/7_8-14.jpg"
tags = ["news", "steam deck", "deckhd"]
keywords = ["deckhd", "steam deck", "steam deck resolution upgrade", "steam deck bios flash"]
description = "Upping the resolution and color quality might be nice, but there are a couple of \"gotchas\" to be aware of."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
As I had alluded to in yesterday's [weekly recap](https://linuxgamingcentral.com/posts/news-for-july-8-14/), it appears that, if you want to use the [DeckHD](https://deckhd.com/) -- a screen for the Steam Deck that upgrades the resolution to 1200p and provides better color quality -- in the fullest capacity, you'll need to flash your Deck's BIOS.

This wasn't something that the DeckHD team was upfront about. Only recently did a member of the team address this technical hurdle in the [DeckHD Discord](https://discord.gg/kZamUWKQUS):
> It is currently a 'must-do' procedure to flash the BIOS after installing the DeckHD screen on your Steam Deck. There are a couple [of] reasons for this, but mainly down to these three:

1. We need to flash the BIOS to adjust the configuration of the different chips on the motherboard.
2. Implement the correct display initialisation commands for DeckHD display.
3. To let the OS know that you're booting up with a 1200p display instead of the default 800p.

> So in theory, each time Valve releases a new BIOS version, we will take that and customise it to make it compatible with the DeckHD display. Users would need to perform a simple BIOS-flashing procedure via our installation script in Desktop Mode whenever they upgrade to a new SteamOS version. At this moment, I'm not able to answer whether our BIOS versions will be made open-source, I will need to confirm with our team about this. Though, our goal is to ultimately work with Valve to support our DeckHD screen so users don't have to flash BIOS every time.

As [SteamDeckHQ](https://steamdeckhq.com/news/1200p-steam-deck-screen-replacement-bios-flashing/) brought out, this is concerning. Not only is it a royal pain to replace the Deck's screen -- it's also going to be more demanding on both the Deck's battery and its APU. Now on top of this, a script needs to be run by a third-party every time Valve releases a new BIOS update. [Cryobyte33](https://linuxgamingcentral.com/posts/interview-with-kyle-cryoutilities-dev/), author of the CyroUtilities app, mentions that he doesn't "personally feel safe" about this:
> The BIOS files are a black box and could be very dangerous if ever tampered with or packaged with bad intent. I'd feel much safer with an open-source tool or set of commands to do the unlock, rather than a direct flash...I would personally recommend waiting for the growing pains to clear out before buying, unless you're a tinkerer who would be okay swapping back if there's an issue. Unfortunately the possibility of the developers either abandoning new BIOS revisions or doing something malicious is non-zero, so I wouldn't recommend it for the average consumer.

I will be getting a review sample of the DeckHD later this month or next -- a concrete shipping date hasn't been set in stone yet. But man, I've got some chills running up my spine upgrading the display.

Still, if you're feeling confident, you can join the waitlist on the [official website](https://deckhd.com/). Whenever the display becomes available for purchase, it will be $100.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
