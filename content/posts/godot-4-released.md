+++
title = "Godot 4 Finally Released As Stable, Brings 12K Merged Pull Requests, 7K Issues Fixed, and 1.5K Contributors"
date = 2023-03-01T16:54:20Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/godot/4.0_stable/cover.webp"
tags = ["news", "software update", "godot"]
keywords = ["godot 4.0", "godot 4", "godot engine", "godot 4 stable"]
description = "WAY too many changes to list!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Four years in development, and Godot hits the major 4.0 milestone. It's now officially stable. A *huge* congrats to all involved with the development of this engine, and making open-source gaming development a reality.

**The new release boasts Vulkan and OpenGL renderers, a game-specific physics engine, boosted graphics and VFX, drastically improved 3D, 2D, multiplayer and XR workflows, as well as wider localization, accessibility, and platform support.**

In an example of community-driven software development gone right, the increasingly popular free and open source game engine has truly leaned into its ability to leverage user input. For the past 3 years, Godot has been quietly undergoing an ambitious overhaul capitalizing on the experience of its numerous contributors and the feedback of its growing user base.

![Godot 4.0 2D lighting](/images/godot/4.0_stable/2d.webp)

The result: A powerful new release that sees the game engine reviewed from the ground up, improving what worked well and closing the gap on frequently requested features. All while remaining under MIT license, free and open-source forever.

The engine core was rewritten from scratch to build a more robust foundation for evolution. Godot 4.0 now targets developers and gamers who have access to high performance hardware while maintaining and further extending support for users who rely on less powerful devices. 

Like its predecessors, the new release is compatible with Windows, Linux and MacOS, but it also runs in and exports to the web browser and Android devices. 

There’s a quantum leap in visual performance with the new Vulkan backend and support for FSR 1.0, [AMD’s Fidelity FX Super Resolution 1.0](https://github.com/godotengine/godot/pull/51679). This is in addition to OpenGL renderers for devices that are not Vulkan compatible. 

For 3D game developers who previously found Godot better suited for 2D development, this might be the right time to reconsider. Shadows have significantly improved, and the introduction of new real-time global illumination techniques makes it a breeze to achieve great lighting for both large open worlds and smaller or closed environments. This is in addition to multiple new occlusion culling and LOD methods to optimize rendering, as well as a variety of mid and post-processing options including realistic light units. 

![Godot 4.0 3D scene](/images/godot/4.0_stable/3d.webp)

VFX and shader support have also level up. Several atmospheric effects are available out of the box such as Volumetric Fog and Sky Shaders, while decals make it easier than ever to project materials and textures. The shader language has been extended and the visual shader editor is more intuitive.

For 2D game makers, Godot 4.0’s brand new tile editor is a real game changer. It’s effectively a full-fledged level-editing software that brings a plethora of practical additions such as: layers, terrain auto-tiling, a randomized painting system, a tool to copy, stamp, and save selections for reuse, to name just a few.

Godot 4.0 makes importing 2D and 3D assets very straightforward with preview and customization options for every part of the imported asset, its materials and physical properties.

For multiplayer game development, Godot 4.0 networking has become much more reliable with more stable connections, less hanging, and the option to set timeouts and limit network bandwidth. Peer-to-peer networking is available and scene replication is easier than ever. Godot 4.0 can also run in headless mode for server hosting and testing. 

With OpenXR, no plugin is necessary to build XR projects and all major Windows and Linux SteamVR headsets are supported out-of-the-box, including the Oculus and Monado. A dedicated XR toolkit and a project template make it easy to get started and WebXR is also supported for browser games.

![Godot 4.0 editor](/images/godot/4.0_stable/editor.webp)

Godot Physics, the new game-specific physics engine replaces Bullet with major stability improvements, better performance through broadphase optimization and multithreading, as well as a more intuitive workflow and simplified scripting. 

Godot 4.0’s new server-based navigation system supports fully dynamic environments and on-the-fly navigation mesh baking. Any physics body can be marked as an obstacle for automatic collision avoidance and AI agents can use navigation links for complex pathfinding requiring crossing over gaps, walking onto moving platforms, climbing ladders, etc.

With Navigation Links, AI pathfinding is greatly improved. AI agents can navigate to any point of interest in 2D or 3D scenes, crossing over gaps, walking onto moving platforms, climbing ladders and more. 

Speaking of scripting, documentation can be automatically generated from script comments and the script editor offers better syntax highlighting, multiple cursor support, drag and drop interaction with the editor and support for various text-based data files, such as JSON, YAML, and more. 

![Made with Godot Brotato](/images/godot/4.0_stable/brotato.webp)

Godot’s own language, GDScript, has also been revamped for a better coding experience. It features improved syntax, more robust typing, first-class functions and signals, support for unicode characters and faster runtime. 

For C# users, the port to .NET6 opens up all the features of C#10. Engine extensions can now be written in C# where only lower level languages could be used in the past. In addition, the engine now relies on source generators for better performance and error reporting. 

For companies, studios and developers who need to adapt the engine to their specific use cases, the introduction of GDExtension makes it possible to write custom engine modules using high performance languages such as C, C++ or Rust without ever having to recompile Godot. 

UI design is noticeably easier in Godot 4.0 with a new theme editor, multiple window support, more visual layout options, finer control of components and improved text rendering with text wrapping/trimming and access to ligatures and right-to-left languages. Godot 4.0’s editor itself benefits from these improvements. 

To make localization even simpler, the context-aware translation system now supports plurals and generates translation files directly from project scenes and scripts.

![Made with Godot Shima](/images/godot/4.0_stable/shima.webp)

One great example of the editor’s many new features, widgets and docks, is the new movie maker mode which makes it possible to render scenes and record videos or trailer footage directly in the engine. 

Audio in Godot 4.0 is revised for quality and sound cleanliness. It now features a smart track importing system. Sounds are easier to superimpose to create SFX. Most importantly, text-to-speech is available to support and encourage accessibility in games and apps.

Another game-changing improvement in Godot 4.0 is on the animation front. Reuse greatly speeds up the workflow with the addition of animation libraries and a new animation retargeting system. Blending systems have been rewritten from scratch and the animation tree editor now provides much more control and better flexibility to set up advanced animation graphs and complex state machines.

Console portability is always a point of contention between Godot users and critics. It comes down to Godot’s commitment to remain open-source. Any extension of console support would require incorporating console manufacturer’s devkits which are hardly ever open source. 

This said, [W4 Games](https://w4games.com/), a new company created by Godot Engine veterans is developing a free and easy solution for console ports. According to Godot Lead developer Juan Linietsky, beta access is coming soon. 

Godot 4.0 is free to [download](https://godotengine.org/download/), use and modify.

Once again, big congrats to the developers of this huge release. Time to break out the champagne.

*All images used in this article are credit of the Godot team.*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
