+++
title = "Enhance Your Steam Deck Experience with Plugins"
date = 2022-06-24T07:55:00-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/screenshots/power_tools.webp"
tags = ["steam deck", "plugins", "guide", "decky loader"]
keywords = ["steam deck", "plugins"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Ever wanted to quickly launch Flatpak applications from the Quick Access menu without having to add them as shortcuts on Steam in Desktop Mode? Or automatically enable the night light when it's the right time? Or customize the CPU frequency? Play music? Customize the Home screen to look like the Switch's home menu? That's all possible thanks to Steam Deck plugins. 

The best part: just run a few commands from the terminal, and install your plugins from the [plugins "store."](https://plugins.deckbrew.xyz/) That's it. No need to have a specially-crafted RCM jig and taking apart the back of the Deck and soldering it somewhere on the motherboard and mucking about with SD cards. No need to tap the volume button 10 times to activate developer mode. Such is the beauty of the open-source nature of Linux and Valve's open-ness concerning the Steam Deck.

# Get the Plugin Loader
We'll first need to enable Developer Mode on the Deck, as well as CEF (Chromium Embedded Framework) Remote Debugging. CEF Remote Debugging will allow us to add web browsing functionality within the Steam Deck client (plugins use a combination of HTML and Python). To do so, do the following:
1. Tap the Steam button while in Game Mode, go to Settings
2. Under System -> System Settings enable dev mode with the appropriate toggle
3. A new option should now be available at the bottom of the sidebar: Developer. Go to it
4. Under Miscellaneous, toggle CEF Remote Debugging on

![cef toggle](/images/steam_deck/screenshots/cef.jpeg)

Now we'll need to go to Desktop Mode. Open a terminal (you may want to have a keyboard attached) and set a root password with `passwd`. Simply pass this command to the terminal and you'll be prompted to create a new password if you haven't already. After that, input this command:

`curl -L https://github.com/SteamDeckHomebrew/PluginLoader/raw/main/dist/install_release.sh | sh`

You'll be asked to enter the password you just created earlier. That's it! Now we can install plugins.

# Get Plugins
If you switch back to Gaming Mode, you should now have a new icon on the Quick Access menu:

![plugins from quick access menu](/images/steam_deck/screenshots/plugins.jpeg)

Unlike my screenshot though, your list of plugins will be empty. As of version 1.3 of the Plugin Loader, we no longer need to manually copy plugins over in Desktop Mode. If you tap the little shopping bag on the upper-right, you'll be taken directly to the plugin "store." You can see all the available plugins, what they do, and if you tap the blue "Install" button, it will install the plugin you selected. If you want an older version of the plugin for whatever reason, you can tap the arrow icon to the right of the button and select the version from the dropdown list.

If you wish to copy the plugins over manually, just download the plugin from the project's GitHub page while in Desktop Mode, and extract the release to `/home/deck/homebrew/plugins/`.

Once a plugin is installed, it should now appear in the Quick Access menu. From there you can tap the plugin for more options. As an example, once I tap CSS Loader, I'll now have a list of options for different themes/customizations for my Steam Deck library:

![css loader](/images/steam_deck/screenshots/css_loader.jpeg)

I can make my Home screen look similar to the Switch's UI and make it less cluttered. I can also enable the classic Steam theme, customize the color of the toggles, and add more Steam library icons by reducing the space between them.

# Recommended Plugins
I like the **CSS Loader** since I can make the toggles in Game Mode red. The "More Library Icons" toggle can be a bit glitchy at times when browsing through my Steam games. If you have familiarity with CSS you can add your own themes as well (I might work on a black and red theme at some point).

**Auto Night Mode** certainly helps when you're in bed and you don't have to manually put the toggle on every time you want to put it to use.

**Quick Launch** is definitely useful for running any Flatpak-based application you have installed on your handheld without having to go to Desktop Mode and adding a shortcut for the app on Steam.

You may want to have a look at **Power Tools** if you want to control the fan speed, limit the number of threads in the APU, or change the max frequency. Useful if you want to squeeze as much battery life as you can for games that aren't graphically intensive. But be careful: you might overheat your system if you limit the fan speed!

There's a plugin called **Extra Settings**. This allows you to enable SSH and turn Transparent Huge Pages (THP) on or off. Supposedly with the latter enabled, it can lead to [performance improvements](https://www.reddit.com/r/linux_gaming/comments/uhfjyt/underrated_advice_for_improving_gaming/). I'm here to tell you, after I benchmarked *GRID (2019)* and *Shadow of the Tomb Raider* with THP on and off, the difference is so small (2 FPS) that it's frankly not going to be useful. But I keep the plugin anyway for SSH, which is helpful for running terminal commands on the device with my desktop.

![extra settings](/images/steam_deck/screenshots/extra_settings.jpeg)

**DeckBattery** is useful if you wanted detailed stats about the battery.

All available plugins for the Deck can be found at [plugins.deckbrew.xyz](https://plugins.deckbrew.xyz/) and are open-source.

# Plugins Menu only Works with Touch
Unlike the rest of the Quick Access menu, the Plugins section does *not* work with the buttons. You can only use touch for now.

# Want to Make a Plugin?
There's no development documentation, but you can make use of the [Plugin Template](https://github.com/SteamDeckHomebrew/Plugin-Template) to get started. You'll need some Python and HTML skills. When publishing your plugin, you can put it under whatever license you prefer.

Any other plugins that you'd recommend? Let me know!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
