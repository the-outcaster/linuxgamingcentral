+++
title = "Lenovo Legion Go - Can it Linux?"
date = 2023-11-03T17:16:32Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/legion_go/chimeraos/cover.jpg"
tags = ["chimeraos", "legion go"]
keywords = ["lenovo legion go", "legion go", "linux on legion go", "chimeraos", "chimeraos on legion go"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
After picking up a 512 GB Legion Go from Micro Center on Tuesday, naturally I wanted to see how well the device would perform with Linux. For this, I went with [ChimeraOS](https://linuxgamingcentral.com/posts/second-interview-with-chimeraos-founder/) -- the closest distro that's going to give you that SteamOS-like experience.

# Installation
First, to boot any external media, you'll need to **disable Secure Boot.** To do this, hold the Volume+ button while turning the device on. Tap "BIOS Setup" from the dropdown menu. Tap "More Settings". Tap the Security tab and scroll down to Secure Boot. Disable it from the dropdown menu. Exit saving changes from the Exit tab.

![Disabling secure boot in Legion Go](/images/legion_go/disabling_secure_boot.jpg)

Shut the console off. Turn it back on with the Volume+ button held down. Tap "Boot Menu" and select your flashed media to boot from it.

The installation went just fine (albeit you'll have to tilt your head slightly due to the way the text is oriented). You'll need to connect a keyboard, either to a USB-C dock or directly if your keyboard supports that type, to navigate through the options. Wi-Fi was picked up out-of-the-box, so I could connect to my local network and download the latest ChimeraOS image (which, at the time of writing this, is [44-1](https://github.com/ChimeraOS/chimeraos/wiki/Release-Notes#chimeraos-44-1-2023-10-15)).

![ChimeraOS installer on Legion Go](/images/legion_go/chimeraos/installation.jpg)

# Fix For Rotated Display and Missing Controls
After installation, the speakers worked just fine, including the volume controls. No need to override the DSDTs as users once had to do with the ROG Ally. Bluetooth, brightness controls, and the touchscreen also worked.

Two caveats, however. One, the display is rotated upside down.

![Upside down screen in game mode](/images/legion_go/chimeraos/upside_down_display.jpg)

Two, the controls on the joycons don't work, unless you put them into D-input mode by holding the Legion L button and the right shoulder button for one second. Or by detaching one joycon and holding it sideways (the Legion Go switches to Dual D-input mode when you do this).

Fortunately, both of these issues have been fixed very quickly, thanks to ChimeraOS dev Matthew Anderson and Nobara Project founder GloriousEggroll (GE contributed the changes to Nobara Project and these have been upstreamed to ChimeraOS unstable). **By opting into the "unstable" ChimeraOS branch, both of these issues are solved.**

To opt into the unstable branch, while your keyboard is still connected, press CTRL + ALT + F2 to access a terminal. Login with username "gamer" and password "gamer". Enter this:

`sudo frzr-deploy chimeraos/chimeraos:unstable`

Enter "gamer" again when prompted for the sudo password. ChimeraOS will download the unstable build. When finished, the console should reboot.

Alternatively, you can do the same thing within Steam's interface:

1. Tap the Steam icon on the screen to access the Steam menu.
2. Select "Settings". Under System, enable developer mode with the appropriate toggle.
3. Scroll down to the new "Developer" tab on the left. Scroll down to "Show Advanced Update Channels" and toggle this on.
4. Go back to the System tab. Under the "OS Update Channel" dropdown menu, select "unstable".
5. Tap "Check for Updates" to download and install the unstable build. Restart when finished.

![Enabling dev mode and selecting unstable branch](/images/legion_go/chimeraos/enable_dev_mode.jpeg)

Bam. Now the screen is properly rotated, and the joycons now work with the default X-input mode. [A udev rule was added to make this work](https://nobaraproject.org/2023/11/01/november-1-2023/) "until we have real patches." Vibration should work as well, and you can adjust the strength by holding the Legion L button and the Up or Down directions on the D-pad.

As a side note, most plugins with [Decky Loader](https://linuxgamingcentral.com/posts/steam-deck-plugins/) have worked based on my testing so far, as well as [CryoUtilities](https://linuxgamingcentral.com/posts/cryoutilities/) and [EmuDeck](https://www.emudeck.com/) (yes, of course I would test to see if Slippi would run directly through Steam BPM, and it did).

# Remaining Issues and Workarounds
A few hiccups -- many of which are minor -- remain for now:
- you can't map the Guide or QAM buttons to any of the extra buttons on the joycons
- while you can move the mouse cursor around with the touchpad, it won't register any mouse clicks
- no gyro support
- TDP controls can't be adjusted via software
- toggling Night Mode or adjusting the color temperature doesn't do anything
- the option to enable adaptive brightness is greyed out
- pressing the power button doesn't suspend the device -- while it turns the screen off, the battery is still consumed quite heavily
- no way to turn off the LEDs around the sticks, as far as I know
- the battery icon may say "full" all the time even though it actually isn't -- you can see the real percentage left with MangoHUD
- sometimes the screen may white out entirely -- or parts of it will flicker -- when you access Steam while a game is running

I've found a temporary workaround for most of these issues. **For the Guide button, you can remap it to any of the working buttons, but you will lose functionality for that button.** For instance, I've mapped the Guide button to D-pad Up -- but now I can't use D-pad Up for what it normally does, if that makes sense. You can remap the controls by going to Steam -> Settings -> Controller -> Test Device Inputs -> Setup Device Inputs.

![Setting controls on the Legion Go](/images/legion_go/chimeraos/controls.jpeg)

As for TDP controls, you actually *can* adjust them through the hardware itself by switching thermal modes. Observe the color of the power LED. **You can switch colors by holding Legion L + Y. Each time you press this combination, you change the performance mode:**
- quiet: blue LED; uses about 8 W
- balanced: white LED; uses about 15 W
- performance: red LED; uses about 20 W
- custom: purple LED; uses anywhere from 5-30 W; although at default it seems to be around 20 W

You can use this to adjust how much performance you want in your games versus how much battery life you want to conserve and how loud you want the fans to get. As far as I know, there isn't a way to adjust the watt usage in Custom mode.

{{< rawhtml >}}

<video width=100% controls autoplay loop>
    <source src="/videos/legion_go/chimeraos/testing_thermal_modes.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

For gyro, I know it's not the greatest solution but **if you're playing a first-person shooter you can switch the right joycon to FPS mode. This controller will turn into a mouse** (there's an IR sensor at the bottom of the joycon). From there you can put the joycon in the magnetic stand that's provided with the case and put it on a table. Then you can move the joycon around like a mouse. Pretty neat! I'm not sure if you can remap any of the buttons though.

{{< rawhtml >}}

<video width=100% controls autoplay loop>
    <source src="/videos/legion_go/chimeraos/fps_mode.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

(Yes, I know, I need some practice with this mode.)

**You can still put the Legion Go to sleep. Instead of pressing the power button directly, just access Steam's menu -> Power -> Sleep.** It works as expected, and turning the device back on will go right to where it was before it went to sleep, without much battery lost.

Those are all the notes I have for now. Overall it's been a pretty good experience so far. And I'm sure in due time a lot more of the remaining issues will be fixed. In the meantime, let me know in the comments if you'd like to see a full, hands-on review of the Legion Go itself.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
