+++
title = "Beautify Your Steam Deck Library with SteamGridDB"
date = 2023-03-27T13:46:30Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/plugins/steamgriddb/frontiers_new_hero.jpeg"
tags = ["steam deck", "steam deck plugin", "steamgriddb", "decky loader"]
keywords = ["steamgriddb", "steamgriddb plugin", "steamgriddb for steam deck", "slippi on deck", "sonic frontiers"]
description = "One of the most useful plugins to have, and super easy to use!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
The Steam Deck has proven to be one of the most versatile options out there when it comes to portable PC gaming. It's not just for games on Steam, it's also for games on [the Epic Games Store](https://linuxgamingcentral.com/posts/rare-epic-games-launcher/) and other store fronts. It's also proven to be one of the most popular devices out there when it comes to [emulation](https://overkill.wtf/interview-emudeck-creators-steam-deck-emulation/).

One thing might be missing though: artwork for your favorite non-Steam games. Generally when you add a non-Steam game with the Steam client, there's no artwork associated with it. It's just this dull, gray icon that just sits in your library.

Well, we can fix this with [the SteamGridDB plugin](https://github.com/SteamGridDB/decky-steamgriddb). While SteamGridDB has infamously [been attacked by the Big N with frequent DMCAs](https://gamerant.com/nintendo-dmca-takedown-steamgriddb-art-sharing-website/), this plugin is otherwise a fantastic addition to your Steam Deck to add missing artwork for your games. Oh, and don't worry -- artwork for Nintendo games is still available to download.

Install [Decky-Loader](https://github.com/SteamDeckHomebrew/decky-loader) if you haven't already. From there, go to Game Mode and access the QAM. Navigate to the plugin icon, and go to the shopping icon on the top right. Install SteamGridDB from there.

![SteamGridDB in Decky Loader store](/images/steam_deck/plugins/steamgriddb/in_store.jpeg)

From there it's as simple as selecting the game in your library, pressing Start, and selecting "Change artwork..." from the context menu. If the option doesn't appear, you may need to exit the menu and press Start again to see it.

I'll take Slippi as an example, an AppImage that I added to my library as a non-Steam game. By default, it looks like this:

![Slippi on Steam without artwork](/images/steam_deck/plugins/steamgriddb/slippi.jpeg)

![Slippi on Steam without artwork](/images/steam_deck/plugins/steamgriddb/slippi2.jpeg)

Pretty boring, right? Let's fix this.

Select the application from your library and press Start. Select "Change artwork..."

From here you can customize the capsule, wide capsule, hero, logo, and icon. Here's what each one does:
- Capsule - the icon you see in your Steam library
- Wide capsule - the icon you see on the Home screen
- Hero - the thumbnail in the background after selecting the game from your library
- Logo - the icon that appears on the lower-left of the screen in the game preview
- Icon - the icon that appears to the left of the game name when the Steam overlay is brought up. Note that applying this may require a restart

![Slippi capsule selection](/images/steam_deck/plugins/steamgriddb/capsule_selection.jpeg)

There's a slider on the top of each tab -- you can adjust this to modify the size of the icons. The lower the slider, the more icons per row there will be.

You can select "Filter" to open up a context menu. Here you can change the game name to find artwork for something else, select the dimensions that you want, style type, file type, etc. You can even search for animated icons by toggling this on, provided that they are available for the game you're seeking artwork for. However, I don't recommend applying animated icons; I've found that they can lag the Steam library navigation pretty badly.

![Slippi capsule filter](/images/steam_deck/plugins/steamgriddb/capsule_filter.jpeg)

With the "Slippi" filter active, I don't have a lot of choices here. So, if I wanted to expand the number of icons available, I can change the filter and have SteamGridDB search for "Super Smash Bros. Melee" instead.

![SBBM filter applied](/images/steam_deck/plugins/steamgriddb/ssbm_filter.jpeg)

To apply an icon, select it, then press A to download. It's that simple.

Ah, much better.

![Slippi capsule applied](/images/steam_deck/plugins/steamgriddb/slippi_capsule.jpeg)

![Slippi wide capsule applied](/images/steam_deck/plugins/steamgriddb/slippi_wide_capsule.jpeg)

![Slippi hero and logo applied](/images/steam_deck/plugins/steamgriddb/slippi_hero.jpeg)

The SteamGridDB page will also allow you to manage these assets. You can delete them, browse for local files, or render them invisible. If you want to apply new artwork, simply download it and it will overwrite the existing one.

![Managing assets](/images/steam_deck/plugins/steamgriddb/manage.jpeg)

Note that you can also customize the artwork for games that were added with Steam ROM Manager. Sometimes, it downloads the wrong artwork -- you can fix this with SteamGridDB.

Also, Steam games themselves can have their artwork customized, if you so choose. So here's *Sonic Frontiers* by default:

![Sonic Frontiers default capsule](/images/steam_deck/plugins/steamgriddb/frontiers_capsule.jpeg)

![Sonic Frontiers default hero](/images/steam_deck/plugins/steamgriddb/frontiers_hero.jpeg)

And here it is customized, applying the same principles as non-Steam games:

![Sonic Frontiers new capsule](/images/steam_deck/plugins/steamgriddb/frontiers_new_capsule.jpeg)

![Sonic Frontiers new wide capsule](/images/steam_deck/plugins/steamgriddb/frontiers_new_wide_capsule.jpeg)

![Sonic Frontiers new hero](/images/steam_deck/plugins/steamgriddb/frontiers_new_hero.jpeg)

As you can see, the artwork customization is pretty endless. SteamGridDB is definitely a useful plugin to have!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
