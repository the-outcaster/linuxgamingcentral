+++
title = "Valve Quietly Upgrades SteamOS to 3.4 -- Stock Firefox Now Removed"
date = 2022-07-27T09:56:13-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steamos/3.4/firefox.jpg"
tags = ["news", "steam deck", "steamos"]
keywords = ["steamos", "steam deck"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
*UPDATE: the SteamOS beta update is now [official](https://store.steampowered.com/news/app/1675200/view/3413183219978214105). As confirmed, Firefox is now Flatpak-based. There's also a new theme for the Plasma desktop, network connections are shared between Desktop and Game Mode, a small update for Chinese, Japanese, and Korean keyboards, the controller firmware has been updated, and the Xbox login window should now render characters that were previously hidden.*

Looks like a new [update](https://www.reddit.com/r/SteamOS/comments/w9bxyl/steamos_34_has_been_released_in_previewmain_but/) has shipped to SteamOS on the "Main" OS update channel, but don't get your hopes up -- almost everything that I mentioned in my [SteamOS](https://linuxgamingcentral.com/posts/the-growing-security-risk-with-steamos/) piece, those packages have **not** been upgraded. The kernel remains at 5.13, Mesa drivers are still at 22.0.2, glibc is still 2.33, Plasma is still at 5.23.5. As this update has not been officially released yet, there's no patch notes available.

If there's one good thing I can extract from the update, however, it would be this: though the Firefox build is still in the SteamOS repo, it has been removed from the OS itself. If you try to launch Firefox from the taskbar, and you haven't installed the Flatpak version, Discover will open up and you will be prompted to install that. So, at least you can take some solace in the fact that you'll be using the latest version of the browser -- which, at the time of writing this, is [103](https://www.mozilla.org/en-US/firefox/103.0/releasenotes/).

![plasma on steamos 3.4](/images/steamos/3.4/plasma.jpg)

Other than that, I haven't observed much of anything different with this update. I will update this post if I discover anything else that's changed (or if Valve says anything about it).

Note that if you want access to this update, you'll need to enable developer mode under the System tab in the Settings menu, and then under the Development tab, show advanced update channels from the "Miscellaneous" section. Go back to the System tab and select "Main" as the OS update channel. Apply the update and restart the Deck.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
