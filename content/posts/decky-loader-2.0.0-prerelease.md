+++
title = "Decky Loader (formerly known as Plugin Loader) 2.0.0 'React' Released, Updates the Web-Based Plugin Store with React"
date = 2022-07-04T22:25:59-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/screenshots/power_tools.webp"
tags = ["news", "software update", "steam deck"]
keywords = ["steam deck", "plugins"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
The Plugin Loader for the Steam Deck is now known as [Decky Loader](https://github.com/SteamDeckHomebrew/decky-loader), and along with the new name change come a few updates. Primarily we're looking at a React-based plugin store now, which, per the [pull request](https://github.com/SteamDeckHomebrew/decky-loader/pull/81), "replaces the web-based plugin store with a native-feeling one." It's also now possible to uninstall Decky Loader. Full patch notes are as follows:
- Uninstall script addition by @ggppjj in #48
- Use unique ids in call_server_method by @patkub in #55
- react: Add Router hook & fix typescript issues by @AAGaming00 in #68
- Add contributor install script by @TrainDoctor in #69
- Implement React-based plugin store by @AAGaming00 in #81
- remove body property in args by @hulkrelax in #91
- Uninstall functionality by @botatooo in #97
- Use deckyState in uninstall menu (fixes #98) by @botatooo in #100
- Fixed plugin installation ssl verification issue by @WerWolv in #101

Keep in mind **this is a pre-release**. Also SDH-Toolbox and some legacy plugins no longer work. Hopefully it won't be long before we're able to work with the plugins with the Deck's built-in controls rather than the touchscreen exclusively.

See the patch notes on [GitHub](https://github.com/SteamDeckHomebrew/decky-loader/releases/tag/v2.0.0-pre), and if you want a guide on getting plugins set up on your Deck, look no further than LGC's [guide](https://linuxgamingcentral.com/posts/steam-deck-plugins/).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
