+++
title = "SteamOS 3.3 Now Stable, Plus Deck Client Update"
date = 2022-08-02T21:25:58-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/cover.png"
tags = ["steam deck", "software update", "steamos update", "deck client update"]
keywords = ["steam deck", "steamos"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Looks like all the changes from the SteamOS 3.3 beta have now been pulled in and put into a stable release. It seems the SteamOS update has been pushed alongside a new stable Deck client update as well, as the patch notes are combined. Among some of the many changes in this update include the removal of Firefox as part of the SteamOS image; it's now replaced with the latest Flatpak from Flathub. Achievements and Guides have been added to the Steam overlay, adaptive brightness is now able to be toggled again, performance improvements with Steam Input, better support for external displays, support for more languages for the on-screen keyboard, and *tons* of other features and bug fixes.

[Full patch notes](https://store.steampowered.com/news/app/1675200/view/3401924854795478414) are as follows:

**General**
- Added Achievements page to overlay (while in-game press Steam button)
- Added Guides page to overlay (while in-game press Steam button)
- Added notification when Steam Deck temperature goes outside the safe operating range
- Added a scheduled night mode feature, allowing players to choose if and when they’d like night mode to automatically turn on
- Added a button to clear entered text in search bar
- Adaptive Brightness toggle is now active again
- Fixed notification for claiming digital rewards firing endlessly for some customers
- Fixed issue with medium length game names in the Main Menu Overlay not properly scrolling
- Fixed some issues with claiming Steam Deck digital rewards
- Fixed sound playing for achievement progress notifications
- Fixed washed-out colors in the Remote Play client when playing with specific hosts
- Fixed Xbox login window for Flight Simulator and Halo Infinite not rendering certain characters properly

**Steam Input**
- Added missing Deck buttons for Gyro Enable and Button Chord options
- Added support for game-bundled Virtual Menu icons in the in-game Deck UI
- Miscellaneous performance improvements

**Keyboards**
- Added support for Simplified Chinese, Traditional Chinese, Japanese, and Korean keyboard. We are still refining these keyboards, please provide feedback in the forums.
- Added initial IBus IME input support on the desktop for Chinese, Japanese, and Korean keyboards
- Fixed desktop mode keyboard sometimes failing to show or dismiss
- Fixed on-screen keyboard showing up under the Steam or Quick Access menu
- Updated keyboard behavior for improved fast typing on trackpad and touchscreen. (pressing a key while holding another key will now commit the held key instead of waiting for first to release)
- Fixed some touch styling issues with the virtual keyboard

**System Updates**
- Added a new Steam Deck software update channel selector – there are now three options:
- **Stable**: Recommended experience for most users. This option will install the latest stable Steam Client and SteamOS.
- **Beta**: Testing for new Steam features. Updates frequently. This option will install Steam Client Beta and the latest stable SteamOS.
- **Preview**: Testing for new Steam and system-level features. Updates frequently. You may encounter issues. This option will install Steam Client Beta and the SteamOS Beta.
- You will only see patch notes for the update channel you've selected. As this feature is in Beta, if you opt into the Stable channel, you will not see this selector anymore.

**Performance / Stability**
- Fixed some performance problems for users with many screenshots
- Fixed several crashes related to managing screenshots
- Fixed several crashes related to non-Steam shortcuts
- Fixed some native Linux games not exiting when force-quit through Steam
- Fixed flatpak Chrome closing improperly when quit through Steam
- Fixed a bug where some flatpak applications (like Edge) couldn't successfully quit
- Fixed a performance issue with some games when the backlight changes intensity

**Desktop Mode**
- Updated Firefox to be installed as a Flatpak, rather than from the OS repositories, to ensure timely updates
- First-time launches of Firefox from the desktop will now prompt for installation via the Discover Software Center, which will handle updates as they are published.
- Updated network connections created/edited on the desktop to default to system-wide, ensuring they are available in gaming mode
- Added VGUI2 Classic Plasma Desktop theme
- Resized virtual keyboard in Desktop mode to the appropriate dimensions
- Added support for the Qanba Obsidian and Qanba Dragon arcade sticks in Desktop mode

**Docked Mode**
- Added an option to scale the Steam Deck user interface for external displays
- Added a toggle for automatic scaling of the Steam Deck user interface for external displays
- Added ability to adjust image display settings for external displays that have overscan issues
- Fixed the panel staying off when disconnecting from dock shortly after resuming from sleep
- Fixed the panel backlight staying on while docked

**Audio / Bluetooth**
- Fixed Bluetooth profile selection not being saved when switching away from Desktop mode
- Fixed echo cancellation CPU overhead when the microphone isn't being used, improving power usage in idle or near-idle scenarios
- Fixed multi-channel audio on external displays
- Fixed audio out on some capture cards
- Fixed some instances of corrupt audio after resuming from sleep
- Fixed audio output with some 32-bit games that use ALSA

**Drivers / Firmware**
- Updated graphics driver with compatibility and performance fixes
- Updated wireless driver with fixes for WiFi disconnection issues on 5Ghz
- Updated controller firmware utilities to support future controller hardware revisions

Congrats to Valve on such a huge release! Hopefully they'll start addressing the [outdated software packages](https://linuxgamingcentral.com/posts/the-growing-security-risk-with-steamos/) on the system soon.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
