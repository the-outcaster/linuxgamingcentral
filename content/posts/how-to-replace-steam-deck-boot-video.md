+++
title = "Want to Customize The Intro Video on Deck? Here's How"
date = 2022-09-26T08:46:22-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck/bootloader_customization/cover.webp"
tags = ["guide", "steam deck", "bootloader"]
keywords = ["steam deck", "bootloader", "intro video"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
**UPDATE (10/7/2022): this tutorial is no longer relevant, Valve has made it easier to replace the bootloader video with this week's [update](https://linuxgamingcentral.com/posts/steamos-3.3.2-and-steam-deck-client-update-10-5-2022/) to the Steam Deck client.**

The beauty of the Steam Deck is how *insanely* customizable it is. We can go so far as replacing the Steam intro video when turning the device on, or when switching to Game Mode. So if you wanted something like this:

{{< rawhtml >}} 

<video width=100% controls>
    <source src="/videos/melee_deck_intro.webm" type="video/webm">
    Your browser does not support the video tag.
</video>

{{< /rawhtml >}}

It's totally do-able! Best part is, it's really not that difficult, and even if something goes wrong, the custom video will be replaced with the stock one. Here's how to do it!

*NOTE: to my knowledge it is NOT possible to replace the Steam logo at boot time, but feel free to let me know in the comments if I'm wrong.*

I recommend using your desktop for getting the clip of your choice, then use something like [Syncthing](https://linuxgamingcentral.com/posts/how-to-sync-non-steam-cloud-games/) to transfer the video file to your Deck. This is all possible on the Steam Deck itself, but it can be a bit of a pain to work with.

You'll first want to start off by getting the clip. It could be a customized [*Futurama*](https://www.reddit.com/r/SteamDeck/comments/xi3vno/my_custom_futurama_boot_video/) boot intro, it could be [*Breaking Bad*](https://www.reddit.com/r/SteamDeck/comments/xm8hpz/custom_boot_animations_breaking_bad_and_frasier/), it could be [Gabe Boy](https://www.reddit.com/r/SteamDeck/comments/wjxhqh/gabe_boy_steam_deck_intro_video_oc/), a Nintendo 64/GameCube intro, you name it. If you find these clips on r/SteamDeck, chances are these videos will already be formatted for you, and you can simply copy the video file over to the appropriate place on your Deck's internal storage.

If you're using your own clip, I suggest downloading the video and trimming it down to **no more than 10 seconds** with your preferred video editor. I personally like to use [Shotcut](https://shotcut.org/). This is a video you're going to be seeing time and again whenever you turn the Deck on, or whenever you switch from Desktop to Game Mode, so ideally you want to keep it short. 

In your video editor's export settings, it's not a requirement, but you may want to set the aspect ratio to 16:10 with the resolution set to 1280 x 800 if you want your clip in fullscreen. Setting the framerate to 30 FPS also helps for keeping the file size down. **Export the clip as a WebM file. Make sure the file is 1.8 MB or less**; if the file size is larger, keep trimming the clip down until it's smaller (I also found that if you use CPU encoding rather than the GPU when exporting the video, this decreases the file size). Here in this screenshot I give you a general idea of what your export settings should be (obviously these settings will be in different places depending on what video editor you use).

![Video export settings](/images/steam_deck/bootloader_customization/export_settings.jpg)

Rename the exported video file to `deck_startup.webm`. The next step is important: we need to **truncate the video file to be the same size as the original**. If we don't do this, the Deck will know that the file has been modified, and it will replace the custom video with the stock startup video. Truncating is simple; in the terminal, in the same folder where your clip is located, enter this:

`truncate --size=1840847 deck_startup.webm`

"1840847" in this instance is the amount of bytes that we want to set the file size to. Running this command will make the clip the same file size as the original startup video on the Deck, 1.8 MB. Transfer this new video file to your Deck.

On your Steam Deck in Desktop Mode, open your file manager (Plasma uses Dolphin by default). By default hidden files and folders are not visible; click the hamburger icon in the file manager and check the box for "Show Hidden Files". Navigate to `/home/deck/.local/share/Steam/steamui/movies`. Copy the new clip over, replacing the existing file.

![Show hidden files in Dolphin](/images/steam_deck/bootloader_customization/hidden_files.png)

That's pretty much it. However, you might notice that the clip isn't in fullscreen when switching to Game Mode, or when turning the Deck on. There's an easy fix for this. Go back one folder and go to `css`. Open `library.css`. Depending on the text editor you use (such as KWrite), you may need to temporaily reload the file since it's so large. Go all the way down the file. Towards the last line there should be `video` followed by a set of squiggly brackets with parameters inside, such as `flex-grow`, `width`, etc. It should have something like this:

`video{flex-grow:0;width:300px;height:300px;z-index:10}`

You're going to want to replace that entire line with this:

`video{flex-grow:1;width:100%;height:100%;z-index:10}`

Make sure there are no spaces between the semicolons. Save the file. We need to truncate this file as well:

`truncate -s 38492 library.css`

If the intro video still isn't in fullscreen, you may need to truncate the CSS file to a different value:

`truncate -s 38488 library.css`

That's it! Not only should you have a custom bootloader, but it should be fullscreen as well.

![Futurama bootloader on Deck](/images/steam_deck/bootloader_customization/futurama.jpg)
*Image credit: u/DerpinHerps*

So here's the quick rundown:
1. Get the clip of your choice. Make sure it's less than or equal to 1.8 MB and formatted as a WebM file
2. Rename the clip to `deck_startup.webm`
3. Truncate the file: `truncate --size=1840847 deck_startup.webm`
4. Copy the clip over to `/home/deck/.local/share/Steam/steamui/movies`. Replace the existing `deck_startup.webm` file
5. (Optional) Set the video to fullscreen by replacing `video{flex-grow:0;width:300px;height:300px;z-index:10}` found in `/home/deck/.local/share/Steam/steamui/css/library.css` with `video{flex-grow:1;width:100%;height:100%;z-index:10}`. Truncate the CSS file with `truncate -s 38492 library.css`

Special thanks to [u/yaenzer](https://www.reddit.com/user/yaenzer/), [u/DerpinHerps](https://www.reddit.com/user/DerpinHerps/), [u/wilduk1](https://www.reddit.com/user/wilduk1/),  [u/Zacketry](https://www.reddit.com/user/Zacketry/), and [u/Crazy89_](https://www.reddit.com/user/Crazy89_/) for figuring this out and having their custom boot intros!

Any questions, feel free to ask.

*Cover image credit: u/Zacketry*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
