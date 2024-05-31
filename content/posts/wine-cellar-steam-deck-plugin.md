+++
title = "Easily Install GE-Proton, Luxtorpeda, and Boxtron on Steam Deck with Wine Cellar"
date = 2023-10-05T15:42:22Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/plugins/wine-cellar/about.jpg"
tags = ["steam deck", "steam deck plugin", "wine cellar", "decky loader"]
keywords = ["wine cellar", "ge-proton", "proton-ge", "steam deck", "steam deck plugin", "decky loader", "luxtorpeda", "boxtron", "decky wine cellar"]
description = "All within the comfort of Game Mode."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
One recent plugin that I came across after I had installed Decky Loader on my Steam Deck was [Wine Cellar](https://github.com/FlashyReese/decky-wine-cellar). And holy crud, it's made installing the latest version of GE-Proton *so* much easier. Not that I'm giving any crap to ProtonUp-Qt; that's still a spectacular tool, but that's more so for being used in Desktop Mode. With Wine Cellar, you can download and install the latest version of GE-Proton, Luxtorpeda, and Boxtron all within the comfort of Game Mode. No need to switch over to Desktop Mode.

Just as a reminder, if you're not familiar with either [Luxtorpeda](https://github.com/dreamer/luxtorpeda) or [Boxtron](https://github.com/dreamer/boxtron), the former will allow games to run with native Linux engines, while the latter runs DOS games with the native Linux DOSBox build.

# Installation
If you haven't installed Decky Loader already, go to the [GitHub page](https://github.com/SteamDeckHomebrew/decky-loader) with your browser in Desktop Mode, and click the Download button to get started. Go back to Game Mode, press the QAM button, navigate down to the plugin icon, then go to the plugin store on the top right. Go all the way down the list until you find Wine Cellar. Press Install and you're good to go.

![Wine Cellar in Plugin Store](/images/steam_deck/plugins/wine-cellar/plugin_store.jpg)

# Usage
After the plugin has been installed, navigate to it from the QAM. Select Wine Cellar from the list of installed plugins and press A. Press A on "Manage". From here you can see what versions of Steam Play compatibility tools you may have installed already. If you press A over on the three-dotted icon, a context menu will show up where you can easily read the patch notes for that particular version, or uninstall the compatibility tool if you wish.

![GE-Proton8-16 installed, restart required](/images/steam_deck/plugins/wine-cellar/dashboard.jpg)

So let's say you wanted to install the latest version of GE-Proton. Select "ProtonGE" from the navigation bar, and from the "Not Installed" list, select the version you want to install. Press A on the three-dotted button to install or read the patch notes. The plugin will take care of downloading and extracting the compatibility tool to the appropriate directory. This same concept applies to installing Luxtorpeda or Boxtron.

After a compatibility tool is installed, you will be prompted to restart Steam if you select the three-dotted button from the freshly installed compatibility tool. Do so in order for Steam to pick up the new tool.

![GE-Proton8-16 patch notes](/images/steam_deck/plugins/wine-cellar/patch_notes.jpg)

On the About page you can check for plugin updates, visit the project's [GitHub page](https://github.com/FlashyReese/decky-wine-cellar), where you can have a look at the source code, join the project's [Discord](https://discord.gg/MPHVG6MH4e), or support the creator, FlashyReese, via [Ko-Fi](https://ko-fi.com/flashyreese). What's neat is there is a QR code for each option, making it very easy to submit an issue, join the Discord, or support the author of the plugin.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
