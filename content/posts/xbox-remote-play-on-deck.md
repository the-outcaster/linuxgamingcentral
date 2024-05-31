+++
title = "You Can Stream Your Xbox to Your Steam Deck"
date = 2022-09-04T15:27:37-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/xbox_remote_play/cover.jpg"
tags = ["steam deck", "xbox", "guide"]
keywords = ["steam deck", "xbox"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
[Steam Deck Checker](https://www.youtube.com/c/SteamDeckChecker/videos) is a YouTube channel that covers all things Steam Deck. Though it's primarily a German-speaking channel, there are a few videos that are in English. One such video is [how to stream your Xbox to your Deck](https://youtu.be/qRlRjWdvA-8).

The video has step-by-step instructions on how to get it set up. The process requires getting the AppImage of [Xbox Xcloud client](https://github.com/unknownskl/xbox-xcloud-client/releases/), marking it as executable, then adding it as a non-Steam game. Sign in to your Xbox account and so long as your Xbox is on and connected to your local network, you should now be streaming your Xbox to your Deck.

Launch parameters that you should have for the Xbox Remote Play app include `--no-sandbox --fullscreen`, and if you have multiple Xboxes, you can choose the one you want to connect to by adding `--connect=` followed by the Xbox ID.

I don't own an Xbox but this tutorial will definitely come in handy for those of you that do. And it's interesting since I thought you could only stream a PS4/PS5, not an Xbox. Guess I was wrong!

*Cover image credit: Steam Deck Checker*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
