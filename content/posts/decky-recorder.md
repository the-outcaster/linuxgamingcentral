+++
title = "Record Your Deck's Screen with Decky-Recorder"
date = 2023-02-14T03:58:47Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/guides/decky-recorder/qam.jpeg"
tags = ["guide", "steam deck", "decky loader", "decky recorder"]
keywords = ["steam deck", "decky-recorder", "steam deck recorder"]
description = "Here's how to get it installed and running."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
I've been getting a lot of comments on my last couple of [YouTube videos](https://www.youtube.com/@linuxgamingctr) as to how I got Decky-Recorder, as well as how to install it.

If you hadn't already noticed, the plugin isn't available in the Decky Loader store. It's currently in the process of [being merged with Decky Loader as a pull request](https://github.com/SteamDeckHomebrew/decky-plugin-database/pull/190). But we can still make use of the plugin. Here's how.

If you haven't installed Decky Loader on your Deck already, go and do so. Go to Desktop Mode, head to the [GitHub page](https://github.com/SteamDeckHomebrew/decky-loader), and click the Download button to download the .desktop file and run through the installation.

![Decky Loader GitHub page](/images/steam_deck/guides/powertools/decky_loader_github_page.webp)

Now head to the [Decky-Recorder GitHub](https://github.com/marissa999/decky-recorder). Go to the [Releases](https://github.com/marissa999/decky-recorder/releases) page. You'll notice two versions: 0.02 and 0.03. **I recommend going with 0.02 as it is more stable than 0.03**. Only use 0.03 if you want to record your voice.

Download the .zip file and extract it anywhere. Open your file manager (Plasma uses Dolphin by default) and go to `~/homebrew/`. You may notice the `plugins/` folder has a lock icon next to it. Meaning we can't just copy the extracted zip file over to this folder. So we'll need to modify the permissions of the folder.

Right-click `plugins/`, go to Properties, and go to the Permissions tab. Open the dropdown menu for all three items (Owner, Group, and Others) and select "Can View & Modify Content". Now check the box for "Apply changes to all subfolders and their contents". Click "OK" and the permissions should be applied. 

![Decky Loader plugins permissions](/images/steam_deck/guides/decky-recorder/permissions.png)

Now you can just copy the `decky-recorder/` folder and put it inside of the `plugins/` folder without getting a copy failure.

![Decky Loader plugins folder](/images/steam_deck/guides/decky-recorder/plugins_folder.webp)

That's it! Decky-Recorder is now installed. Go to Game Mode and it should be available as a plugin from the Quick Access Menu. Simply press "Start recording" and "Stop recording" to make use of it. Recordings will be captured at 60 FPS and will be saved in `~/Videos/`.

![Decky Loader in QAM](/images/steam_deck/guides/decky-recorder/qam.jpeg)

A couple of caveats to be aware of:
1. There's a 10-15% chance the recording won't actually save. If you try to play the video in Desktop Mode and nothing happens, you'll know the recording didn't work. You'll have to record again and just hope it works that time.
2. Small performance hit while recording. So if you have custom TDP/GPU clock settings for a particular game, you may want to bump it up a couple of notches to keep the performance the same.

{{< rawhtml >}} 

<video width=100% controls autoplay loop>
    <source src="/videos/mpr_on_deck/yuzu_clip.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

[Steam Deck Checker](https://linuxgamingcentral.com/posts/interview-with-steam-deck-checker/) also has a [video tutorial](https://www.youtube.com/watch?v=px3hSJMn928) (it's in German though). I'll make a video guide as well soon.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
