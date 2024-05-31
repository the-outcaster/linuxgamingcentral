+++
title = "Overclock Your GameCube Controller Adapter on Steam Deck"
date = 2023-11-29T18:27:16Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck_oled/guides/overclocking_gc_adapter/cover.jpg"
tags = ["guide", "smash bros", "slippi", "steam deck", "steam deck oled", "overclocking"]
keywords = ["gc adapter overclocking on steam deck", "slippi", "super smash bros melee", "ssbm", "gamecube controller adapter overclock", "steam deck", "steam deck gamecube adapter overclock", "gamecube controller adapter"]
description = "Finally, an easy way of doing it, and stays consistent across reboots too!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
I finally figured it out. There is a now relatively straightforward way of overclocking your GameCube controller adapter on Steam Deck/Steam Deck OLED with SteamOS 3.5.7. Here's how to do it. I highly recommend connecting a keyboard and mouse. (Note that I have not tested this on the SteamOS "Preview" branch, but it *should* still work.) Instructions for OC'ing your GCC adapter can also be found on the [gcadapter-oc-kmod GitHub](https://github.com/hannesmann/gcadapter-oc-kmod/blob/master/STEAMOS.md).

**EDIT (11-30-2023): made installation even easier with a [script](https://github.com/linuxgamingcentral/gcadapter-oc-kmod-deck). Just download the `.desktop` file in Desktop Mode (right-click, save as), then run it. Let me know how it goes!**

Go to Desktop Mode. If you don't have a root password set up already, open up a terminal and run `passwd`. Set up your password as desired.

Next, disable SteamOS' read-only filesystem:

```
sudo steamos-readonly disable
```

Enter your sudo password when prompted.

Populate the pacman keys:

```
sudo pacman-key --init
sudo pacman-key --populate archlinux holo
```

Install the necessary developer tools and the Linux headers, so we can compile gcadapter-oc-kmod:

```
sudo pacman -S --needed base-devel "$(cat /usr/lib/modules/$(uname -r)/pkgbase)-headers"
```

Press Enter when prompted to install the packages.

Great. Now clone the gcadapter-oc-kmod repo and change into the newly created directory:

```
git clone https://github.com/hannesmann/gcadapter-oc-kmod.git
cd gcadapter-oc-kmod
```

Compile the program with make:

```
make
```

Finally, install the module:

```
sudo insmod gcadapter_oc.ko
```

Done! Your GC controller adapter should now be overclocked to 1,000 Hz in both Desktop Mode and Game Mode.

# Keep the Adapter Overclocked Across Reboots
The polling rate will go back to 125 Hz if you restart the Deck. Fortunately, we can keep the overclock persistent across reboots. While you're still in Desktop Mode with the terminal open, and you're in the gcadapter-oc-kmod folder, run the following:

```
sudo mkdir -p "/usr/lib/modules/$(uname -r)/extra"
sudo cp gcadapter_oc.ko "/usr/lib/modules/$(uname -r)/extra"
sudo depmod
echo "gcadapter_oc" | sudo tee /etc/modules-load.d/gcadapter_oc.conf
```

Optionally restore the read-only filesystem with:

```
sudo steamos-readonly enable
```

Note that, if Valve decides to update the kernel at some point (6.1 at the time of writing this), you'll need to re-run most, if not all of these commands.

See my [Slippi guide](https://linuxgamingcentral.com/posts/steam-deck-and-melee/) if you want to get Slippi set up on your Steam Deck, and my older [guide](https://linuxgamingcentral.com/posts/overclocking-gc-adapter-guide/) for getting the adapter OC'd on other Linux distros. Thanks to **hannesmann** for helping me to future-proof this guide and figuring out how to keep the adapter OC'd across reboots.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
