+++
title = "Steam Deck Repo -- Quality Boot Videos For Your Steam Deck"
date = 2022-10-08T14:05:20-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck_repo/cover.jpg"
tags = ["steam deck repo", "website", "steam deck"]
keywords = ["steam deck repo", "steam deck startup video"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
With the recent [update](https://linuxgamingcentral.com/posts/steamos-3.3.2-and-steam-deck-client-update-10-5-2022/) that Valve pushed to the Deck, it's now easier than ever to use custom boot animations or videos. And as [Steam Deck Life](https://steamdecklife.com/2022/10/08/steam-deck-repo-lets-you-upload-and-share-steam-deck-boot-videos/) brought out earlier today, there's a website where you can easily find quality videos -- Steam Deck Repo, founded by Reddit member [u/waylaidwanderer](https://www.reddit.com/user/waylaidwanderer). Featuring Love, Death & Robots, Kill Switch, a PS3-styled bootloader, a *Cyberpunk*-themed one, the GabeCube, and a plethora of other cool-looking animations, you can easily download them now and put them on your Deck.

Basically, this is how the process goes:
1. Go to the [Steam Deck Repo](https://steamdeckrepo.com/) site on your Deck while in Desktop Mode
2. Find an animation that you like and download it. These video files are already in `webm` format; no need to convert them or truncate the file
3. Rename the downloaded file to `deck_startup.webm`
4. Place it in `~/.steam/root/config/uioverrides/movies/`

Note that you will need to show hidden files in your file manager in order to see these folders, and you will likely need to create the `uioverrides` and `movies` folders. But the good news is that these videos won't get wiped with any new Deck update.

I'm personally fond of the [GabeCube](https://steamdeckrepo.com/post/6YWNE/valve_gabecube) intro. I put my own little spin on it and gave it a red hue:

{{< rawhtml >}} 

<video width=100% controls>
    <source src="/videos/gabecube.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

If you want to upload your own videos, you're welcome to do so. Looks like you can sign in via your Steam account.

I'm wondering if it would be possible to create a simple bash script that pulls a list of available videos, from which you can pick, download, have it automatically rename the file, and put it in the right location. Should be fairly simple. Maybe even a Crankshaft plugin so you can download directly from Game Mode?

If you have multiple startup videos, and want to use a random one each time you start the Deck up, you can use kageurufu's [script](https://github.com/kageurufu/steamdeck_startup_animations).

Check out the [site](https://steamdeckrepo.com) for more info!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
