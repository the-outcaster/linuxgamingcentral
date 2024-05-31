+++
title = "DXVK 2.1 Adds HDR Support, Shader Compilation Improvements"
date = 2023-01-24T21:13:10Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/game_reviews/sonic_frontiers/cover.jpg"
tags = ["news", "software update", "dxvk"]
keywords = ["dxvk", "directx to vulkan", "d3d9", "d3d10", "d3d11", "dx9", "dx10", "dx11"]
description = "HDR support with Gamescope, shader compilation improvements, sample rate shading for older titles, and plenty more!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Sweet new release for the excellent DXVK (DirectX-to-Vulkan) -- a part of what makes up Proton and is responsible for translating DX9/10/11 titles on Linux/Steam Deck. This follows shortly on the heels of the big [Wine 8.0](https://linuxgamingcentral.com/posts/wine-8.0-released/) update.

First up, we have **HDR support** for systems "supporting HDR10 color spaces." This can be enabled by using `DXVK_HDR=1` or setting `dxgi.enableHDR` to `true` in the [config file](https://github.com/doitsujin/dxvk/wiki/Configuration). This should work for D3D12 games as well when using [VKD3D-Proton 2.8](https://linuxgamingcentral.com/posts/vkd3d-proton-2.8/).

Here's a few caveats: **you will need to use Gamescope with `--hdr-enabled`**, as no major DE supports HDR at the moment. Additionally, **you'll need to have an AMD GPU and have the necessary [kernel patches](https://gitlab.freedesktop.org/JoshuaAshton/linux-hdr/-/commits/josh-hdr-colorimetry) installed.** Finally, D3D11 is "not expected to work in most games," and only NVIDIA drivers are expected to work on Windows.

Second, **shader compilation improvements**. Pipeline libraries have been extended with tessellation or geometry shaders to further reduce stutter. One extension in particular was "leveraged" to reduce stutter with MSAA, "provided that the Vulkan driver supports them."

Third, **sample rate shading** for older titles that support MSAA. This will "let users enabled sample rate shading for all shaders." Though this will have "a very high impact on GPU-bound performance," it may "increase overall image quality in certain games that suffer from specular aliasing or shimmering alpha-tested geometry."

Native Linux builds of DXVK now have a [GLFW backend](https://github.com/doitsujin/dxvk/pull/3111) as a "compile-time alternative to the existing SDL2 backend."

Besides this, of course we get the round of bug fixes and improvements. **Game-specific fixes/workarounds** include:
- *Ashes of the Singularity*: Fixed performance regression caused by suboptimal descriptor set allocation.
- *Battlefield: Bad Company 2*: Fixed flickering (#3078, PR #3079)
- *Cardfight!! Vanguard*: Fixed rendering (PR #3068).
- *Gujian 3*: Fixed rendering issues on some GPUs. (#1784)
- *Resident Evil 4 HD*: Fixed invalid Vulkan usage causing a GPU hang on RADV. (PR #3089)
- *Saints Row: The Third*: Fixed a severe performance issue with rain when using the D3D9 renderer. (#2473, PR #3158)
- *Sekiro: Shadows Die Twice*: Fixed stuttering issues on Nvidia GPUs. (#3179)
- *Sonic Frontiers*: Worked around a game bug that would cause shadows to flicker when GPU-bound.
- *Supreme Commander*: Forged Alliance: Fixed a crash after loading (#3058, PR #3060)

That fix for *Sonic Frontiers* in particular sounds interesting. I wonder if that will improve performance at all on NVIDIA GPUs.

**Fixes** include:
- Fixed D3D11 reference counting issues around 2D textures. (#3169)
- Fixed Vulkan validation errors when creating DXGI_FORMAT_A8_UNORM UAVs. Note that UAVs of this format may not work as expected.
- Fixed Vulkan validation errors that would occur when allocating dedicated image memory on Nvidia GPUs in some situations.
- Fixed Vulkan validation errors caused by broken timeline semaphores on 32-bit Proton.

**Workarounds:**
- Worked around an issue with the Uplay overlay being stuck on screen. (#3146) Note that this fix does not apply to Windows as it was achieved by loading winevulkan.dll directly instead of the actual Vulkan loader. Note that this change will break Red Dead Redemption 2 with dxvk-nvapi prior to this commit: jp7677/dxvk-nvapi@ac00a42
- Worked around a bug in AMD's Windows driver as well as AMDVLK that would cause numerous games to crash since DXVK 2.0. (#3172)

Everything else:
- Improved D3D11 command submission logic in order to make overall performance more consistent, and to bring DXVK's behaviour more in line with native D3D11 drivers.
- Fewer threads will be used to perform background optimization of graphics pipeines. This may result in a **smoother gameplay experience** on some systems. Note that this change does not affect initial shader compiling, as finishing that quickly is crucial to avoid stutter.
- The state cache file will now only be created when the first pipeline is written to it, in order to avoid empty cache files. This change mostly affects D3D9 games on systems with EXT_graphics_pipeline_library support.
- The setup script `setup_dxvk.sh` was no longer deemed useful and got removed.

**Note that DXVK 2.1 will NOT work with versions of VKD3D-Proton prior to 2.8.**

See the patch notes on [GitHub](https://github.com/doitsujin/dxvk/releases/tag/v2.1).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
