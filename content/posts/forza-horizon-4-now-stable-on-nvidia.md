+++
title = "Forza Horizon 4: Finally Playable Without Crashing?"
date = 2023-01-24T14:14:34Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/fh4/cover.jpg"
tags = ["news", "racing", "forza horizon series"]
keywords = ["forza horizon 4 on nvidia", "forza horizon 4 on linux", "forza horizon 4", "forza horizon 4 no crashing"]
description = "A Reddit user may have discovered how to play the beloved racing title on NVIDIA without random crashing (perhaps could work for AMD as well?)."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Going by the reports on [ProtonDB](https://www.protondb.com/app/1293830), it seems *Forza Horizon 4* suffers from random crashing across all GPU vendors, including the Deck. I do recall playing the game back when I had a NVIDIA GPU and getting a consistent crash at the same area in-game.

Seems like [u/Conradson](https://www.reddit.com/r/linux_gaming/comments/10k05w4/forza_horizon_4_stable_on_nvidia_with_geproton724/) spent ten hours trying to figure out a solution. At least for NVIDIA users. Their process is as follows:
- *don't* use GameMode
- need to use [GE-Proton7-24](https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-24) for some apparent reason
- Before the first run with GE-Proton7-24, remove the Proton prefix `steamapps/compatdata/1293830` if it exists (in your Steam install folder)
- Before the first run with GE-Proton7-24, disable Shader Pre-Caching, then re-enable it to generate new cache (in Steam > Settings > Shader Pre-Caching)
- In-game, disable MSAA in the video settings, you can set the other settings as you like

They reported both singleplayer and multiplayer are working without a hitch. Both the native .deb package of Steam on Ubuntu as well as the Flatpak version worked.

Mildly interesting. Since I refunded the game I can't verify if this works or not. But I'd be curious if this will work on AMD/Steam Deck.

Game is on [sale](https://store.steampowered.com/app/1293830/Forza_Horizon_4/) for 67% off during the Xbox lunar sale.

*Cover image credit: Playground Games/Xbox Game Studios*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
