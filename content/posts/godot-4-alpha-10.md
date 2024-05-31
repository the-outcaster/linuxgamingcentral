+++
title = "Godot 4 Alpha 10 Adds TAA and Conversion Tool for Godot 3.x Projects"
date = 2022-06-15T14:02:20-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/godot/4_alpha_10.jpg"
tags = ["news", "software update", "godot"]
keywords = ["godot", ""]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Godot 4 is a pretty major release for the open-source game engine. As such, the developers behind the project have entered into the double-digits territory: alpha 10.

New features with this alpha include initial support for temporal anti-aliasing (TAA), a CLI tool to convert your older Godot 3.x projects to the version 4 API, and a TileMap terrain center bit to support "connect" and "path" draw modes.

Here you can observe the difference in graphical quality with TAA disabled, per the [pull request](https://github.com/godotengine/godot/pull/61319):

![godot 4 taa off](/images/godot/taa_disabled.jpg)
*Image credit: JFonS from GitHub*

It might be a bit difficult to notice at first glance, but here is the same scene with TAA enabled:

![godot 4 taa on](/images/godot/taa_enabled.jpg)
*Image credit: JFonS from GitHub*

If you zoom in on both screenshots, though, the difference becomes more clear. The latter screenshot with TAA enabled makes the graphics look much more smooth.

For converting a Godot 3.x project to 4, all you need to do is run the `--convert-3to4` command. You're definitely going to want to make a backup of your project first though; there's no telling what might happen, seeing as we're still in the alpha stages.

There's been 149 commits since the last alpha 9 release. Read the Godot [blog post](https://godotengine.org/article/dev-snapshot-godot-4-0-alpha-10) for an overview of what's new, and see the commit history on [GitHub](https://github.com/godotengine/godot/compare/d9daf3869f27e2afdacb2744168052ce0d4ae43b...4bbe7f0b98de72d6dd77d5ade4b761de375bcf66) for the full list of changes.

*Cover image credit: godotengine.org*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
