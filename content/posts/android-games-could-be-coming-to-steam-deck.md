+++
title = "Android Games: Coming to Steam Deck Soon?"
date = 2023-01-25T19:11:50Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/android_on_deck.jpg"
tags = ["news", "steam deck", "android", "wayland", "gamescope", "waydroid"]
keywords = ["steam deck", "android", "wayland", "gamescope", "waydroid", "android on steam deck", "steam deck with android"]
description = "Speculation gears are flowing following a batch of recent commits to Gamescope."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
A couple of developers who I'm friends with have closely been following the commit history to [Gamescope](https://github.com/Plagman/gamescope). They just pointed out to me some of the commits that have been pushed today. There's two things that we can glean:
1. Gamescope just got native Wayland client support.
2. With this added, and following the comment of one of the developers ([Joshua Ashton](https://github.com/Joshua-Ashton)), it appears as though they're looking into Waydroid support.

Part of their [comment](https://github.com/Plagman/gamescope/commit/ecee87b15794d1afa767ee8b33abe9dbd0456215) is as follows:
> Given we are only expecting like 1-2 xdg-shell windows for our current usecases (**Waydroid**, etc) I think this is reasonable for now.

[Waydroid](https://github.com/waydroid/waydroid), in case you're not aware, "uses a container-based approach to boot a full Android system on a regular GNU/Linux system." Given that the Steam Deck uses Gamescope, this would allow said device to boot and use Android. Therefore this would allow the Deck to run Android-based games with a container.

Valve did mention in [their interview with The Verge](https://linuxgamingcentral.com/posts/valve-doesnt-consider-6800u-handhelds-as-competition/) that they were looking at supporting mobile, touch-only games to the Deck. With Waydroid, the developers of the game wouldn't have to convert their code from ARM to x86. So I guess it would be a win-win situation for both the developer/publisher of the game and Valve. This way Valve can add support for Android games, as they had alluded to in the interview.

Keep in mind this is just *a comment*. Picture a grain of salt sitting on your Deck:

![Grain of salt on Deck](/images/steam_deck/photos/grain_of_salt_on_deck.jpg)

That's how you should similarly take it when it comes to comments like this.

In any event, if this *does* happen it will be some exciting news!

See today's [commit history](https://github.com/Plagman/gamescope/commits/master) if you want more details.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
