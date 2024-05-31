+++
title = "Steam Deck Client Update Adds LAN Game Transfer, DualSense Edge Support, and Improves UI Responsiveness"
date = 2023-03-16T03:05:40Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/client_updates/stable/3-15-2023/cover.jpeg"
tags = ["news", "steam deck", "software update", "steam deck client update", "stable"]
keywords = ["steam deck", "steam deck client", "steam deck client update", "steam deck client stable update", "steam deck stable client update", "dualsense edge", "razer wolverine v2", "steam deck lan"]
description = "Plus: new Steam console feature and a broken Soundtracks tab!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Well, a stable update has come faster than I knew it. There's just a *ton* of stuff here, so I'm only going to highlight some new features added to this update.

First thing is, it looks like you can access the **Steam console** by pressing the Steam button and selecting Console from the menu. This can also be accessed by enabling dev mode and going to the Developer tab in the Settings menu. Not really sure what someone would use this for -- it's not even mentioned in the patch notes -- but I guess it's something.

![Steam Deck console](/images/steam_deck/client_updates/stable/3-15-2023/console.jpeg)

Second, **LAN game transfers** are in! According to [Gardiner Bryant](https://viewsink.com/hands-on-with-steams-beta-lan-transfer/), this feature is useful for those who have "limited connections" but otherwise, "you might find its simpler and just about as fast to download your games right from Steam's servers at the outset."

Third, you can apparently **get Steam runtime system info**, but this hasn't really been working for me. You can access this from the System tab in the Settings menu.

![Steam runtime info](/images/steam_deck/client_updates/stable/3-15-2023/steam_runtime.jpeg)

A "Soundtracks" tab was added to the library!

![Steam Music tab](/images/steam_deck/client_updates/stable/3-15-2023/music.jpeg)

...but it crashes as soon as you select an album.

![Steam Music crash](/images/steam_deck/client_updates/stable/3-15-2023/music_crash.jpeg)

UI responsiveness has been improved in regards to Steam reconnecting. DualSense Edge gets support, including back button remapping. Razer Wolverine V2 gamepads are also now supported. There are just so many other fixes and changes, so I'll just let the patch notes do the rest of the talking for me.

Patch notes can also be read on [Steam](https://store.steampowered.com/news/app/1675200/view/3716071853478720783).

**Local Network Game Transfers**
- Added new feature that allows Steam users to copy existing Steam game installation and update files from one PC to another over a local area network, without having to download and install from a Steam content server on the internet. This helps you stay below your ISP monthly transfer limits and can speed up installs or updates.
- Steam users have control over who files can be sent to: self only, friends only, or everyone. The default setting is self only.
- More info about this new feature can be found [here](https://help.steampowered.com/en/faqs/view/46BD-6BA8-B012-CE43)

**General**
- Move advanced HDR options to Developer Settings
- Streamable games are now included in the Ready to play game filter, though the default action is still to install them locally.
- Fixed a bug preventing some Demo apps that store files under the full-game App ID from uploading to Steam Cloud from Steam Deck devices
- Stop prompting users to register for Steam Deck rewards if they have chosen the Ignore Forever option
- Fixed some transparency issues with the background in the in-game overlay.
- Fixed issue where user could not re-enter a context submenu after backing out of it
- Fixed issue where incoming chat messages would not be delivered properly while in-game
- Reduced flashing in background when scrolling through games on home screen
- Game invites in the Quick Access Menu will now default to opening a context menu to accept the invite rather than navigating to the chat tab and having to hit Accept there.
- Added ability to retrieve Steam Runtime System Information for Linux devices
- Improved UI responsiveness when reconnecting to Steam
- Fixed the appearance of jumbled UI that could happen for a second or two when starting Steam
- Fixed crash when in a voice chat
- Fixed crash when authorizing a microtransaction purchase
- Fixed the Play button stealing focus when a game is launching
- Constrain the width of settings, chat, and other non-grid based views when connected to larger monitors
- Fixed misalignment of loading throbber after logging in.
- Fixed universal search not applying mature content filtering preferences

**Steam Input**
- Added support for the Sony DualSense Edge controller including support for remapping of the rear buttons.
- Added a loading throbber when waiting on Steam Cloud to update 
- Improved the latency of querying the workshop in the Configuration Browser and fix issues with configurations popping-in or opening the wrong tab because results weren't fully received
- Added a loading throbber that shows while the Configuration Browser workshop query is running
- Fixed PS5 edge settings leaking into PS5 controller
- Fixed Steam Link app mobile touch gyro not working
- Fixed crash exiting deadzone visualization
- Fixed the physical input visualization only looking at the first connected controller
- Fixed rumble for Nintendo Joy-Con controllers
- Added support for the Razer Wolverine V2 controllers
- Added the ability to reset the device input mapping in new Big Picture
- Added the ability to install and uninstall the Windows Xbox Enhanced Features driver to the new Big Picture controller settings
- Updated the Windows Xbox Enhanced Features driver with the following changes:
  - Added support for Xbox Series X controllers connected via the Xbox Wireless Adapter
  - Fixed delay detecting hotplugged USB controllers, occasionally causing duplicate controllers in Steam
  - Fixed interference with the Victrix Control Hub after the driver has been uninstalled
- Fixed Logitech F310 controller input on macOS and Linux
- Added mapping for DualSense Edge Wireless Controller on Linux (note that advanced feature support require Steam to be able to access the /dev/hidraw* devices)
- Fixed unintended inversion of Gyroscope Roll Axis on Steam Deck
- Added some optimization around DualSense adaptive trigger effects interaction with the Bluetooth stack

**Desktop Mode**
- Added UI that temporarily replaces the What's New section of the Library when pre-purchased games are available to pre-load or install and play
- Added UI at startup for account selection
- Added a sign out option to the main menu that removes credentials for the signed in account from the machine
- Fixed a crash when the OS is notifying Steam that it should shutdown
- Improved performance of games when using Steam Workshop APIs
- Refreshed the profile games page with a new style and improved performance
- Fixed crash for some uses of %command% in shortcut launch options
- Fixed quotes surrounding shortcut exe and paths
- Fixed Steam Library Folder dialog showing in Downloads settings
- Fixed soundtrack cover art, artist, and track information not appearing in Additional Content section of app details
- Fixed some actions that should have opened external applications, such as a URL in your default browser, that were instead doing nothing
- Fixed a crash loading the standalone controller configurator
- Fixed another issue blocking download of precached shaders

Also, if you happen to be on the Beta or Preview branch, there's an [update](https://store.steampowered.com/news/app/1675200/view/3716071853479110833) for you. Guide page layout in overlay with 4:3 aspect ratio games, in addition to "downloading optional DLC," has been fixed.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
