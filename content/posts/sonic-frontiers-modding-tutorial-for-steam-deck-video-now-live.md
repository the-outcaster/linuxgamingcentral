+++
title = "Sonic Frontiers Modding Video Tutorial is Up!"
date = 2022-11-30T14:34:42-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/game_reviews/sonic_frontiers/cover.jpg"
tags = ["news", "guide", "video tutorial", "sonic", "steam deck", "steamtinkerlaunch"]
keywords = ["sonic frontiers", "hedge mod manager", "steamtinkerlaunch", "sonic frontiers modding", "steam deck"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Some folks wanted a video tutorial going over how to get Hedge Mod Manager running on Deck, so [here you go](https://www.youtube.com/watch?v=FJs1FADQI08).

Text version:
1. Get STL: `git clone https://github.com/sonic2kk/steamtinkerlaunch.git`
2. `cd steamtinkerlaunch`
3. `./steamtinkerlaunch` (updates to latest git and installs all dependencies needed)
4. `./steamtinkerlaunch compat add` (adds STL to Steam)
5. Restart Steam and force *Frontiers* to use STL. Run the game
6. Go to GLOBAL, configure HMM to use nightly build. Close STL and force Frontiers to use GE-Proton7-41 (or an older build if it doesn't work for some reason)
7. `./steamtinkerlaunch hmm start nightly` (to verify if HMM works. Will take a while)
7b. If HMM doesn't open, delete "hedgemodmanager" folder in `/home/deck/.config/steamtinkerlaunch/`, then run the above command again
8. Get mods and place them in the "Mods" folder inside the game install directory
9. Run HMM again with `./steamtinkerlaunch hmm start nightly`, configure mods and codes
10. Click "Save" when done. Launch the game either directly through Steam or with HMM
11. (Optional) Create a desktop shortcut for HMM. Paste the following into a text editor:

```
[Desktop Entry]
Encoding=UTF-8
Exec=path/to/stl_executable/./steamtinkerlaunch hmm start nightly
Icon=path/to/icon
Name=Hedge Mod Manager
Type=Application
```

Save the file to your desktop with a .desktop extension. You can then right-click this file and add it as a non-Steam shortcut so you can run it in Game Mode.

If *Frontiers* doesn't load, use an older version of Proton.

If anyone comes across any issues, well, I might not be able to help any further. You may want to describe your issue on the [HMM GitHub thread](https://github.com/thesupersonic16/HedgeModManager/issues/219).

If you want to get HMM running on desktop Linux, you can refer to my other [guide](https://linuxgamingcentral.com/posts/sonic-frontiers-modding-guide/).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
