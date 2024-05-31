+++
title = "You May Want to Avoid Using Firefox on the Steam Deck"
date = 2022-07-06T22:26:53-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/firefox.webp"
tags = ["news", "steam deck", "firefox"]
keywords = ["steam deck", "steamos", "firefox"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
*UPDATE: Valve will reportedly be using the Flatpak version of Firefox with the next update to SteamOS 3.3, according to an update from [GamingOnLinux](https://www.gamingonlinux.com/2022/07/you-should-avoid-the-stock-firefox-install-on-steam-deck-as-its-badly-outdated/).*

Well, at least the *stock* version of Firefox supplied with SteamOS.

It's come to my attention, thanks to Quinn from our [Matrix channel](https://matrix.to/#/#linux-gaming-central:matrix.org), that SteamOS is using a *highly* outdated version of Firefox. The latest version is [102.0.1](https://www.mozilla.org/en-US/firefox/102.0.1/releasenotes/), which came out today. However, the latest build on SteamOS, even on the beta 3.3 branch, is using [96.0.3](https://www.mozilla.org/en-US/firefox/96.0.3/releasenotes/), which came out almost *six months* ago.

Two responses came from Steam Support regarding this issue, according to a thread posted on [r/SteamDeck](https://www.reddit.com/r/SteamDeck/comments/vszcq8/the_steam_decks_firefox_continues_to_be_outdated/). They were reported as saying:
> I am sorry to hear that you are having trouble with Steam Deck. We are investigating this issue further. As soon as we have more information, we will update your ticket.

And:
> Thank you for the report. The Steam Deck development team is aware of the concerns/issue around this and are looking into it. Any new updates will be detailed [here](https://store.steampowered.com/news/app/1675200) in our release notes.

I'm not sure when the issue was reported, but Firefox right now is still on version 96.0.3 on the Deck. This brings security concerns. Supposedly Firefox 96 is known to be vulnerable to at least four critical security flaws, and potentially dozens of others. Examples of such security flaws are explained [here](https://www.mozilla.org/security/advisories/mfsa2022-09/) and [here](https://www.mozilla.org/security/advisories/mfsa2022-19/). And there's no way of updating the browser until Valve releases a new image of SteamOS, or if the user unlocks the immutable file system, which could again lead to compromise if the user doesn't know what they're doing.

So, unless you want your data compromised, I *strongly* suggest installing Firefox as a Flatpak, which is going to use a *much* more up-to-date version (102.0.1 at the time of writing this, as a matter of fact!). LibreWolf, Chrome, Chromium, Brave, and even Microsoft Edge are all available on Flathub as well (not that I'd recommend anyone using Edge, unless they're using [Xbox Game Pass](https://linuxgamingcentral.com/posts/xbox-game-pass-quality-throttled-on-linux/)). Only problem there is because the Flatpak is sandboxed and in isolation from the rest of the system, you'll have to re-install your add-ons, log back in if you were signed in to Firefox Sync, re-add your bookmarks, yada yada.

It makes me curious why Valve never shipped Firefox on SteamOS as a Flatpak in the first place. It would be much more up-to-date and the user would be able to update as soon as a new version becomes available. But for some reason, Firefox is part of the SteamOS image as a whole.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
