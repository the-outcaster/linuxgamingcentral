+++
title = "Need to Clear Up Some Space on Your Steam Deck? Try DeckCleaner"
date = 2022-09-24T11:56:18-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/deckcleaner/freed_space.jpeg"
tags = ["guide", "steam deck", "deckcleaner", "utility"]
keywords = ["steam deck", "deckcleaner"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
When downloading games on the Steam Deck, more space on the hard drive gets occupied than just the game itself. Shaders will either be downloaded along with the game, or they will get added as you play the game. While these shaders can be useful for reducing in-game stutter, these shaders will pile up over time. Games that you no longer play will still have their shaders intact, thus taking up space that could be used for something more important.

As you can see here, "Other" on my Deck consumes about 154 GB of space. "Other" is a very generic category; it could refer to the files that you've stored in Desktop Mode, ROMs that you've copied over, etc. Shader cache is also a part of this category.

![Steam Deck storage space before clearing shader cache](/images/deckcleaner/space_before_cache_cleared.jpeg)

Thanks to community-made efforts, clearing up the shader cache is as simple as downloading and running a bash script. For this tutorial, we'll be using [DeckCleaner](https://github.com/MiaPepsi/DeckCleaner). In my case I freed about 10 GB of space on my Deck using this script.

I strongly recommend connecting a keyboard and mouse to your Deck, at least during first time setup; this will make our life quicker and easier. Later on you can add the script as a non-Steam game and use it via the touchscreen.

Go to Desktop Mode (press the Steam button > Power > Switch to Desktop). Open up a terminal (Plasma uses Konsole by default) with `CTRL + ALT + T`, or select Konsole from the Start Menu. Download the latest version of the DeckCleaner script (1.2 at the time of writing this) with:

`wget https://raw.githubusercontent.com/MiaPepsi/DeckCleaner/main/deckcleaner1.2.sh`

By default this script will be saved to `/home/deck`, should you need to refer back to it later. Mark the script as executable:

`chmod +x deckcleaner.sh`

And then run it:

`./deckcleaner.sh`

Note that if you press Tab while typing in the terminal, it will autocomplete the name for you. This should make your life a little more convenient as you're typing.

A dialog box should open if everything went well. You'll be shown how much space the shader cache is taking and what you want to do with it. If you want, you can move the shaders to your MicroSD card; this is particularly useful for those who have the 64 GB model of the Deck to maximize as much space on the eMMC while still having the shaders available. Otherwise, you can either delete the cache or keep it.

![DeckCleaner dialog box](/images/deckcleaner/confirm_deletion.png)

After clearing the cache and going to the Storage tab in Game Mode, I now see that I have 144 GB occupied in "Other" rather than the 154 GB that it was before.

![Deck storage after clearing cache](/images/deckcleaner/freed_space.jpeg)

Note that your most recently-played games may download the shader cache again. But you should still have some storage freed up from the games that you either uninstalled or haven't played in a while.

To add the script as a non-Steam game, simply right-click the file in your file manager while in Desktop Mode, and in the context menu, select "Add to Steam." This way you can run the script at any time you want without having to resort to Desktop Mode. You can select one of the options in the dialog box with the touchscreen.

If you prefer to delete the cache from only a few specific titles, you can use [Shader Cache Killer](https://github.com/scawp/Steam-Deck.Shader-Cache-Killer), as [Steam Deck Life](https://steamdecklife.com/2022/09/24/heres-a-tool-to-selectively-delete-shader-cache-compatdata-on-the-steam-deck/) recently brought out. This script will also allow you to delete the compatdata for individual games; this can be useful for games that may have once run but are no longer doing so, for whatever reason.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
