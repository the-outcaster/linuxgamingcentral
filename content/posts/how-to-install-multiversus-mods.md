+++
title = "How to Install Mods for MultiVersus"
date = 2022-07-25T16:03:30-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/multiversus_mod_guide/cover.jpg"
tags = ["guide", "multiversus", "modding"]
keywords = ["multiversus", "mods"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
*MultiVersus* hasn't even reached a stable state yet, but the modding community has already made it possible to add your favorite characters from other games. Want to add Link over Wonder Woman? Ganondorf over Superman? Waluigi over Shaggy? A darker-colored skin for Harley Quinn, based on her appearance in *Injustice 2*? It's possible! Best part is, it's *dead* simple. Just a matter of downloading the mod and putting it into the appropriate folder. No extra launch parameters needed or other files to copy over.

Let me just add this disclaimer, though: *MultiVersus* uses Easy Anti-Cheat. The game runs with Proton, and surprisingly, based on the three-or-four hours that I've tested so far, EAC doesn't seem to care about the fact that I'm running mods. I've been able to play dozens of online matches and haven't experienced any kicks, desyncs, or other hiccups. That being said, though, I'm still giving the warning that *you should proceed at your own risk.* The game may get an update later on that may prevent mods from being able to be used, or worse, could result in a ban. Enjoy them for now.

![waluigi mod page for shaggy](/images/multiversus_mod_guide/waluigi.jpg)

Right now, mods for *MultiVersus* are mostly character skin/model replacements. So far it doesn't seem voice clips are able to be swapped out. There aren't any mods at the moment that change the texture of stages or replace music tracks, but I wouldn't be surprised if the modding community comes up with those later on.

Mods for the game are available on [GameBanana](https://gamebanana.com/games/14946). Some notable mods include:
- [Blaziken over Shaggy](https://gamebanana.com/mods/391737)
- [Waluigi over Shaggy](https://gamebanana.com/mods/391623)
- [Link over Wonder Woman](https://gamebanana.com/mods/391131)
- [Ganondorf over Superman](https://gamebanana.com/mods/391442)
- [Captain Falcon over Batman](https://gamebanana.com/mods/390746)
- [Chowder over Steven Universe](https://gamebanana.com/mods/391706)
- [*Injustice 2*-inspired Harley Quinn](https://gamebanana.com/mods/391088)

Simply head to the mod page and download it. The mod will generally consist of a zip archive with a PAK file inside. Go to the game's installation directory, and in `MultiVersus/Content/Paks/`, create a new folder: `~mods`. By default this is what the folder structure would look like:

`~/.local/share/Steam/steamapps/common/MultiVersus/MultiVersus/Content/Paks/~mods/`

Extract the PAK file to `~mods/`. That's literally it. Now you've got a custom character skin! Multiple PAK files can go in here; just make sure you don't have two mods that go over the same character. Run the game and verify that the mod is working.

![multiversus mods in action](/images/multiversus_mod_guide/in_game.jpg)

I'm having a blast with the game, by the way. I will likely have an overview of my impressions with the game in the next couple of days. Also, if you want to get into the modding scene yourself, there's a [model import tutorial](https://youtu.be/TwPSkPEBI6k) on YouTube.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
