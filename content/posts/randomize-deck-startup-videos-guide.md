+++
title = "Randomize Your Steam Deck Startup Videos - Here's How"
date = 2022-10-12T09:19:17-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/bootloader_customization/portal.jpg"
tags = ["guide", "steam deck"]
keywords = ["steam deck", "steam deck startup video", "randomization"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
So, you found a bunch of startup videos for your Deck that you like. Maybe you found them over on [Steam Deck Repo](https://linuxgamingcentral.com/posts/steam-deck-repo/). But perhaps you're a bit disappointed that you can only use one startup video at a time.

Well, the good news is you *can* randomize the startup video each time you turn the Deck on. This way, you always have something fresh to watch. And it's relatively simple. Here's how to do it. As usual with most of my Deck tutorials, I highly recommend docking your device and connecting a keyboard and mouse.

# 1. Get Your Videos
[Steam Deck Repo](https://steamdeckrepo.com) is the perfect place to get custom startup videos for your Deck. Download a bunch -- whatever you want. No need to truncate these files or convert them; just place them in `~/.steam/root/config/uioverrides/movies/` (you may need to create the latter two folders if they're not there already).

# 2. Create a Startup Service File
We need to create a `.service` file which will automatically execute a custom script that we're going to make each time the Deck is turned on or restarted. In a terminal, run:

`nano ~/.config/systemd/user/switch_startup_vids.service`

Paste the following contents in this new file:

```
[Unit]
Description=Switches startup videos

[Service]
ExecStart=/bin/bash /home/deck/./update_boot_vid.sh

[Install]
WantedBy=default.target
```

Save the file with `CTRL + O`. Then exit Nano with `CTRL + X`.

Now we need to run a command to enable this service to run at boot time:

`systemctl --user enable switch_startup_vids`

![Steam Deck custom startup video](/images/steam_deck/bootloader_customization/steam_deck.jpg)

# 3. Create a Script to Randomize Startup Video
Navigate back to your `home` directory in the terminal:

`cd ~`

Create a new bash script:

`nano update_boot_vid.sh`

Paste the following contents into the new file:

```
#!/bin/bash

VID_PATH=~/.steam/root/config/uioverrides/movies

if [ -f ~/.last_boot_vid ]; then
        mv "$VID_PATH"/deck_startup.webm "$VID_PATH"/$(cat ~/.last_boot_vid)
fi

RANDOM_VID=$(ls "$VID_PATH" | sort -R | head -1)
echo "$RANDOM_VID" > ~/.last_boot_vid

mv "$VID_PATH"/"$RANDOM_VID" "$VID_PATH"/deck_startup.webm
```

Save the script with `CTRL + O`, then exit the editor with `CTRL + X`. Make the script executable:

`chmod +x update_boot_vid.sh`

Then run it:

`./update_boot_vid.sh`

You can verify if it worked by going to your `/uioverrides/movies/` folder and playing the `deck_startup.webm` file. Play this same file each time you run the script to ensure the startup video has changed.

Restart your Deck, and confirm if the boot video changes on each startup.

Thanks to [u/Mounir9912](https://www.reddit.com/r/SteamDeck/comments/xys7qk/random_boot_video/) for the original tutorial. I had to modify the contents a little bit (for instance, it's *very* important that you add the `/` to `ExecStart=/bin/bash /home/deck/./update_boot_vid.sh` in the service file, otherwise the service won't run the script).

*EDIT (10/13/2022): if you happen to understand German you can also view [Steam Deck Checker's guide](https://youtu.be/1U6t2weV_0E) in video format. He also has an [English version](https://www.youtube.com/watch?v=d8URqBMUgZE&feature=share&utm_source=EJGixIgBCJiu2KjB4oSJEQ).*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
