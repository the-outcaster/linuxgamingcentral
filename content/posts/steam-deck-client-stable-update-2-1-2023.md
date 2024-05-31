+++
title = "Steam Deck Client Updated on Stable, Brings Improved Library Load Times, JoyCon Improvements, Default User Selection, and Lots More!"
date = 2023-02-01T18:16:47Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/client_updates/stable/2-1-2023/controller_settings_for_non_steam_game.jpeg"
tags = ["news", "software update", "steam deck", "steam deck client update", "stable"]
keywords = ["steam deck", "steam deck client", "steam deck client update", "steam deck client stable update", "new big picture mode"]
description = "But be aware: Valve will soon cut the ax for the old Big Picture Mode!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Users on the stable branch, rejoice that you've now received a big update that contains a month and a half's worth of changes since the [last stable update](https://linuxgamingcentral.com/posts/steamos-3.4-stable/). We've got some great stuff here. I'm also glad to report Decky Loader still works with this update!

I won't go over everything, but to start, you can now disable the prompt that may show up on some games when launching them by adding the ability to use your choice as the default:

![Steam Deck default launch option selection](/images/steam_deck/client_updates/stable/2-1-2023/default_launch_option.jpeg)

You can then change this at will later on in the game's properties:

![Steam Deck default launch option selection in properties](/images/steam_deck/client_updates/stable/2-1-2023/default_selection_in_properties.jpeg)

Got a large Steam library? Well, "further optimizations" have been made to improve load times.

![Steam Deck library](/images/steam_deck/client_updates/stable/2-1-2023/library.jpeg)

Notifications are now pinned.

![Steam Deck pinned notifications](/images/steam_deck/client_updates/stable/2-1-2023/notifs.jpeg)

Supposedly changing download regions doesn't need the Steam client to be restarted anymore, although I'm still getting asked to do that every time I change it.

![Steam Deck changing download region](/images/steam_deck/client_updates/beta_1-11-2023.jpeg)

If you dock your Deck, "various fixes" have been made to the UI so that it can scale better in higher resolutions.

On the OSK, you can now use Up or Down arrow keys by pressing Shift + left/right arrow key:

![Steam Deck up and down arrow keys](/images/steam_deck/client_updates/stable/2-1-2023/osk.jpeg)

The OSK can also be moved up or down. But keep in mind this only works in Desktop Mode.

![Steam Deck OSK moved up](/images/steam_deck/client_updates/stable/2-1-2023/osk_moved.webp)

Gamepad templates can be previewed before applying.

![Steam Deck previewing gamepad template](/images/steam_deck/client_updates/stable/2-1-2023/controller_preview.jpeg)

A search tab has also been provided in the controller layout browser screen.

![Steam Deck search tab for controller layout screen](/images/steam_deck/client_updates/stable/2-1-2023/controller_search_tab.jpeg)

Non-Steam games should now have a controller settings icon.

![Steam Deck controller settings for non-Steam game](/images/steam_deck/client_updates/stable/2-1-2023/controller_settings_for_non_steam_game.jpeg)

Some joy for JoyCon users, as there is an improved layout preview, properly functioning gyro, and updated behavior of the SL/SR buttons when using a single JoyCon or paired.

Be aware, **Valve will soon remove the old Big Picture Mode entirely**. They are replacing the big picture interface in Desktop Mode with the one that Game Mode uses. If you want to use the old interface, you'll need to launch Steam with the `-oldbigpicture` argument. Valve notes that "this functionality will be removed in a future update." So, enjoy it for now, while it lasts. RIP old BPM.

That being said, the new BPM adds a quick guided tour, an option to start in windowed mode, an option to turn off gamepads when exiting, Steam controller dongle pairing, and quite a few fixes.

![Steam Deck new BPM windowed toggle](/images/steam_deck/client_updates/stable/2-1-2023/windowed_mode_in_new_bpm.png)

Of course, *tons* of fixes have made it in regards to audio crackling, the OSK, UI scaling, external gamepads, desktop mode, and a plethora of other areas.

Below are the full patch notes.

**General**
- Replaced launch option dialog with new UI that includes a checkbox to remember the user's selection - this selection can be changed in game properties
- Further optimizations to load times for users with large game libraries
- Added pinned notifications for new inventory items, trade offers, async game turns, moderator messages, offline chat messages, and help request replies in Quick Access  Notifications
- Added more buttons to the list of inputs that skip the BPM/Deck start up animations
- Changing download regions no longer requires restarting the Steam client
- UI Digital Navigation Key Repeats are faster
- Added setting for controller idle turn off timeout
- Navigation column in the Overlay is now centered vertically to match the rest of the main menu
- Various fixes to make the UI scale better in higher resolutions
- Fixed intermittent browser crash when closing Update news dialog
- Fixed background images on a collection on the app details page not being clipped correctly
- Fixed some issues completing purchases through some payment providers
- Fixed some UI scaling issues in the overlay when running in games in high resolution
- Fixed a case where disconnecting a controller while navigating would not cancel repeating movements
- Fixed issue opting in to some game beta branches
- Fixed issue viewing the hardware survey web page after submitting results
- Fixed audio crackling and loss when streaming from Linux / Steam Deck using Remote Play
- Fixed a and c keystrokes on the app details page triggering an animation

**Keyboard**
- Added up/down cursor keys to onscreen keyboard, press shift then left/right cursor to use
- Added ability to move the standalone & overlay keyboard
- Fixed issues w/ digital navigation getting stuck on text boxes when using a physical keyboard
- Fixed some issues using the virtual keyboard Paste button outside of a web context
- Fixed issue where the virtual keyboard would continuously be made visible after exiting a game

**Steam Input**
- Controller configuration browsing screen can now preview configurations and the selection processes now previews then applies instead of directly selecting the configuration
- Added a search tab to the controller layout browser screen
- Changed controller mode sliders to default to larger step sizes that match the old BPM interface and added footer button to switch to fine adjustment mode with smaller step sizes
- Reworked the layout of the mode settings page to show more content
- Generate Steam Input API origins for some virtual menu modes that were missing them
- Show controller settings in app properties game for non-Steam games
- Gyro Calibration Rework: Calibration Calculates an anti-drift value as normal, but also records Gyro and Accelerometer noise while stationary, so that Always-On Auto Calibration (toggle to enable) is more discerning, and should only recalculate anti-drift when on a stable surface
- Controller configurator now groups commands if they are attached to the same input
- Added support for the Armor-X Pro gamepad in PS4 mode
- Added direct navigation to controller inputs and modes from the preview screen
- Added a specific XBox Elite layout preview page
- Added a specific Switch Pro layout preview page
- Added support for the ThrustMaster eSwap PRO Controller Xbox
- Handle errors better and fix some cases where configs would no longer load
- On larger screens combine the keyboard and numpad tabs of the choose binding screen
- Remember the last active tab in the choose binding screen and open to that instead always using the tab w/ the current binding value
- Added upper grips as an option for mode shifts
- Improved Layout Preview for Nintendo Switch Joycon Left/Right/Pair
- Nintendo Switch SL/SR buttons now show up as Bumpers for single Joycons or Grip buttons for a JoyCon Pair
- Joycon individual/pair Gyro now displays and functions properly
- Filtered Mode Shift button options to only show available buttons based on the controller type
- Fixed an issue with the Joystick Deadzone sliders having delayed input
- Fixed an issue with gamepad navigation in the Steam Deck haptics calibration screen
- Fixed an issue w/ enabling Gyro for Switch controllers
- Fixed long delay at startup when the Razer Huntsman Elite keyboard is plugged in
- Fixed the Logitech G29 controller showing up as a gamepad instead of a wheel
- Fixed the XBox layout preview page layout having some incorrect items and missing others
- Fixed issue where Steam Controller joysticks would have unintended input during Steam Button chords
- Fixed long delay at startup when Razer keyboards are connected
- Fixed crash with games that use Windows Gaming Input
- Fixed issue w/ Joystick Deadzone visualization not updating
- Fixed some cases where some languages could have text overflow in choose binding screen
- Fixed chord activator options for XBox and XBox Elite controller types
- Fixed Capture button icon not being displayed for Joycon Pair
- Fixed the Switch Pro Layout Preview not showing the gyro

**Desktop Mode**
- Fixed a crash on Linux in libaudio
- Fixed crash when taking screenshots through the overlay
- Fixed instances of Steam freezing or crashing in desktop mode on Steam Deck
- Fixed closing non-Steam shortcuts via the overlay when two or more are running
- Fixed some errors causing the Library not to render properly

**Big Picture (while in Desktop Mode)**
- The new Big Picture Mode has been made the default experience.  For compatibility purposes, you can access the old experience by using the command-line option -oldbigpicture.  Note that this functionality will be removed in a future update.
- Added a quick guided tour
- Added option to start in windowed mode under Settings = Display = Big Picture Mode = Windowed
- Allow onscreen keyboard to be activated while in New Big Picture Mode and Steam window is not focused
- Added option to turn off controllers when exiting BPM
- Implemented Steam Controller dongle pairing
- Prevented launch option reminder from appearing on top of other UI while a game is launching
- Show icons for partial/full controller support, VR Support, or Mouse & KB only support in Library when a game portrait is focused or hovered
- Detect focus shifting away from the BPM window faster and reduce instances of navigation going to BPM after starting a game
- Hide the cursor when in gamepad-navigation mode in Big Picture
- Fixed a rare crash exiting BPM
- Fixed the new Big Picture Mode overlay being incorrectly sized when the monitor is set to display scaling other than 100%
- Fixed overlay scaling when resizing game window
- Fixed issue where a browser opened by a game was sticking around after closing the overlay
- Fixed launch options dialog not closing when cancelling game launch
- Fix the Start in Big Picture Mode setting not updating
- Fixed problem where setting certain library filters in Big Picture Mode could cause those games to become hidden when switching back to desktop
- Fixed an issue with detecting game windows

Patch notes can also be read on [Steam](https://store.steampowered.com/news/app/1675200/view/3635002625425792684).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
