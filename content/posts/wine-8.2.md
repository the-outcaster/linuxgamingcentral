+++
title = "Wine 8.2 Adds Indeo IV50 Codec Support, Fixes Keyboard Glitch with Final Fantasy XI"
date = 2023-02-17T21:10:24Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/wine/8.2.jpg"
tags = ["news", "software update", "wine"]
keywords = ["wine 8.2", "the void", "if else", "heroes of might", "magic iv", "final fantasy xi"]
description = "This, along with 22 bug fixes."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Wine 8.2 just released, and with it is 22 bug fixes, "better debug information" in Wow64 mode, [Indeo IV50](https://en.wikipedia.org/wiki/Indeo#Implementations) codec support, Wow64 thunks in the WPCAP library, and "monitor names set from EDID data." Some other features have made it in as well.

Bug fixes are as follows (gaming-related fixes are in bold):

- **The Void crashes with builtin d3dx9_36 (needs D3DXFillCubeTextureTX() to return S_OK)**
- **vbscript fails to compile when colon follows Else in If...Else**
- **GOG Heroes of Might and Magic IV crashes on launch**
- **Switching active window (alt+tab or otherwise) away from Final Fantasy XI causes keyboard keys to remain pressed**
- Regression: Visual Studio 2005 "package load failure"
- STDOUT lost from a forked program on Cygwin/MSYS2
- SubLab VST3 plugin fails to register (needs Windows.System.Profile.SystemManufacturers.SmbiosInformation)
- New typelib marshaller depends on IID_IDispatch support from target interface
- opengl32:opengl - test_copy_context() crashes on w11pro64_nv
- d3dcompiler_43:hlsl_d3d11 & d3dcompiler_47:hlsl_d3d11 - test_trig() fails on w11pro64_nv
- Rich Edit inserts newly composed text at wrong position when system IME composition ends while a selection is active
- loader won't launch from PATH unless named "wine"
- vbscript memory leak in For Each with SafeArray as group
- vbscript memory leaks in interp_redim_preserve
- vbscript memory leaks in Global_Split
- Wrong version value is returned from win32_operatingsystem on win10 (regression)
- dbghelp:dbghelp - The 64-bit test_modules() fails on Windows 7
- user32:msg - test_message_conversion()'s broadcast test fails on Windows 7 and 10
- getenv_s returns the wrong value
- VarAbs() does not handle BSTR arguments correctly
- vbscript fails to compile when statement follows ElseIf
- vbscript fails to compile concat when used without space and expression begins with H

See the patch notes at [WineHQ](https://www.winehq.org/announce/8.2).

*Cover image credit: Square Enix*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
