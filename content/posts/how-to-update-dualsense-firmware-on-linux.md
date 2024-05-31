+++
title = "You Can Update the Firmware for Your DualSense on Linux. Here's How"
date = 2022-04-21T09:01:10-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/guide_ds_fw_updater/cover.jpg"
tags = ["guide", "dualsense"]
keywords = ["wine", "bottles", "dualsense", "playstation"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Most of you who read the headlines are probably aware of the fact that as of yesterday, [you no longer need to own a PS5 in order to update the firmware on your DualSense gamepad](https://controller.dl.playstation.net/controller/lang/gb/fwupdater.html). It's now possible to upgrade the FW on your Windows PC.

But I've noticed that, even though some have [claimed to get the FW updater to work on Linux via Wine](https://www.reddit.com/r/pcgaming/comments/u7r53s/comment/i5ic3dt/?utm_source=share&utm_medium=web2x&context=3), I didn't have such luck myself. That is, until I finally figured it out, based on some hints by fellow Redditors. You can update the FW on Linux too, and here's the step-by-step process.

**TL;DR**:

1. Download Sony's FW updater [installer](https://controller.dl.playstation.net/controller/lang/gb/fwupdater.html)
2. Install [Bottles](https://usebottles.com), run it, then close it
3. Download the latest release of [wine-ge-custom](https://github.com/GloriousEggroll/wine-ge-custom/releases), extract the tarball to `~/.local/share/bottles/runners/`
4. Create a new Bottle with the Bottles application, select "Custom," use the `lutris-GE-Proton` runner
5. Direct the newly created Bottle to the FW installer, install the app, ignore the .NET warning
6. Run the app!

*NOTE: some have had success using Proton Experimental and adding the installer as a non-Steam game, so your mileage may vary. I've found the only solution that works for me is to use wine-ge-custom (AKA lutris-ge-custom) with Bottles.*

First, you're going to want to head over to [PlayStation's website](https://controller.dl.playstation.net/controller/lang/gb/fwupdater.html) and download the installer. Next, install [Bottles](https://usebottles.com/). Bottles, as the documentation for it brings out, "allows you to easily manage Windows prefixes on your favorite Linux distribution." Kind of think of it like Lutris, but with a more simplified interface. You can install Bottles as a [Flatpak](https://flathub.org/apps/details/com.usebottles.bottles), get it from the [AUR](https://aur.archlinux.org/packages/bottles) if you're on Arch, or by [other means](https://docs.usebottles.com/getting-started/installation#other-packages).

Launch Bottles. Bottles will need to download some important packages for the sake of running your bottles, including:

- Caffe runner
- DXVK
- VKD3D
- NVAPI
- LatencyFleX
- Runtime

Let it do it's thing, then you should be presented with something like this:

![bottles create a new bottle page](/images/guide_ds_fw_updater/create_a_bottle.jpg)

Close the application for now, we're going to need [wine-ge-custom](https://github.com/GloriousEggroll/wine-ge-custom) in order to get the FW updater to properly work and detect the controller when it's connected via USB. Head to the [Releases](https://github.com/GloriousEggroll/wine-ge-custom/releases) section, download the latest tarball, and extract the contents to `~/.local/share/bottles/runners/`. This will allow Bottles to make use of said runner.

Open Bottles again. Go ahead and click the button: "Create a new Bottle."

With the new window, we can give our Bottle a name, as well as assign it a Gaming environment, an Application environment, or a custom one. We're going to want to use "Custom," as we're going to make this Bottle use the `wine-ge-custom` runner we just downloaded. So after clicking "Custom," we will be presented with some advanced customization options. All we need to do is under the Runner dropdown list, select `lutris-GE-Proton` + whatever version was downloaded. In my case it's `lutris-GE-Proton7-8-x86_64`. That's all we need to customize for this Bottle, now click "Create."

![bottles custom bottle](/images/guide_ds_fw_updater/custom_bottle.jpg)

Give it some time, as this will update the Bottle's Wine configuration. After closing the window, the main window should now display your new Bottle:

![bottles new bottle](/images/guide_ds_fw_updater/new_bottle.jpg)

Click the newly created Bottle and click "Run executable." Your file manager will open. Find the installer you had downloaded earlier. Go through the installation process. The installer requires the .NET 4.8 framework. Chances are the installation of this requirement will fail, but you can proceed with the installation.

![DualSense FW installer](/images/guide_ds_fw_updater/fw_updater_installer.jpg)

If you want you can check the box for "Launch program" at the last window to immediately launch the FW updater. If you decide not to do this you can run the app any time by clicking the play button under "Programs."

![Bottles FWupdater](/images/guide_ds_fw_updater/fwupdater_option.jpg)

The FW updater should now open:

![FW Updater main window](/images/guide_ds_fw_updater/fwupdater_main_screen.jpg)

Plug in your DualSense to a USB port. In my experience it doesn't matter whether it's connected to USB 2 or 3. The app will let you know if your gamepad is using outdated FW; if it is, it will prompt you to download and install the new FW. Don't disconnect the USB cable during the FW upgrade process!

![FW Updater new update available](/images/guide_ds_fw_updater/new_fw_available.png)

Looks like there's a new FW update available for my DualSense. I just click on "Update Now," then there will be a progress bar. A few minutes later, done:

![FW Updater up-to-date](/images/guide_ds_fw_updater/fw_up_to_date.jpg)

There you go! Now you can enjoy...whatever latest features Sony packed into their gamepad. Yeah, unfortunately (but also unsurprisingly) Sony hasn't detailed what each FW update does. I searched high and low for any patch notes but couldn't find any. Supposedly, [according to someone on Reddit](https://www.reddit.com/r/linux_gaming/comments/u80n5i/comment/i5kuqev/?utm_source=share&utm_medium=web2x&context=3), newer FW "improves battery life and legacy rumble emulation," but I haven't spent enough time to confirm either case. I'll definitely take the longer battery life though; it's surprisingly short despite the capacity being larger than the DS4.

*Cover image credit: isenacode.com*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
