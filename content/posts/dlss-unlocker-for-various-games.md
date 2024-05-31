+++
title = "Unlock DLSS For Faster Framerates and Better Graphics Quality, Regardless of Your GPU Vendor (Including Steam Deck)"
date = 2022-10-18T11:09:28-04:00
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/fsr/kena/cover.jpg"
tags = ["guide", "fsr", "dlss", "steam deck"]
keywords = ["fsr", "amd", "nvidia", "dlss", "steam deck", "kena: bridge of spirits", "cyberpunk 2077"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
You might have heard about NVIDIA's Deep Learning Super Sampling ([DLSS](https://www.nvidia.com/en-us/geforce/technologies/dlss/)). While it may be advantagous for achieving higher framerates at lower resolutions, while still retaining *most* of the same graphics quality, the downside is that the technology is essentially locked behind a paywall: you need to have a RTX GPU in order to use it.

But you don't need to pay an arm and a leg for said GPU. Fortunately for us, we can make use of an alternate technology that offers much of the same capabilities: [FSR 2.1](https://community.amd.com/t5/gaming/amd-fidelityfx-super-resolution-2-1-out-now-even-more-fsr-2/ba-p/544170). With FSR 2.1, we can use this across *any* GPU, including the GTX line of graphics cards, the Steam Deck's APU, and even Intel's integrated graphics. So let's go over how we can make use of FSR 2.1 for games that only have DLSS, and the benefits that come with it.

# How?
It all started with a DLSS unlocker for [*Cyberpunk 2077*](https://www.nexusmods.com/cyberpunk2077/mods/3001). Normally, when running a game that has support for DLSS, this option will either be greyed out or not even be visible when using any GPU outside of the RTX family. This mod adds an injector to disable RTX checking, and will use FSR 2.1 in replacement of the DLSS option in the game's graphics options. This is possible thanks to NVIDIA providing its DLSS implementation as a DLL file; modders can simply replace said DLL file with their own that translates DLSS calls to FSR 2.1.

Thanks to DLSS2FSR being [open-source](https://github.com/PotatoOfDoom/CyberFSR2), modders have been able to modify the code and make it work with other games. You can see here there's no option for DLSS in the Advanced Graphics menu when running [*Kena: Bridge of Spirits*](https://linuxgamingcentral.com/posts/kena-bridge-of-spirits-review/) on my GTX 1660:

![No option for DLSS on Kena](/images/fsr/kena/no_dlss_option.jpg)

However, by installing the [DLSS unlocker mod](https://www.nexusmods.com/kenabridgeofspirits/mods/18), the option now becomes visible:

![No option for DLSS on Kena](/images/fsr/kena/dlss_option.jpg)

There's many other games that support this mod:
- [*DOOM Eternal*](https://www.nexusmods.com/doometernal/mods/1170)
- [*Horizon Zero Dawn*](https://www.nexusmods.com/horizonzerodawn/mods/133)
- [*Marvel's Spider-Man Remastered*](https://www.nexusmods.com/marvelsspidermanremastered/mods/683)
- [*No Man's Sky*](https://www.nexusmods.com/nomanssky/mods/2485)
- [*Rise of the Tomb Raider*](https://www.nexusmods.com/riseofthetombraider/mods/82)
- [*Red Dead Redemption 2*](https://www.nexusmods.com/reddeadredemption2/mods/1640)
- [*The Ascent*](https://www.nexusmods.com/theascent/mods/11)
- [*Ghostrunner*](https://www.nexusmods.com/ghostrunner/mods/17)
- [*Soulstice*](https://www.nexusmods.com/soulstice/mods/3)
- [*Diablo II - Resurrected*](https://www.nexusmods.com/diablo2resurrected/mods/269)
- [*Myst*](https://www.nexusmods.com/myst/mods/3)

There's also a [compatibility list sheet](https://docs.google.com/spreadsheets/d/1XyIoSqo6JQxrpdS9l5l_nZUPvFo1kUaU_Uc2DzsFlQw/edit#gid=0) that you can see for even more games.

# Why?
FSR 2.1 will give us small performance gains over FSR 1.0. The sharpening detail should also be better in most cases (as you can see in the cover photo). In my testing on my NVIDIA GPU, I've also noticed slightly less RAM and VRAM consumption. If that carries the same precedent on the Steam Deck, that should translate to a longer battery life.

# 1. Get the Mod
In this guide, I will be walking through *Kena: Bridge of Spirits* on my Arch desktop. The process should be fairly similar with any other game. If you're wanting to add support for FSR 2.1 on Deck, this is also similar, but I will add a few notes along the way since there are a few differences.

So first thing's first, download the DLSS unlocker mod appropriate for the game you want to use it on. Most of these mods will be available over on [Nexus Mods](https://www.nexusmods.com/). Note that you may need to have an account and be logged in in order to download the mod. Inside the zip file you will usually find three files:
- `nvmgx.dll`
- `nvngx.ini`
- `winmm.dll`

You're going to want to extract these files to where your game's executable file is located. An easy way of getting access to your game's install directory is by right-clicking the game on Steam -> Manage -> Browse local files:

![Browsing install directory for Kena](/images/fsr/kena/browsing_files.jpg)

In the case of *Kena*, these files will go to `/Kena/Binaries/Win64/`:

![DLSS unlocker files for Kena](/images/fsr/kena/dlss_unlocker_files.jpg)

Inside the zip file are also two registry files: `DisableSignatureOverride.reg` and `EnableSignatureOverride.reg`. On desktop you can extract these anywhere you want, but on Deck, you're going to want to extract it to a location that a Flatpak has access to, such as `Documents` or `Downloads` (for the Deck, we'll need to use a Flatpak later on).

# 2. Run Protontricks to Enable Signature Override
We'll need to install [Protontricks](https://github.com/Matoking/protontricks) if you don't already have it. This will give us access to the registry editor. On Arch, it's available on the [AUR](https://aur.archlinux.org/packages/protontricks). On Deck, you can install it as a Flatpak via the Discover app or via the terminal:

`flatpak install flathub com.github.Matoking.protontricks`

Now run the installed application. Select the game that you want to use the mod with. In our case I will go with *Kena*:

![Protontricks game selection](/images/fsr/kena/protontricks_game_selection.jpg)

Ignore the Wine Prefix error. This isn't relevant to us. In the new window that pops up, click "Select the default wineprefix." This should already be the default option selected. Click OK. When you're asked what you want to do with the wineprefix, select "Run regedit."

![Run regedit option in protontricks](/images/fsr/kena/regedit_selection.jpg)

Now you should have the registry editor open. We need to import the `EnableSignatureOverride.reg` file we extracted earlier. Do so by going to Registry -> Import Registry File:

![Importing registry file](/images/fsr/kena/importing_reg_file.jpg)

Find said registry file. If the importation was successful, the registry editor should let you know:

![Importing success](/images/fsr/kena/import_success.jpg)

Note that, if this doesn't work the first time, you may need to try it again. Close the registry editor and all the Protontricks windows.

# 3. Enable DX12 And Make WinMM Native
With *Kena*, we'll need to use DirectX12 in order to make use of FSR 2.1. You can either add this as a launch parameter with `-dx12`, or go to the game's graphics options, and enable DX12 from there. We will also need to make `winmm` native. To do so, add this as a launch parameter (right-click the game in Steam -> Properties):

`WINEDLLOVERRIDES="winmm.dll=n,b" %command%`

![Adding winmm launch parameter](/images/fsr/kena/winmm_native_launch_parameter.jpg)

# 4. Play the Game and See the Difference
DLSS should now be available in the Advanced Graphics menu. I can adjust the quality, from Ultra Performance, Performance, Balanced, Quality, and Ultra Quality. There's also a slider for sharpness scale. Tweak these options depending on what you want for performance and graphics quality.

Here are some comparisons with *Kena*, resolution set to 720p on my 1440p monitor, ultra graphics settings, using [GE-Proton7-37](https://linuxgamingcentral.com/posts/ge-proton7-37-brings-fsr-back/). On the left side is the vanilla FSR 1.0 filter that GE-Proton supplies, the right with FSR 2.1.

Performance:

![FSR 1.0 vs. 2.1 performance](/images/fsr/kena/comparisons/performance.jpg)

Balanced:

![FSR 1.0 vs. 2.1 balanced](/images/fsr/kena/comparisons/balanced.jpg)

Quality:

![FSR 1.0 vs. 2.1 quality](/images/fsr/kena/comparisons/quality.jpg)

Ultra:

![FSR 1.0 vs. 2.1 ultra](/images/fsr/kena/comparisons/ultra.jpg)

FSR 2.1 uses slightly less VRAM and ~1.5 GB less of RAM. We're also seeing ~10% performance increase in most options, albeit for Ultra (which the author of the mod doesn't recommend anyway, since it's apparently a bit buggy). The sharpness is *slightly* better as well.

Please note I haven't tested the DLSS unlocker on Deck; you may not see these improvements there. Other AMD GPUs may also have different results.

**UPDATE (10/24/2022): I have tested [*Kena* on Deck](https://linuxgamingcentral.com/posts/fsr-2.1-vs-fsr-1.0-tested-on-deck/) and can confirm there is indeed a huge framerate difference!**

Should you want to remove the mod, run the registry editor again and import the `DisableSignatureOverride.reg` file.

Special thanks to **PotatoOfDoom1337** for the original *Cyberpunk 2077* mod, and **Goghor** for the *Kena: Bridge of Spirits* version. Also thanks to [**CryoByte33**](https://www.youtube.com/watch?v=1zUloyYPIBo) for the *Cyberpunk 2077* Deck tutorial, whose notes I borrowed for this guide.

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
