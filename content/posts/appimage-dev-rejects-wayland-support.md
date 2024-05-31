+++
title = "AppImage Developer Rejects Wayland Support"
date = 2023-01-19T14:07:59Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/linuxdeployqt/cover.webp"
tags = ["news", "appimage"]
keywords = ["appimage", "linuxdeployqt", "wayland"]
description = "Well, I guess we'll never get Wayland support for AppImages."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Someone had made a [pull request](https://github.com/probonopd/linuxdeployqt/pull/540) for LinuxDeployQt, the system that "takes an application as input and makes it self-contained by copying in the resources that the application uses...into a bundle. The resulting bundle can be distributed as an AppDir or as an AppImage to users." The PR adds the necessary libraries and plugins "to support the Wayland platform."

This PR isn't new. It's been around since July. Only did one of the developers respond six months later after someone had left a "friendly ping." They responded with:

> Thanks, but I am not interested in Wayland. None of my systems run Wayland, because it never works quite right in my experience. Especially when you are not using GNOME or KDE.

It's a bit of a strange response to be honest -- especially the "it never works quite right in my experience" part. I wonder if there's some sort of political reasoning behind their decision. The response has currently been met with 17 thumbs down.

They added a link in their response to a [document](https://gist.github.com/probonopd/9feb7c20257af5dd915e3a9f2d1f2277) that they wrote regarding all the reasons why Wayland should be boycotted. I will admit OBS has kind of been a pain with Wayland, particularly when [getting hotkeys to work](https://linuxgamingcentral.com/posts/nobara-project-impressions/#impressions). But their reasons seem heavily biased, especially when they say "Wayland breaks everything and then expects others to fix the wreckage it caused on their own expense." 

They also mention that Wayland causes screen tearing on Intel. It actually *doesn't*; at least not anymore, according to a friend of mine.

It's a bit of sad news as there are some applications that I use that are *only* available as an AppImage, that I would otherwise have to compile from source to use (provided that the application is open-source). Guess we'll just have to keep using XWayland as a workaround. Or maybe just make a fork and provide Wayland support that way.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
