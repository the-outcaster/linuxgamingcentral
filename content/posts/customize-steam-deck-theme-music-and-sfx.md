+++
title = "How to Customize Steam Deck's Theme, Background Music, and Sound Effects"
date = 2023-02-07T18:17:38Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/guides/customizing_steam_theme_bgm_and_sfx/clean_gameview.jpeg"
tags = ["guide", "steam deck", "audio loader", "css loader", "decky loader"]
keywords = ["steam deck", "steam deck decky loader", "steam deck custom sound effects", "steam deck custom bgm", "steam deck custom theme"]
description = "It's so easy that your grandmother could do it."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
The Deck UI is a much-needed replacement for the old Big Picture interface. But at times, you might get...bored of the interface after a while. Maybe you want to make it reminiscent of the Wii days. Maybe you want a darker theme so it's easier on your eyes. Maybe you want to spice up the font a little bit, or have a less cluttered Home screen.

Well, this is all possible, thanks to [CSS Loader](https://github.com/suchmememanyskill/SDH-CssLoader). Not only this, but you can add background music as well, and change the sound effects when navigating across different options. Let's get started.

# 1. Get Decky Loader
If you don't already have Decky Loader installed on your Deck, go to Desktop Mode. Navigate to the [Decky Loader GitHub page](https://github.com/SteamDeckHomebrew/decky-loader) with your web browser. Click the "Download" button and install Decky Loader. There's not much more to it than that; the developers have made it easier than ever to get this homebrew plugin launcher working.

![Decky Loader](/images/steam_deck/guides/powertools/decky_loader_github_page.webp)

# 2. Install CSS Loader and Audio Loader
CSS Loader allows us to override Steam's CSS ([cascading style sheet](https://www.w3schools.com/html/html_css.asp)) code, therefore giving it a fresh coat of paint. [Audio Loader](https://github.com/EMERALD0874/SDH-AudioLoader), if it wasn't obvious by the name, allows us to run custom background music while Steam is running, and customize the UI sound effects.

![Decky Loader](/images/steam_deck/guides/customizing_steam_theme_bgm_and_sfx/decky.jpeg)

To install these plugins, go back to Game Mode. Open the Quick Access Menu (QAM). There should now be a plugin icon on the bottom. Navigate to it, and then select the shopping icon on the top-right. From there, you can browse and install any plugins that are available, including the CSS and Audio Loaders. Just press A on the Install button, and the plugin should be installed in a matter of seconds.

![Decky Loader store](/images/steam_deck/guides/customizing_steam_theme_bgm_and_sfx/decky_loader_store.jpeg)

Once these plugins are installed, they should appear in the QAM:

![Decky Loader plugins](/images/steam_deck/guides/customizing_steam_theme_bgm_and_sfx/installed_plugins.jpeg)

# 3. Customize the Steam Theme
Access CSS Loader from the QAM. There shouldn't be anything there on the first install besides "Download Themes".

There's lots of different things we can customize, from the system-wide theme, to OSK tweaks, to library icons, to the font, the lock screen, and many others. So I'd recommend setting the filter to the setting that you want to customize, such as "System-Wide", then adjusting the sorting filter to "Most Stars" or "Most Downloaded" so you're not overwhelmed with the plethora of options available. You can also use the search bar if you're looking for something specific, and use the slider on the right to adjust the number of icons there are per row.

![CSS Loader home](/images/steam_deck/guides/customizing_steam_theme_bgm_and_sfx/css_loader.jpeg)

Let's say you find something you like, such as the Wii theme. Select it with the A button, then select Install to install said theme.

![CSS Loader Wii theme](/images/steam_deck/guides/customizing_steam_theme_bgm_and_sfx/wii_theme.jpeg)

This should now show up in the QAM. Now you can easily turn the theme on or off with the toggle.

![CSS Loader Wii theme toggle](/images/steam_deck/guides/customizing_steam_theme_bgm_and_sfx/toggle_theme.jpeg)

Here's a few screenshots with the Wii theme enabled:

![CSS Loader Wii theme home](/images/steam_deck/guides/customizing_steam_theme_bgm_and_sfx/wii_home.jpeg)

![CSS Loader Wii theme game description](/images/steam_deck/guides/customizing_steam_theme_bgm_and_sfx/wii_game_desc.jpeg)

From here you can customize the theme a bit further, including what color you want the toggles to be, whether clean gameview is enabled or not, more library icons, etc. There's too many to list, but here's a few of my recommendations:
- center game text -- by default the title text by a game isn't centered, so this fixes that
- centered home -- this gets rid of the What's New, Friends, and Recommended tabs on the bottom of the Home screen
- clean game view -- hides the tabs that are present at the bottom of a game page and enlarges the game art to fit the entire screen
- colored toggles -- this allows you to change the default blue color for Steam's toggle options
- customize the font to make the Deck more "personal" to you
- more library icons -- does as it says; fits more icons in your library on a per-row basis
- no Deck badge -- gets rid of the Deck icon for your games; I find the icon to be unnecessary
- no Home edge fade
- round avatar status
- Switch-like Home -- cleans up the Home screen a bit to make it less cluttered

With these options enabled, here's what Steam will look like:

![CSS Loader Wii home theme more customized](/images/steam_deck/guides/customizing_steam_theme_bgm_and_sfx/wii_home_more_customized.jpeg)

![CSS Loader clean game view](/images/steam_deck/guides/customizing_steam_theme_bgm_and_sfx/clean_gameview.jpeg)

To uninstall or update a theme, go to the Installed Themes tab. From there you can either update a theme if there is one available (which doesn't work for me for some strange reason), or uninstall it.

![CSS Loader update or remove a theme](/images/steam_deck/guides/customizing_steam_theme_bgm_and_sfx/installed_themes.jpeg)

# 4. Customize BGM and SFX
Access Audio Loader from the QAM. Go to "Manage Packs" to download and install tracks and sound effects.

From here you can filter to see BGM or SFX, or both. As with CSS Loader, installation is as simple as going to the BGM/SFX that you want, then pressing the Install button. Some tracks I'd recommend downloading:
- DSi menu music
- GameCube menu music
- PS2 ambience
- PSVita menu
- Wii menu music -- compliments the Wii theme very well
- original Xbox music pack
- Wii U system setup/settings/Mii maker menu/main menu/Friends theme/Download management
- PS5/PS4 home menu
- watch music from *Goldeneye 64*
- 3DS Internet settings

![Audio loader store](/images/steam_deck/guides/customizing_steam_theme_bgm_and_sfx/audio_loader_store.jpeg)

SFX recommendations would be as follows:
- GameCube menu SFX
- Zelda BoTW SFX
- PS5 sounds
- Switch sounds
- *Smash Bros. Brawl* SFX
- Wii menu sounds -- again, fits the Wii theme even more
- original Xbox sound pack
- *Cuphead* SFX
- BPM SFX -- if in the event you want to re-live the old BPM's SFX
- PS4 SFX
- XMB SFX
- PS2 SFX
- *Sonic the Hedgehog* SFX

After you have the BGM and SFX installed, you can select them at any time by going to the dropdown menu in Audio Loader, and selecting the option of your choice. You can change the volume of both the BGM and SFX, so if one sounds louder over the other, you can fine tune the volume to your liking. BGM automatically stops playing when a game is launched, then played again when exiting the game, so no need to worry about that.

![Audio loader settings](/images/steam_deck/guides/customizing_steam_theme_bgm_and_sfx/audio_loader.jpeg)

In the event you want to uninstall any tracks or sound effect packs, simply head to the Uninstall tab in the Audio Loader store and select the Trash icon to remove it.

![Audio loader uninstall music/SFX packs](/images/steam_deck/guides/customizing_steam_theme_bgm_and_sfx/uninstall_audio.jpeg)

# Want to Make Your Own Theme, Music Pack, or SFX?
There's [documentation](https://docs.deckthemes.com/#/CSSLoader/README?id=%f0%9f%8e%a8-creating-a-theme) for making your own theme. You'll need some basic CSS and JSON skills. Documentation is also available for [adding your own BGM or SFX](https://docs.deckthemes.com/#/AudioLoader/README). Should you want others to enjoy your theme, music, or SFX, you can submit it, but be sure to check the [criteria](https://docs.deckthemes.com/#/Submission?id=submit-to-deckthemescom) first before doing so.

If you want I have [*Melee* SFX](https://github.com/linuxgamingcentral/melee-sfx) and [BGM from the Snes9xGX Wii app](https://github.com/linuxgamingcentral/snes9xgx-bgm); just too lazy to submit it. Just go to the repo, click the green "Code" button, select "Download ZIP". Extract the zip files to `~/homebrew/sounds/` and they should now appear as options in the dropdown menus.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
