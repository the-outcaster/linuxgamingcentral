+++
title = "Overclock Your Controller for Less Input Lag"
date = 2022-12-06T11:46:04-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/controller_overclocking/cover.jpg"
tags = ["guide", "smash bros", "slippi"]
keywords = ["super smash bros. melee", "ssbm", "melee", "steam deck", "linux", "gamecube", "gamecube controller adapter", "slippi", "mayflash"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
By default, your controller adapter polls at a rate of 125 Hz, or every eight milliseconds. However, by overclocking it, we can increase that rate to nearly 10 times at *1,000 Hz*. The result of this overclock, per the [document](https://docs.google.com/document/d/1cQ3pbKZm_yUtcLK9ZIXyPzVbTJkvnfxKIyvuFMwzWe0/edit) by [SSBM_Arte](https://twitter.com/SSBM_Arte), results in "a much closer experience to console play. It considerably improves the latency stability, which directly impacts execution, and also reduces input lag."

You might have seen this in action with a [mouse](https://www.youtube.com/watch?v=AZ9qutNL_-w). Increasing the poll rate allows for smoother motion and less input latency. We'll apply these same steps with a GameCube controller.

As people were quick to point out to me on [Twitter](https://twitter.com/linuxgamingctr/status/1598798857776791554), third-party controller adapters will *not* work with overclocking. So I went and got myself a [Mayflash adapter](https://www.amazon.com/dp/B00RSXRLUE). Works like a charm. You can either use this, or the [official Wii U GC adapter](https://www.ebay.com/itm/374376707069). The latter has less latency volatility, but they're expensive and hard to find. Make sure *both* USB ports are plugged into your desktop.

# Is Overclocking Dangerous?
No. Per the [document](https://docs.google.com/document/d/1cQ3pbKZm_yUtcLK9ZIXyPzVbTJkvnfxKIyvuFMwzWe0/edit#heading=h.e3nzjbxw89pn):
>  “Overclocking” a USB device is specification compliant. USB devices say to the PC “I would like to be polled at least every X ms when I’m in use.” Polling less often than that is not specification compliant...nothing changes inside the device, we’re just polling it faster than it asked for. Operating systems by default poll devices as rarely as they’re allowed to so as to preserve USB bandwidth. Then depending on the philosophy of the OS, the difficulty of explaining to the OS you don’t want to poll as seldom as possible differs.

# Linux Desktop
It's actually quite simple. Hopefully you've got some familiarity with the terminal (and pro-tip: pressing TAB while putting in a command or folder path name will auto-complete it, making your life easier). We'll make use of a kernel module called [gcadapter_oc_kmod](https://github.com/HannesMann/gcadapter-oc-kmod). Make sure you have `linux-headers` installed on your system (sounds like a no-brainer, but believe me, I didn't have the headers when I first ran this script and it wouldn't run). Then clone the repository:

`git clone https://github.com/hannesmann/gcadapter-oc-kmod.git`

If you're on Arch, your life has been made simple. Change into the `gcadapter-oc-kmod/packaging/arch/` directory, then run `makepkg -si`. You should be all set. If Dolphin/Slippi was open while you installed the module, restart the emulator and you should see the changes. Polling rate should stay consistent across reboots and kernel updates thanks to the use of DKMS.

![Overclocked GC adapter](/images/controller_overclocking/overclocked.png)

On distros outside of Arch, change into the new directory:

`cd gcadapter-oc-kmod`

Run "make" to build gcadapter_oc.ko:

`make`

Load the module into the running kernel:

`sudo insmod gcadapter_oc.ko`

![Terminal commands for installing kernel module](/images/controller_overclocking/terminal_commands.png)

Restart Slippi and you should be good.

In the event you want to revert the poll rate back to 125 Hz, simply run `sudo rmmod gcadapter_oc.ko`.

# Steam Deck
See my [updated guide](https://linuxgamingcentral.com/posts/overclock-gc-adapter-on-steam-deck/) for getting the GCC adapter overclocked on Steam Deck.

# Change Polling Rate
You shouldn't need to do this, but if for some reason setting the adapter to 1,000 Hz causes stutter or dropped inputs, you can reduce the polling rate to a lower value, such as 500 Hz. There's one of two ways to do this. The first way would be (this needs to be run inside the directory where you built the kernel module; make sure the kernel module has been removed before doing this):

`sudo insmod gcadapter_oc.ko rate=X`

Change "X" to the polling rate in milliseconds. For example, if you wanted to set the rate to 250 Hz, you would replace "X" with "4" (without quotes). To set it to 500 Hz, you would use "2". 1,000 Hz would be "1". You get the idea.

![Polling rate set to 2ms (500Hz)](/images/controller_overclocking/500hz.png)

Alternatively, you can do it this way:

```
sudo su
cd /sys/module/gcadapter_oc/parameters/
echo X > rate
```

When I run `echo 4 > rate` and restart Slippi, now my adapter's polling rate is 250 Hz:

![Polling rate set to 4ms (250Hz)](/images/controller_overclocking/250hz.png)

# Ports Matter
For some reason, if you connect your GC controller to port 2 in the Mayflash adapter in single player, you'll get ["the best experience."](https://docs.google.com/document/d/1cQ3pbKZm_yUtcLK9ZIXyPzVbTJkvnfxKIyvuFMwzWe0/edit#heading=h.18skeoosa2vw) It's apparently better than using port 1, although the document doesn't mention why. I'd love if someone could fill me in on that. Use ports 1 and 2 for doubles.

If you're using the official adapter, plug a spare controller into port 1, and the one you're planning on using into port 2. The document notes: "I am dead serious" and they get into why.

If you need more info about overclocking, see the [document](https://docs.google.com/document/d/1cQ3pbKZm_yUtcLK9ZIXyPzVbTJkvnfxKIyvuFMwzWe0/edit).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
