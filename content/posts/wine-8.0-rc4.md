+++
title = "Wine 8.0-rc4 Fixes 25 Bugs, Increases Rendering Speed on External Monitor"
date = 2023-01-17T02:45:52Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/wine/8.0-rc4.jpg"
tags = ["news", "software update", "wine"]
keywords = ["wine", "wine is not an emulator", "wine 8.0"]
description = ""
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Wine 8.0 continues in the release candidate stages. RC4 just released, and with it are 25 bug fixes (remember, Wine 8.0 is in feature freeze; only bugs are getting ironed out at this point). Gaming-related fixes have been added for *Guild Wars*, *Petz 4*, and *Hyperdimension Neptunia Re;Birth*. Patch notes are as follows:

 - #48553  Catia (CAD software) refuse to run installation on newest wine   (<=4.18)
 - #51268  Assembler messages: Error: no such instruction: `xsavec (%esp)'
 - #51301  Any action that locks the cursor into place inside the Roblox Client window causes the cursor to freeze
 - #51420  Running any program in Wine causes 100% cpu usage in Xorg
 - #52089  d2d1:d2d1 fails in test_draw_geometry() on Wine
 - #52152  comctl32:edit gets unexpected heights in test_text_position_style() on Windows 10 1809+
 - #52429  Guild Wars: login not possible
 - #52557  GetNetworkParams loops forever on musl
 - #52749  winetricks dotnet35sp1: printfilterpipelinesvc.exe crashes in background
 - #52932  comctl32:edit & user32:edit have test_char_from_pos() failures on Windows with the UTF-8 codepage
 - #52994  mstask:task_trigger - test_GetNextRunTime() fails in Wine on date change
 - #53382  Slow rendering when connected to external monitor
 - #53536  ntdll:rtl - The 32-bit RtlUlonglongByteSwap() breaks test_RtlDecompressBuffer() on Windows
 - #53583  FindNLSStringEx reimplementation doesn't match native
 - #53671  No objects are being rendered in any DX10/11 apps with older GPU drivers
 - #53837  HS_hevo_gc 8.6.1.2 fails to install
 - #54045  ntdll:rtl - test_RtlIpv6StringToAddress() fails on Windows 11
 - #54151  xactengine3_7:xact3 crashes when no speaker is connected
 - #54172  ddraw:ddraw1, ddraw:ddraw2, ddraw:ddraw4, ddraw:ddraw7 - test_window_position() gets the size of the wrong screen in Wine
 - #54180  Petz 4 has corrupt .pet files at startup
 - #54210  Wine fails to compile with Linux 4.11 headers (use of undefined AT_HWCAP2)
 - #54218  RTLD_SELF use breaks musl build since 8.0-rc1
 - #54263  Build of 7.22 fails with mingw-w64 10.0
 - #54264  Hyperdimension Neptunia Re;Birth1 crashes on exit in xactengine notification callback
 - #54287  wineconsole: alternate screen buffer does not work
 
Patch notes can also been seen on [WineHQ](https://www.winehq.org//announce/8.0-rc4).

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
