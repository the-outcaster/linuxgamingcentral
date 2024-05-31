+++
title = "WinesapOS Now Works on Steam Deck with MicroSD Card"
date = 2022-07-15T18:48:20-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/winesapos/cover2.jpg"
tags = ["news", "distro update", "winesapos"]
keywords = ["winesapos", "steam deck"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
When I had reported to Luke Short -- the main developer behind [WinesapOS](https://github.com/LukeShortCloud/winesapOS) -- that his distro wouldn't boot on a MicroSD card on the Steam Deck, he personally saw to it that he would replicate the issue and fix it. As such, we now have a new update to enjoy: [3.1.1](https://github.com/LukeShortCloud/winesapOS/releases/tag/3.1.1).

I can now confirm WinesapOS runs on the Steam Deck when it's installed on a MicroSD card. Display is rotated (though I've found this to be a very common issue with distros outside of SteamOS). Some other changes have landed with this update as well. GE-Proton is now installed during first-time setup, the GRUB theme has been changed to Vimix, pre-built AUR packages have been added to the WinesapOS repo, and `pipewire-media-session` has been changed to `wireplumber`.

The image file size is still rather large at 30 GB, but the team is aware of this and will be shrinking the installer image down with the 3.2.0 update.

One big advantage WinesapOS has over SteamOS is the packages are *much* more up-to-date. I'm still trying to figure out if I can get *Halo Infinite* to run; I haven't had enough time to test but if I do happen to have success I will report about it.

See the patch notes on [GitHub](https://github.com/LukeShortCloud/winesapOS/releases/tag/3.1.1).

*Cover image credit: WinesapOS GitHub*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
