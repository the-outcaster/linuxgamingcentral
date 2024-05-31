+++
title = "You Can Run Containerized Distros on Steam Deck Thanks to Distrobox"
date = 2022-09-08T12:47:04-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/distrobox/cover.jpg"
tags = ["news", "software update", "distrobox", "steam deck"]
keywords = ["distrobox", "steam deck"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
As [Phoronix](https://www.phoronix.com/news/Distrobox-1.4-Released) had spotted earlier today, Distrobox -- a wrapper that creates and uses containers (like a distro) that are highly integrated into the host machine -- got a pretty big update with 1.4.0. I won't go over the changes, but I will say this: there's now [documentation](https://github.com/89luca89/distrobox/blob/main/docs/compatibility.md#host-distros) on how to get Distrobox set up on the Steam Deck. Just look under the "SteamOS 3" section on their table. Simply run `steamos-readonly disable` via the terminal to disable the immutable file system, then follow their installation instructions for Arch Linux or install Podman to `$HOME`.

A question you might have is, "Why use Distrobox on the Steam Deck?" Well, Distrobox allows you to run virtual distros on your system, without having to resort to installing the distro separately on an external storage medium, such as a MicroSD card. You can then reap all the benefits of that virtual machine -- such as patched Mesa drivers -- on SteamOS. So, for instance, if we were to go back to the time when *Halo Infinite* was running on Deck with [Nobara Project](https://linuxgamingcentral.com/posts/nobara-project/) (Fedora spinoff) but *not* with SteamOS, you could run Nobara Project as a container within SteamOS with Distrobox. You could then allow *Halo Infinite* to run via the virtual machine.

When installing Distrobox on Deck, I recommended that you follow the instructions for [installing Podman in a static manner](https://github.com/89luca89/distrobox/blob/main/docs/compatibility.md#install-podman-in-a-static-manner). This way you can install `podman` -- the container engine that Distrobox uses -- to your `$HOME` directory and not have Distrobox wiped with every update that comes to SteamOS (due to the way SteamOS handles updates to the immutable file system).

See the patch notes for Distrobox 1.4.0 on [GitHub](https://github.com/89luca89/distrobox/releases/tag/1.4.0). And who knows, I might have a guide soon on how to get Distrobox running on Deck.

*Cover image credit: Distrobox GitHub*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
