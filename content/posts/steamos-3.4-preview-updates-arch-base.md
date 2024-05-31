+++
title = "SteamOS Has Finally Been Rebased to the Latest Version of Arch Linux! (Plus Plenty of Other Goodies)"
date = 2022-11-12T00:06:21-05:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/steamos_updates/3.4_preview/mangohud.jpeg"
tags = ["news", "steam deck", "steamos", "steamos update", "preview", "software update"]
keywords = ["steam deck", "steamos", "kde", "mesa", "glibc", "steamos 3.4"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Holy crap. And here I thought Valve was never going to update the Arch base.

Turns out I was wrong.

You might recall back in the summer I wrote about the [outdated packages on SteamOS](https://linuxgamingcentral.com/posts/the-growing-security-risk-with-steamos/) and the security risk that brought. Well, I guess you can finally use Desktop Mode with more peace of mind, now that most everything has been updated. Per Steam's post, this update "pulls in the latest performance, security and stability fixes for the underlying packages that are the foundation for SteamOS."

Packages that have been updated include:
- Mesa -- [22.2.0](https://docs.mesa3d.org/relnotes/22.2.0.html)

![Mesa 22.2.0 in SteamOS](/images/steam_deck/steamos_updates/3.4_preview/mesa.jpeg)

- KDE -- [5.26](https://kde.org/announcements/plasma/5/5.26.0/). This includes new touchscreen gestures, new themes and wallpapers, and updates to widgets and KRunner

![KDE 5.26 in SteamOS](/images/steam_deck/steamos_updates/3.4_preview/kde.png)

- glibc -- [2.36](https://sourceware.org/pipermail/libc-alpha/2022-August/141193.html)

![glibc 2.36 in SteamOS](/images/steam_deck/steamos_updates/3.4_preview/glibc.png)

- plenty of other packages that I'm probably forgetting to mention

Unfortunately it looks like the kernel is still stuck at 5.13.

But we got *way* more than just updated software packages with SteamOS 3.4. There's now an option for screen tearing:

![Screen tearing option in SteamOS](/images/steam_deck/steamos_updates/3.4_preview/screen_tearing_toggle.jpeg)

And as you can see in the cover photo, level 2 MangoHUD is now spread across horizontally rather than stacked vertically. It perfectly fits inside the black border for 16:9 aspect ratios, while taking less clutter on the screen!

TRIM has now been "re-enabled." Apparently this was used before, then disabled. Now it's back. It's supported for both internal drives as well as external storage mediums, such as MicroSD cards. This should improve write performance. TRIM gets run "periodically," but you can manually run it in Settings -> System -> Advanced:

![Run TRIM manually in SteamOS](/images/steam_deck/steamos_updates/3.4_preview/run_trim_manually.jpeg)

External storage devices can now be unmounted via the Storage section:

![Ejecting MicroSD card in SteamOS](/images/steam_deck/steamos_updates/3.4_preview/eject.jpeg)

External drives formatted as `ext4` are now automatically mounted and available for use in Steam.

Steam Input got some changes, including the disabling of DS4/PS5 trackpad -> mouse emulation when Steam is running, and the re-enabling of the built-in gamepad driver when Steam is not running in Desktop Mode.

"echo-cancel-sink" is no longer shown in the audio settings:

![Audio device name change in SteamOS](/images/steam_deck/steamos_updates/3.4_preview/audio.jpeg)

When docked, the audio should no longer go to "sleep" after being idle.

Some general changes as well, including a fix for 100ms "hitches" when adaptive backlight is on, and sleep/wake fixes for a "number of titles." Finally, a new firmware is available for the official docking station -- this fixes HDMI 2.0 display issues when waking the deck up.

Note that in order to use this update, you'll need to be opted into the **Preview** branch.

See more info on [Steam](https://store.steampowered.com/news/app/1675200/view/3383920059429575957). Thanks, Valve, for *finally* updating SteamOS!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
