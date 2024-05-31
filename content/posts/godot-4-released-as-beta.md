+++
title = "Godot 4 Is Finally Here! (As Beta)"
date = 2022-09-15T14:25:15-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/godot/4_beta1.jpg"
tags = ["news", "software update", "godot"]
keywords = ["godot", ""]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Man. This has been a long release in the making. But it's finally here: Godot 4. After several alpha releases, it's now hit beta. While it may be in beta, it has entered a feature-freeze state, meaning that once Godot 4 has become stable, it's still going to be the same thing that you've got now, only that the bugs have been ironed out.

For those not aware, Godot is a great FOSS alternative to engines like Unity and Unreal Engine. It's capable of making both 2D and 3D games.

As for the release notes, well, there's just *way* too many things to go over. Judging by the release notes it seems it mostly focuses on improvements to the 3D aspect, although there are some goodies for 2D game makers as well. The biggest changes I see is the Vulkan renderer, support for FSR 1.0, and support for a plethora of platforms outside of x86-based devices. But here's a bullet-point list of some of the interesting stuff that I caught:
- **the Vulkan renderer is now used as default**, rather then OpenGL
- a reconstruction of much of the core of the engine to make it a "better base to build on...which will let us improve Godot at a much faster pace"
- D3D12 support, while still maintaining support for older hardware with OpenGL
- tons of new lighting features and improvements
- volumetric fog, which balances "a realistic look and fast performance" for 3D scenes
- sky shaders; dynamic skies that update in real time
- decals
- physical light units
- several new optimization techniques
- **support for FSR 1.0**. 2.1 "is planned for a future beta release"
- many improvements to their in-house 3D physics engine, Godot Physics, and keep it up to par with the Bullet engine that they were using before
- reorganization of physics nodes to improve the user-friendliness
- new server-based navigation system for physical bodies
- several improvements to the animation system, including reduced memory usage thanks to compression
- GDScript (the default scripting language used with Godot) is faster, more stable, and features new property syntax
- the port to .NET 6 support for C# scripts has been "mostly completed." This brings optimizations and new APIs
- the ability to use extensions without having to recompile the engine from source (GDExtension)
- text rendering improvements
- improvements to their audio system "to address various popping issues, race conditions, and overall poor resampling behavior"
- a "more pleasant and reliable experience" when it comes to multiplayer
- dedicated import dialog when importing 3D models and faster texture import speed
- **export support for Raspberry Pi, Microsoft Volterra, Surface Pro X, Pine Phone, VisionFive, ARM Chromebooks, and Asahi Linux**
- new Tiles editor
- new editor theme
- easier to "polish and optimize your web-based games"

Should you upgrade your existing project to Godot 4? The developers don't recommend it. "It is still a bit risky to upgrade projects that are in the late-stages of development. We anticipate that all users will face bugs that make development more challenging than it should be and may even face engine crashes." So you may be better off just starting with a new project. If you insist, however, be sure to make a backup of your project. Godot 4 has a built-in converter for converting Godot 3.x projects to Godot 4, but you'll likely still have to do a lot of manual labor to get yourself up to speed.

You can [download](https://downloads.tuxfamily.org/godotengine/4.0/beta1/) Godot 4, freely available on Linux. You can also get the [.NET 6 build](https://downloads.tuxfamily.org/godotengine/4.0/beta1/mono/) which includes C# scripting support. Some known issues are listed in the Godot blog post, so be aware of those. And be sure to report any bugs that you find!

I've tinkered with Godot in the past...and I might just use it again now. Would really like to work on a Metroidvania or a fighting game...if I wasn't such a procrastinator.

See the [blog post](https://godotengine.org/article/dev-snapshot-godot-4-0-beta-1) for more info. And check out Boiling Steam's recent [post](https://boilingsteam.com/make-game-in-10-minutes-godot/) on getting set up with the engine.

*Cover image credit: Wojtek Pe*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
