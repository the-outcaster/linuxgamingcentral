+++
title = "GLIBC-EAC -- Get Your EAC-Enabled Games to Run on Arch/Steam Deck Again"
date = 2022-12-30T16:13:33Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/eac/eac_error.jpg"
tags = ["news", "eac", "anti-cheat", "arch linux", "steam deck", "glibc"]
keywords = ["glibc", "glibc-eac", "frogging-family", "eac", "easy anti-cheat", "epic games", "arch linux", "steam deck"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
So, those GLIBC developers...they have a tendancy of breaking things related to anti-cheat (particularly EAC). So much so that even Valve's own Pierre-Loup Griffais had [complained](https://twitter.com/Plagman2/status/1559683905904463873) about it, mentioning that this "contributes to damaging the idea of desktop Linux as a viable target for third-party developers."

If you're on Arch Linux on desktop, or you're using the Steam Deck, you might not be able to get certain games with EAC to run anymore, because both platforms updated to the latest version of GLIBC. For instance, you might not be able to run [*Divine Knockout*](https://store.steampowered.com/app/1294660/Divine_Knockout_DKO/) (DKO) or [*Rogue Company*](https://store.steampowered.com/app/872200/Rogue_Company/). Other games like [*Brawlhalla*](https://store.steampowered.com/app/291550/Brawlhalla/) or [*MultiVersus*](https://store.steampowered.com/app/1818750/MultiVersus/) will still work though, since they use a different version of EAC.

![DKO borked on Deck](/images/guides/glibc-eac/dko_borked_on_deck.jpg)

Unfortunately the GLIBC upgrade -- particularly version 2.36 -- has created more problems than it has solved. To find out what version of GLIBC you're using, open a terminal and run `ldd --version`.

![GLIBC version on Fedora](/images/guides/glibc-eac/glibc_version.png)

You can see here on Fedora, I'm running version 2.35. Which means I don't have to worry about EAC games not running (queue the infamous clip of GloriousEggroll [eating popcorn](https://twitter.com/GloriousEggroll/status/1555003985299374082) while watching Arch users suffer). If you run this command on Arch, however, or on the Steam Deck, you are likely running version 2.36, which has been causing the issues.

![GLIBC version on Deck](/images/guides/glibc-eac/glibc_version_on_deck.png)

But fret not -- [glibc-eac](https://github.com/Frogging-Family/glibc-eac) has come to the rescue. This is the "Arch glibc with the commit breaking eos-eac reverted. By running this script, you *should* be able to get games like *DKO* and *Rogue Company* to work on Arch and the Steam Deck again.

# If You're on Arch Desktop
Simply clone the repo:

```
git clone https://github.com/Frogging-Family/glibc-eac.git
cd glibc-eac
```

Then run the `glibc_eac.sh` script:

`./glibc_eac.sh`

This will build and install GLIBC with the breaking EOS-EAC commit reverted. Get yourself comfortable, because this is going to take a while (on Deck it took close to an hour). When all is said and done, reboot the computer and you *should* be good to go.

# If You're on Steam Deck
Unfortunately with Valve being Valve, they decided to make installing pacman packages a whole lot more complicated than it should be. And while I would offer instructions here on how to fix EAC on Deck, I'm still in the process of trying to figure that out myself. It's proving to be a real pain in the arse. Basically I've made an Arch Linux container with [Distrobox](https://linuxgamingcentral.com/posts/distrobox-1.4-adds-steam-deck-documentation/), and while I was able to install glibc-eac within it, *DKO* still isn't running. It's complaining about something related to DX11 not being present on the system, even though other games are running within the container (Mesa drivers are up-to-date if you were wondering).

![DKO on Deck progress](/images/guides/glibc-eac/dko_on_deck_progress.jpg)

Still, it's progress. Better than the error that you typically get in the cover photo.

If I ever do come across a solution, I will be sure to document the process.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
