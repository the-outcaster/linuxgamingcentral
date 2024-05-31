+++
title = "Steam Deck UI Now Available For Desktop"
date = 2022-10-27T15:01:36-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/steam_deck_ui/cover.jpg"
tags = ["news", "software update", "steam", "steam deck", "steam client update", "beta"]
keywords = ["steam", "steam client", "steam deck", "steam deck ui", "beta"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
The Steam Deck UI, while it has technically [been available for quite some time on devices other than the Steam Deck](https://linuxgamingcentral.com/posts/steamdeck_ui/), is now *officially* available as a beta. You can use this on desktop, or any other PC handheld for that matter. To use the new UI, you'll need to opt-in to the Beta branch in your Steam settings (Steam -> Settings -> Account -> Change... -> Steam Beta Update).

![Steam opting into Beta branch](/images/steam/opting_into_beta.jpg)

Afterwards you'll need to exit the Steam client. Open up a terminal and run Steam with the `-gamepadui` argument:

`steam -gamepadui`

If everything went well you should have the updated Big Picture interface.

![Steam Deck UI on desktop](/images/steam_deck_ui/hot_wheels.jpg)

Bear in mind, as far as I can tell, nothing has been fixed on the NVIDIA side of things. The navigation across the different options is unbearably laggy. The games that I've tried running with are also slow. *Kena* for example runs around 35-40 FPS when it normally runs closer to 50-60. I've also noticed some odd behavior that's hard to explain. For instance, as you can see in the photo below, when accessing the Deck UI menu, only the menu becomes visible, and the rest of the screen becomes transparent. I've also noticed sporadic issues in-game where the Deck UI seems to activate by itself, and then I can't control anything in the game until I press the Guide button to get out of it.

![Steam Deck UI transparency bug](/images/steam_deck_ui/transparency_bug.jpg)

On the other hand, if you're on AMD, you shouldn't have too much of a problem. Intel might be a different story...

Keep an eye out for updates to this. Now that the Deck UI has officially rolled out to beta, hopefully it will catch NVIDIA's attention so they can get their act together to add the proper support on their end.

See more details on Steam's [blog post](https://store.steampowered.com/news/app/593110/view/3394051164709183116). And make sure to provide your feedback in the [Steam Big Picture forum](https://steamcommunity.com/groups/bigpicture/discussions/?snr=1_2108_9__2107).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
