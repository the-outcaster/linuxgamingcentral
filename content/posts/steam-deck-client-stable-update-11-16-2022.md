+++
title = "Steam Deck Client Stable Fixes Delay When Running a Game Offline, Adds QR Code Login (And Tons of Other Features/Improvements)"
date = 2022-11-16T22:54:20-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam/new_bpm/cover.jpg"
tags = ["news", "steam deck", "software update", "steam deck client update", "stable"]
keywords = ["steam deck", "steam deck client", "steam deck client update", "new big picture mode"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Now that a new Steam Deck client update has reached the stable branch, it has incorporated all the changes from the beta branch since [October 18th](https://store.steampowered.com/news/app/1675200/view/3414317363006517615). This is almost a month's worth of changes, including quicker startup times if you have a large library of games, reduced size of the Steam client, QR code functionality when logging into your Steam account, gyro enabling for gamepads that don't support capacitive touch, Nintendo-style button layouts, updated Desktop controller layout, and *tons* of other features, fixes, and improvements. This update also contains the [New Big Picture Mode](https://store.steampowered.com/news/app/593110/view/3394051164709183116) -- you'll need to run Steam in the terminal with `-gamepadui` or `-newbigpicture` to be able to use it.

Check out the new Big Picture Mode video:

{{< rawhtml >}} 

<video width=100% controls>
    <source src="/videos/new_bpm/new_bpm.webm#t=0.5" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

Full patch notes are as follows:

**General**
- Reduced client startup times for users with large game libraries
- Fixed issue where launching a game would take longer to start if there was no network connection.
- Fixed VR flags not showing up in app details for some games
- Fixed downloads page crashing when starting in offline mode
- Downloads page now properly responds to online/offline status
- Collections view can now show more than two rows of collections and allow scrolling
- Reduced size of Steam client download
- Fixed bluetooth failing to turn on in gaming mode if it was disabled in desktop mode
- When installing a game always show the install location picker if there is more than one library folder, and automatically focus the default library folder when the dialog shows up
- Added error dialog for when the user clicks on a mailto link
- Fixed the 'Cancel' button in the wifi password dialogue for a new connection causing the current network to disconnect
- Re-worked "Gifts Pending" page to be gamepad navigable

**Docked Mode**
- Fixed incorrect size of Main Menu in docked mode with 4k displays
- Virtual Keyboard now has a maximum width, so that it doesn't stretch to an unusable size on large screens
- Set scale for startup movies so that the top and bottom of the movie are cropped for 16:9 aspect ratio

**Desktop Mode**
- Fixed issue preventing the Virtual Keyboard from accessing the clipboard and being unable to perform paste operations
- Center the popup controller configurator window when viewing controller layout
- Fixed circular download progress indicator being broken in game entry list

**Sign In**
- Added login flow that supports new QR code functionality
- Fix a case where if the sign-in UI had cached credentials which had become invalid, it could get stuck and not accept valid credentials thereafter
- Fixed an edge case in handling of invalid cached credentials affecting reauthentication

**Steam Input**
- Gyro Enabling: The "Touch" option is now available to controllers which do not have capacitive touch sensors - Moving joysticks out of their deadzone now counts as a "Touch".
- All controller types can each now optionally choose to use a Nintendo-style layout. This flips the A and B button and X and Y button universally in Steam and in games.
- The Xbox extended features driver has been updated for Windows 11
- Fixed hang when the Amazon Luna controller rumbles on macOS
- Fixed issue with the touch binding in As Mouse mode releasing before the end of a swipe
- Fixed doubled input for Nintendo Joy-Cons controllers
- Gyro Yaw & Roll Combined now allows negative contribution values from both sources.
- FlickStick output can now be Inverted, and can be sent to X or Y Mouse axis.
- Fix for FlickStick turning when exiting an overlay layer with the stick still thrown.
- Desktop Controller Layout Now defaults to a desktop friendly set of controls. Long-Pressing Menu Button will toggle back and forth to a Gamepad friendly layout.
- Updated Steam Controller LB and RB button images

**Remote Play**
- Fixed glyphs for third party Nintendo controllers while streaming

**New Big Picture Mode**
- Updated Big Picture is now available for testing. You can read more about it in this blog post. Modify your Steam client shortcut and add -gamepadui on the command-line to automatically start Steam in the new Big Picture Mode. Alternatively, pass -newbigpicture to start in Desktop mode and have access to the new Big Picture Mode at any time.

Additionally, it was apparently updated again to fix a browser crash in Desktop Mode.

Patch notes can also be seen on [Steam](https://store.steampowered.com/news/app/1675200/view/3383920059443299217). On a side note, the SteamOS 3.4 beta also got [updated](https://store.steampowered.com/news/app/1675200/view/3469488996651224898) to fix the OSK with two languages and add a workaround "for an underlying Steam/Proton issue causing some games...to fail to launch."

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
