+++
title = "New SteamOS 3.3 Beta Updates Graphics/Wireless Drivers, Plus a New Deck Client Update with Performance Improvements"
date = 2022-06-30T22:13:26-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/cover.png"
tags = ["news", "software update", "steam deck", "steamos"]
keywords = ["steam deck", "steamos"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Man, it's been hard to keep up with all the updates Valve has aggressively been pushing out for the Steam Deck. So, I hope nobody minds if I just do a quick copy & paste of the patch notes for today's update, as *both* the underlying SteamOS has been updated to 3.3 (as a beta), as well as the Steam Deck client itself (also in beta). The SteamOS update adds keyboard support for additional languages, brings the adaptive brightness toggle back, updates both the graphics and wireless network drivers, adds a built-in controller driver when Steam isn't running in Desktop Mode, and *plenty* of bug fixes. Full patch notes are as follows:
```
- Support for Simplified Chinese, Traditional Chinese, Japanese, and Korean keyboard. These keyboards are now available in Steam Client Beta
- Fixed a performance issue with some games when the backlight changes intensity. The Adaptive Brightness toggle is now active again in the Steam Client Beta
- Updated graphics driver with compatibility and performance fixes
- Updated wireless driver with fixes for WiFi disconnection issues on 5Ghz
- Add built-in controller driver that takes effect when Steam isn't running in desktop mode
- Fixed the panel staying off when disconnecting from dock shortly after resuming from sleep
- Fixed the panel backlight staying on while docked
- Added support for the Qanba Obsidian and Qanba Dragon arcade sticks in PC mode
- Fix washed-out colors in the Remote Play client when playing with specific hosts
- Fixed echo cancellation CPU overhead when the microphone isn't being used, improving power usage in idle or near-idle scenarios
- Fixed Bluetooth profile selection not being saved when switching away from Desktop mode
- Fixed multi-channel audio on external displays
- Fixed audio out on some capture cards
- Fixed some instances of corrupt audio after resuming from sleep
- Fixed audio output with some 32-bit games that use ALSA
```

Note that this update is **beta**. To opt-in, go to System -> Settings -> and under OS Update Channel select "Beta." Download the update, then restart the system.

To go along with this OS update, Valve have also updated the Steam Deck client. Keep in mind this is also in **beta** development. Managing screenshots and non-Steam shortcuts shouldn't crash the system as frequently. Force-quitting native games should actually work, and there's some miscellaneous "performance improvements." Full patch notes are as follows:
```
General
- Fixed some native Linux games not exiting when force-quit through Steam
- Added button to clear entered text in search bar
- Fixed several crashes related to managing screenshots
- Fixed several crashes related to non-Steam shortcuts

Steam Input
- Added missing Deck buttons for Gyro Enable and Button Chord options
- Added support for game-bundled Virtual Menu icons in the in-game Deck UI
- Misc performance improvements

Preview
- The features below also require the Steam OS Beta - you can opt into this in Settings > System > OS Update Channel.
- Added support for Simplified Chinese (Pinyin), Traditional Chinese (Pinyin, Zhuyin, and Cangjie), Japanese, and Korean keyboards. We are still refining these keyboards, please provide feedback in the forums.
- Re-enabled the Adaptive Backlight feature.
```

You can also see the patch notes for [SteamOS 3.3](https://steamcommunity.com/app/1675200/discussions/0/3410929607716145819/) and the [Deck client update](https://steamcommunity.com/games/1675200/announcements/detail/3323108691056012032) on Steam. If you want to add your feedback to SteamOS 3.3, you can do so in the announcement thread. And jeez Valve, you need to slow down!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
