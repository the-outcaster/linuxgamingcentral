+++
title = "Finally, You Can Enable Audio on Deck with Distros Outside of SteamOS"
date = 2023-02-26T22:41:18Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/chimeraos.jpg"
tags = ["news", "steam deck", "steam deck audio", "chimeraos"]
keywords = ["audio on steam deck", "chimeraos on steam deck", "steam deck audio", "acp5x"]
description = "But, unsurprisingly, Valve is 'refusing to comply with GPL source requests.'"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
*EDIT (3/5/2023): accusations from the maintainer of the acp5x-ucm-files repo regarding Valve not upstreaming the ALSA UCM configurations are not true. This comment has been removed from the article.*

One long-standing issue that the Steam Deck has had with support of distributions *other* than SteamOS is the lack of audio. But someone finally figured out how to patch audio support in.

This is thanks to [OpenSD](https://gitlab.com/open-sd) -- one of their repos is [acp5x-ucm-files](https://gitlab.com/open-sd/acp5x-ucm-files). This will "temporarily provide some missing ALSA UCM configuration files needed to fix the audio on the ACP5x which the Steam Deck uses."

Basically, all you need to do after cloning the repo is copy the files from `alsa` into the distro's `alsa` directory, which on Arch, would be `/usr/share/alsa/`. Or just run the install script with `sudo ./install.sh`. In theory you should be able to run the install script on *any* distro with kernel 6.1 or later and get audio support.

Looks like the [ChimeraOS](https://linuxgamingcentral.com/tags/chimeraos) team got audio up and running on their distro:

{{< rawhtml >}} 

<video width=100% controls>
    <source src="/videos/steam_deck/audio_on_deck_chimeraos.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}
*Video credit: Matthew Anderson (Ruineka)*

Actually, this repo has been around for two months, but I didn't find out about this project until now.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
