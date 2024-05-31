+++
title = "Xbox Game Pass Quality Sucks On Linux...But Here's a Quick Hack to Improve It"
date = 2022-07-05T11:07:21-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/xbox_game_pass/cover.jpg"
tags = ["news", "xbox game pass", "streaming"]
keywords = ["xbox game pass", ""]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Exactly a year ago I had conducted an overview of how Xbox Game Pass fares on Linux, over on [Boiling Steam](https://boilingsteam.com/so-i-tried-xbox-game-pass-on-linux/). One of the critical remarks I had about it was the streaming quality being terrible. Even if you had Gigabit Ethernet, you were forced to use Microsoft Edge to get that so-called "Clarity Boost," and while it helped a little, the overall image quality was a disappointment.

Well, perhaps to no one's surprise, it appears Microsoft deliberately throttles the video quality on Linux. A user on [r/xcloud](https://www.reddit.com/r/xcloud/comments/vrfmuz/quality_on_linux/) recently tried to observe the video quality on Manjaro. Here's a screenshot of what the quality normally looks like:

![xbox game pass on linux](/images/xbox_game_pass/before.webp)
*Image credit: u/Spiritual-Ad2806*

Now see the better clarity of the image after using an agent switcher, tricking the browser to thinking it's Windows 10 (you may need to open both images in a new tab to get a better inspection):

![xbox game pass with agent switcher](/images/xbox_game_pass/after.webp)
*Image credit: u/Spiritual-Ad2806*

It's as simple as that. Text isn't as blurry, and overall image quality is improved. It really doesn't surprise me to see the difference. I had a hunch all along Microsoft was doing this on purpose. But I guess the good news is it's possible to achieve the same quality on Windows, by simply using an agent switcher extension like [this](https://add0n.com/useragent-switcher.html) and switching the user agent to Windows 10.

*Cover image credit: stuff.co.za*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
