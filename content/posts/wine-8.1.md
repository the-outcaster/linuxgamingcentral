+++
title = "Wine 8.1 Fixes Bad Performance with Anno 1880, Crash with GOG Galaxy"
date = 2023-02-03T03:28:46Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/wine/8.1.jpg"
tags = ["news", "software update", "wine"]
keywords = ["wine", "wine is not an emulator", "anno 1880 on wine", "gog galaxy"]
description = "Windows 10 is now set as the Windows version with new prefixes, plus the usual set of bug fixes."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Less than two weeks after the massive [8.0 release of Wine](https://linuxgamingcentral.com/posts/wine-8.0-released/), Wine 8.1 is already available. The Windows version is now set to Windows 10 for new prefixes. A total of 27 bugs were fixed (gaming-related fixes are sorted first and in bold):
- **Dungeons & Dragons Online crashes on FreeBSD**
- **Multiple Blizzard games need dxgi and d3d11 dlls mapped without hole between two LOAD segments (Diablo III v2.6.1, 49286+, World of Warcraft, Overwatch)**
- **Anno 1800: Super slow & bad performance**
- **Wine don't recognize Ipega PG-9025 LT, RT and right analog stick is miss-mapped to RT and LT**
- **GOG Galaxy crashes in GetExtendedTcpTable()**
- **Logitech X-56 Stick crashes the joystick subsystem if connected**
- FL Studio: Pressing backspace while editing the name of something closes edit name window prematurely
- Never exited critical section in freetype.c
- Device read errors logged in dmesg when running wine commands with empty CD/DVD drive, since 5.5
- msi:package fails on Windows 10 if privileges not high enough
- gdi32:driver sometimes fails with a STATUS_GRAPHICS_PRESENT_OCCLUDED error
- The dinput8:hid output is too big in Wine
- winemac.drv not functional on non metal GPUs
- Free PC Audit 5.1.211.96 fails to show info in 'Brief' tab (needs GetBinaryValue method of the StdRegProv class)
- winhttp:url assumes 0xfb00 cannot be converted to the ANSI codepage, fails with UTF-8 codepage
- ieframe:webbrowser - test_ClientSite() has a rare failure on Windows 10 1809+
- adsldp:ldap - test_ParseDisplayName() sometimes fails to connect to the server
- cmd.exe: FOR /F USEBACKQ doesn't handle UTF-16 output of commands.
- Snagit needs Win32_Volume class ( 'select deviceid from win32_volume where driveletter =C:')
- ListView doesn't refresh when changing between List and Details styles.
- RtlCopyContext buffer overflow
- nsi:nsi - test_tcp_tables() sometimes crashes in Wine
- AviUtl shows Japanese text as garbage after conversion in ExEdit edit box
- crypt32:cert - testVerifyRevocation() gets unexpected success in Wine on second run
- Spurious fixme message when calling ScrollWindow()
- RtlGenRandom fails on systems with more than 128 cores
- ws2_32:sock - test_reuseaddr() overflows a sockaddr variable by reading an AF_INET6 peer name into it

See the patch notes on [WineHQ](https://www.winehq.org/announce/8.1).

*Cover image credit: Ubisoft*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
