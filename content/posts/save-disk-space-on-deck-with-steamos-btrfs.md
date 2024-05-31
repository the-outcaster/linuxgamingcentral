+++
title = "Save Disk Space on Steam Deck with SteamOS-Btrfs"
date = 2022-10-28T13:30:39-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/steamos-btrfs/cover.jpeg"
tags = ["guide", "steam deck", "btrfs", "ext4", "steamos", "steamos-btrfs"]
keywords = ["steam deck", "btrfs", "ext4", "steamos", "steamos-btrfs"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
There are quite a few ways in which you can free up storage on your Deck. Besides [cleaning up shaders](https://linuxgamingcentral.com/posts/deckcleaner/), you can also convert the default `ext4` file system the Deck uses into [`btrfs`](https://wiki.archlinux.org/title/Btrfs). A few benefits that come from converting to `btrfs` include:
- disk space saved (a little over 50 GB in my case) with the compression method that it uses
- cross-compatibility with Windows, should you use that OS (ex. formatting a MicroSD card as `btrfs` allows you to play the same games between operating systems without having to re-install them or re-formatting the SD card)

Supposedly there's also reduced loading times, but in the scarce research that I found, the [Reddit post](https://www.reddit.com/r/SteamDeck/comments/t8ztuv/btrfs_vs_ext4_tested/) was deleted by the original poster. I have also personally confirmed that, at least for getting in-game with *Horizon Zero Dawn*, it took 29 seconds for both `ext4` and `btrfs`. However, I haven't tested shader compilation times, so that may or may not see a performance improvement.

# User Beware
Some caveats that I'd like to make you aware of before trying this out. First, **neither myself nor the creator of [SteamOS-Btrfs](https://gitlab.com/popsulfr/steamos-btrfs/) are responsible for any damage caused to your system.** I was able to successfully convert my SSD to `btrfs` and keep all my games intact, but in Desktop Mode, some of my Flatpaks stopped working. Brave and Firefox, for example, wouldn't run at all, leading to a [ldconfig error](https://github.com/flatpak/flatpak/issues/5081). The only browser that worked for me was Chrome. In my testing so far I haven't found a fix. So, keep that in mind. 

`Btrfs` has its [known issues](https://wiki.archlinux.org/title/Btrfs#Known_issues) -- for example, encryption is *not* supported. You also can't go back to `ext4` after the conversion process has taken place. Finally, according to the README for SteamOS-Btrfs, this *should* survive updates to SteamOS, but I personally have not been able to verify that yet.

If you're okay with all of this, then let's go ahead and get started.

# 1. Have the Space

![Steam Deck used space](/images/steam_deck/steamos-btrfs/used_space.jpg)

Make sure your SSD has enough space for the conversion to take place. You'll need to have at least 10-20% of free space available. An easy way of checking this is by going to Desktop Mode and running this in a terminal:

`df -h /home`

Observe the `Use%` column. If it's more than 80-90%, stop what you're doing and clear up some space, be it uninstalling some games or deleting ROMs.

# 2. Set up Sudo (If You Haven't Already)
Set up a password for sudo privileges if you haven't done so already:

`passwd`

You'll be prompted to either create a password, or change it if this step has already been done before. Type your password in, then enter it again to confirm.

# 3. Get SteamOS-Btrfs
Enter these commands into a terminal, one line at a time:

```
mkdir steamos-btrfs
curl -sSL https://gitlab.com/popsulfr/steamos-btrfs/-/archive/main/steamos-btrfs-main.tar.gz | tar -xzf - -C steamos-btrfs --strip-components=1
```

# 4. (Optional) Set Up Configuration Options
Prior to installation, you can [configure](https://gitlab.com/popsulfr/steamos-btrfs#configuration-options) how you want SteamOS-Btrfs to work. This isn't something that I have personally messed around with; the default settings should be good enough in most cases.

# 5. Run the Script

![Converting Steam Deck SSD to BTRFS](/images/steam_deck/steamos-btrfs/running_the_script.jpg)

```
cd steamos-btrfs
./install.sh
```

You'll get a few pop-ups along the way. The Deck will reboot, and the conversion process will start.

This took quite a while on my end. I ended up having to leave the system on overnight for it to finish. If it appears as if the progress bar is stuck, it's not frozen; it's still working. So don't turn the system off. After a few minutes of inactivity, the screen will turn off, but you can turn it back on by tapping the screen. Regardless, the process will still be running.

# 6. See the Difference
Here was my storage space prior to conversion:

![Steam Deck storage with EXT4](/images/steam_deck/steamos-btrfs/before.jpeg)

And here it is after converting the file system to `btrfs`:

![Steam Deck storage with BTRFS](/images/steam_deck/steamos-btrfs/after.jpeg)

More than 50 GB was shaved. Though this is in the "Other" category, it's more than likely [a smaller Proton prefix footprint](https://www.reddit.com/r/SteamDeck/comments/t79fqj/comment/hzh7fyh/).

Besides the Flatpak issues, everything is running fine for me. Games are running the way they should, although I haven't tested enough to confirm if the compression method `btrfs` uses actually reduces shader compilation times. I'll tinker around with this some more and will update this post if I come across anything significant. Thanks to Philipp Richter for the script!

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
