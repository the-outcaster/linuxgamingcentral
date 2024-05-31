+++
title = "Open Gamepad UI - Open-Source Game Launcher"
date = 2023-04-10T18:08:52Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/opengamepadui/cover.webp"
tags = ["opengamepadui", "software spotlight"]
keywords = ["open gamepad ui", "open-source game launcher", "godot 4"]
description = "A neat game launcher written in Godot 4 - but needs quite a bit of work."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
I know, I know -- this is probably the umpteeth game launcher you've heard about. You probably can't help but think of that [web comic](https://xkcd.com/927/) where there are 14 competing standards, but someone says, "We need to develop one universal standard that covers everyone's use cases." Then soon thereafter there are 15 competing standards.

But this one in particular holds a special place in my heart, because this project was created by some of the [ChimeraOS](https://linuxgamingcentral.com/tags/chimeraos/) developers. It's called [Open Gamepad UI](https://github.com/ShadowBlip/OpenGamepadUI/). From the project description on GitHub:
> Open Gamepad UI is a free and open source game launcher and overlay written using the Godot Game Engine 4 designed with a gamepad native experience in mind. Its goal is to provide an open and extendable foundation to launch and play games. It also implements a gamepad input system that can allow you to remap gamepad input to mouse and keyboard inputs.

It also offers some advantages that other game launchers don't have:
- integrates [Gamescope](https://github.com/ValveSoftware/gamescope)
- the overlay apparently works with *all* games
- has gamepad mapping/input translation

![OpenGamePadUI update](/images/opengamepadui/updates.webp)

Open Gamepad UI is available in the [AUR](https://aur.archlinux.org/packages/opengamepadui-bin), and there's also a .desktop file on the [Releases](https://github.com/ShadowBlip/OpenGamepadUI/releases) for easy installation on Deck. Otherwise, other distros can follow the instructions for [installing the binary](https://github.com/ShadowBlip/OpenGamepadUI/blob/main/docs/install/INSTALL_BINARY.md). The binary can be installed system-wide, as a systemd extension for immutable distros, or locally in your home directory.

Basically, think of Open Gamepad UI as a launcher for your Steam games. You can also launch Heroic Games Launcher from here, if it's installed on your system, as well as some other applications. Non-Steam games don't seem to show up in the library.

Currently there's four plugins that you can install and use:
- Steam -- installing this and logging into your Steam account will give you access to more of your Steam library
- SteamGridDB -- for giving the games in your library the proper artwork
- Recapture -- for capturing gameplay footage
- Flathub -- browse for Flatpaks from Flathub

![OpenGamePadUI Plugins](/images/opengamepadui/plugin_store.webp)

Documentation is available should you want to [make your own plugin](https://github.com/ShadowBlip/OpenGamepadUI/blob/main/docs/PLUGINS.md).

There's this neat little animation that plays when the launcher is run, and there's some sound effects to boot when navigating across the UI. A different animation plays when a game is being launched. Updates can be seamlessly run through the General tab in the Settings menu.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/opengamepadui/opengamepadui.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

But keep in mind, this launcher needs quite a bit of work. The GitHub even states this:
> This project is currently in the very early stages of development.

# Issues to Keep in Mind
The support of both gamepads and the keyboard + mouse is honestly atrocious at the moment. I think the launcher is extremely sensitive to the movements of my mouse. As a result, sometimes I can't even navigate the menus with my DualSense because the launcher thinks I'm using the mouse/keyboard. The launcher icons constantly shift between the DualSense and the keyboard/mouse. The guide button on the DualSense doesn't even work -- it won't bring up any of the menus.

If you want to exit the launcher, you'll probably need to press Alt + F4. If you select "Exit" from the launcher's menu, the launcher will just hang, and the only way you'll be able to close it is by killing the `gamescope-wl` process.

![OpenGamePadUI launch arguments](/images/opengamepadui/launch_arguments.webp)

For some reason, a few of your Steam games will be present in your library, but not all of them. You'll need to install the Steam plugin and log into your Steam account to see all of your games.

SteamGridDB is kind of weird how it behaves -- you'll need to go to SteamGridDB's website and [obtain an API key](https://www.steamgriddb.com/profile/preferences/api). You'll need to copy the API key and put it into the appropriate field in Open Gamepad UI to use it. From there, missing artwork for *most* of your games should now be showing up in your library, but as far as I can tell, you can't customize the artwork.

![OpenGamePadUI SteamGridDB](/images/opengamepadui/steamgriddb.webp)

The "Store" tab doesn't even work -- if you go to it, you'll just be greeted with a blank page.

And keep in mind the overlay just doesn't seem to work while in-game, at least with a DualSense. I'll need to test with my Xbox pad to see if that works, but PS5 controllers are a bit iffy. Also know that you can't change Proton versions.

There's a page in the launcher where you can customize the controller configuration, but on desktop it shows a Steam Deck. I also can't change the button behavior to use a different gamepad button, for some reason. I can only make a button use a mouse or keyboard input event. Otherwise, I'm stuck with the default button layout.

![OpenGamePadUI controller layout](/images/opengamepadui/gamepad_template.webp)

So yeah, I'd wait a while for the software to mature a bit before you use this, but it's a pretty interesting project nonetheless.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
