+++
title = "Steam Deck Client Stable Fixes OSK In-Game, Fixes Overlay With Native Games (Plus Beta Update)"
date = 2022-12-02T00:04:52-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/client_updates/beta_11-21-2022.jpeg"
tags = ["news", "steam deck", "software update", "steam deck client update", "stable", "beta"]
keywords = ["steam deck", "steam deck client", "steam deck client update"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Yesterday's Deck client update (stable) is almost *all* fixes. Every bullet point except one starts with the word "Fixed." Fixes have been made for Steam Input, Remote Play, Desktop Mode, and in general. Patch notes are as follows:

**General**
- Fixed lock screen PIN reset process to not show PIN entry screen upon Steam Deck restart
- Fixed crash when touching gift or new inventory item notification
- Fixed "show password" toggle to show/hide the password.
- Fixed On Screen Keyboard no longer showing when requested by the game or Proton
- Fixed overlay causing crashes on some native games (Borderlands 2)
- Fixed an issue where context menus would not properly highlight focused items
- Fixed crash when exiting a 1-on-1 voice chat
- Fixed an issue where notification toasts would fail to appear

**Steam Input**
- Fixed a case where switching Virtual Menus w/ an action set, layer, or modeshift could cause them to stop working
- Fixed an issue introduced in a recent update to the old Big Picture configurator causing the names of new virtual menu bindings to be displayed incorrectly
- Fixed the L3 and R3 buttons not working on some third party PS3 controllers
- Fixed controllers being treated as Xbox One controllers by default when defining their layout
- Fixed the L3/R3 buttons not being detected for some third party PS3 controllers
- Added Left and Right Stick Deflection as an option for Gyro Activation Buttons. Stick deflection is no longer considered a part of "Touch" (Cap Sense) on SteamDeck.
- Fixed rumble for Switch Pro Controllers attached over USB

**Remote Play**
- Fixed getting the wrong personalization (colors, etc.) for streaming PS4 controllers
- Fixed streaming Bluetooth controllers not turning off

**Desktop Mode**
- Fixed size of content in Update news dialog when running with Windows text scaling >100%
- Fixed display of the Update News and other popup dialogs w/ GPU accelerated rendering disabled

Doesn't look like the [SteamOS 3.4 update with updated Arch packages](https://linuxgamingcentral.com/posts/steamos-3.4-preview-updates-arch-base/) arrived in this update. I suspect it has to do with [legal issues surrounding the fix for hardware decoding](https://github.com/ValveSoftware/SteamOS/issues/903). The updated Arch packages probably won't show up on stable until this gets fixed.

In addition to the stable client update, an update was shipped to the beta/preview branches on Wednesday. More fixes? Yes, indeed:
- additional crash logging
- fix to input device handling
- fixed an issue where context menus would not properly highlight focused items
- fixed crash when exiting a 1-on-1 voice chat
- fixed an issue where notification toasts would fail to appear

See the patch notes for the stable update [here](https://store.steampowered.com/news/app/1675200/view/3647382450216885311?l=english), and the beta update [here](https://store.steampowered.com/news/app/1675200/view/3647382450216851865?l=english).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
