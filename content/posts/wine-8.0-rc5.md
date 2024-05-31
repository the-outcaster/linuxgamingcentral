+++
title = "Wine 8.0-rc5 Fixes Slow OpenGL Performance with Dark Souls Remastered, Fixes Video Playback for Several Titles"
date = 2023-01-20T19:18:52Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/wine/8.0-rc5.jpg"
tags = ["news", "software update", "wine"]
keywords = ["wine", "wine is not an emulator", "dark souls remastered", "mafia iii", "war mongrels", "the medium", "sherlock holmes chapter one"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
The patch notes mention for this particular release candidate that it should be "the last...before the final 8.0." Not as big of an update as previous release candidates, but bug fixes we did get for a few titles, including *Dark Souls Remastered*, *Mafia III*, *War Mongrels*, *The Medium*, and *Sherlock Holmes Chapter One*.

A total of **nine** bugs were fixed:
- #26822  Double click the icon in the title bar should close the window
- #32643  getsockopt() does not indicate WSAEFAULT when setting optlen too small
- #45542  WeGame hangs after login.
- #50351  Slow text rendering in dofus linked to fnIMLangFontLink2_GetCharCodePages calling WideCharToMultiByte with CP_UNICODE
- #51227  urlmon:url breaks the wininet:http test on Windows 10 1709+ (7 failures)
- #51906  Multiple games fail to play videos (War Mongrels, The Medium, Sherlock Holmes Chapter One)
- #53408  Dark Souls: Remastered has slow performance with OpenGL renderer
- #53761  Broken rendering in Mafia III: Definitive Edition
- #54283  dinput:force_feedback - test_windows_gaming_input() sometimes crashes on Windows

See the patch notes on [WineHQ](https://www.winehq.org//announce/8.0-rc5). Provided that everything goes according to plan we should be seeing the stable 8.0 release within a week or two.

*Cover image credit: Frogwares*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
