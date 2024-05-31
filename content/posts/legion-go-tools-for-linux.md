+++
title = "Give Your Legion Go the Steam Deck-Like Experience - Without Using Windows"
date = 2023-12-17T19:30:20Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/legion_go/legion-go-tools/cover.jpg"
tags = ["legion go", "chimeraos"]
keywords = ["lenovo legion go", "legion go", "linux on legion go", "chimeraos", "chimeraos on legion go"]
description = "Feature parity is pretty close to that of the Steam Deck!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
The Legion Go hasn't even been out for two months and, I've been impressed how quickly the community has been able to get the enormous, Switch-like handheld to work on operating systems *outside* of Windows.

I'd say we're about 90% there as far as feature-parity with the Steam Deck. A little over a month ago I had written down some quick thoughts on [the state of Linux support for the Legion Go.](https://linuxgamingcentral.com/posts/chimeraos-on-legion-go/). At that time, the Guide or QAM menus couldn't be accessed without using a workaround. The TDP couldn't be adjusted through the software itself. Gyro wasn't working OOTB. The RGBs surrounding the sticks couldn't be turned off. And sometimes the screen flickered erratically, depending on what you were doing.

I'm happy to report those issues have been fixed now. [Aarron Lee](https://aarronlee.com/) made a couple of Decky plugins that allow you to [adjust the TDP](https://github.com/aarron-lee/SimpleDeckyTDP), while also giving the user the ability to [turn the RGBs on or off](https://github.com/aarron-lee/LegionGoRemapper/). The RGBs can even be customized with a brightness slider, and can have this "breathing" effect that changes to different colors, if you so choose. The RGB plugin also allows you to remap the back buttons, and enable/disable the trackpad. Interestingly enough you can also remap the gyro to the left or right control stick. Be aware that, if you're using the TDP plugin and set the TDP anything higher than 35 W, the performance will tank.

![SimpleDeckyTDP plugin screenshot](/images/legion_go/legion-go-tools/color-picker.png)

As far as the Guide and QAM controls, those have been fixed via [HandyGCCS](https://github.com/ShadowBlip/HandyGCCS) (handheld game console controller support). This software is already baked into ChimeraOS if you've updated to the latest unstable version. Guide can be accessed by holding Legion L + B, and the QAM can be accessed with Legion L + A. Suspending the device no longer requires going to Steam's menu; you can simply press the Power button now and the device should properly suspend.

As far as gyro support, that's been a little iffy, at least on my end. There's this "hack" that you can apply that makes the Legion Go emulate as a DualSense Edge controller. You can install this with [ROGueENEMY](https://github.com/corando98/ROGueENEMY/). This will supposedly allow the gyro to work. It also switches Legion L and Legion R to Start and Select respectively, and changes the bottom left buttons as Guide and QAM. The back buttons are also supported. While the button glyphs in Steam will change into the PS5 icons, you can change this back to Xbox-style via a [CSS Loader theme](https://github.com/frazse/PS5-to-Xbox-glyphs).

There's an enhanced version of ROGueENEMY called [Handheld Daemon (HHD)](https://github.com/antheas/hhd). Problem is, neither this or ROGueENEMY has been working on my end to get the gyro working. I'm not sure if there are any additional steps required to activate the gyro after installation. I'm not seeing "Gyro Calibration" under Steam -> Settings -> Controller -> Calibration & Advanced Settings.

![Legion Go theme for CSS Loader](/images/legion_go/legion-go-tools/legion_go_theme_for_css_loader.png)

Finally, there's [steam-patch](https://github.com/corando98/steam-patch), although this has been pretty buggy for most users. Essentially installing this will do the following:
- fixes the TDP and GPU clock speed modifiers from the QAM
- replaces the Xbox controller glyphs in Steam to more closely resemble the Steam Deck controller glyphs, for a more consistent look

For the time being, I don't recommend installing this, as I've had a few issues using it. Additionally it will likely conflict with ROGueENEMY/HHD.

# Putting the Tools All Together
Since there are quite a few community-made projects made for the Legion Go, I decided to polish up my bash scriping skills and made a [tool](https://github.com/linuxgamingcentral/legion-go-tools-for-linux) that brings all the projects together. With this, you can now easily install all of the aforementioned tools without having to open up a bunch of tabs in your web browser with a different GitHub page on each one. Be aware that, for the time being, this script was primarily made with ChimeraOS in mind. It *might* theoretically work on other Arch-based distros, but I haven't tested.

The script allows you to install, update, or uninstall the following:
- Decky Loader
- SimpleDeckyTDP plugin
- LegionGoRemapper plugin
- ROGueENEMY
- HHD
- steam-patch
- Legion Go theme for CSS Loader
- PS5-to-Xbox controller glyphs theme for CSS Loader

Literally all you have to do to run the script is by going to Desktop Mode and run the following command in a terminal:

`curl -L https://raw.githubusercontent.com/linuxgamingcentral/legion-go-tools-for-linux/main/lego_chimera.sh | sh`

I also have a .desktop file there on the GitHub repo if you want to save that for easy access to the program, but GNOME doesn't work the same with .desktop files as it does with KDE on Steam Deck. If you try opening the .desktop file on ChimeraOS, it will just open up the file with a text editor as opposed to actually running the command.

Type your sudo password when prompted, and you should be presented with a list of tools to install or remove:

![Legion Go Tools for Linux](/images/legion_go/legion-go-tools/legion-go-tools-for-linux.png)

# Remaining Issues
ChimeraOS is pretty much usable as a daily driver for the Legion Go (so long as you're using the unstable build). The community has also used [Nobara Project](https://linuxgamingcentral.com/posts/nobara-project-impressions/) and [Bazzite](https://github.com/ublue-os/bazzite/) and have reported similar experiences, although these distros come with their own set of issues.

Some caveats to be aware of, for now:
- the battery indictor still doesn't work -- Steam will report it as always being full even if that's not the case
- you can't push the framerate beyond 72 FPS unless you turn off Unified Frame Limit Management and disable the framerate limit in the QAM
- only 60 Hz and 144 Hz refresh rate options work. Setting the refresh rate to anything else will make the screen garbled. You will likely need to use an external monitor to change the refresh rate back
- gyro can be hit-or-miss. You might be able to get it to work after installing ROGueENEMY or HHD, you might not

# Keeping Up-to-Date with Legion Go Linux Support
While I will try to keep readers up-to-date as far as Linux support on the Legion Go, the best place for that is by going to [Aarron Lee's GitHub page](https://github.com/aarron-lee/legion-go-tricks). This document is constantly updated with the latest information as far as:
- what works
- what's available for workarounds
- issues and known bugs
- resources -- such as available tools to enhance the Legion Go experience
- videos
- guides and small fixes

Thanks go to Aarron Lee, corando98, Antheas, frazse, and everyone else who has contributed to making Linux on the Legion Go a better experience.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
