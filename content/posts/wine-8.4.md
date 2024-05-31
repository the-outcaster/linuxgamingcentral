+++
title = "Wine Gets Initial Wayland Support!"
date = 2023-03-18T01:12:26Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/wine/8.4.jpg"
tags = ["news", "software update", "wine", "wayland"]
keywords = ["wine wayland", "wine 8.4"]
description = "This, and 51 bug fixes in the 8.4 release!"
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Great news. A few weeks ago, a pull request was submitted for [adding native Wayland support for Wine](https://linuxgamingcentral.com/posts/wine-may-soon-work-with-wayland/). This had initially been met with some skepticism, but parts of the driver have already been implemented with the new release of Wine 8.4. This is brought to you by Alexandros Frantzis from Collabora. Here's what we've got so far:
- winewayland.drv: Add initial driver stub.
- winewayland.drv: Add initial unixlib stub.
- winewayland.drv: Perform basic per-process Wayland initialization.
- winewayland.drv: Report basic monitor information.
- winewayland.drv: Report all advertised monitor modes to Wine.

Hopefully by 9.0 we'll have *full* Wayland support, but this is a great start.

In addition to basic Wayland support, we've also got cleanups in IME support and 51 bug fixes. Fixes are as follows (gaming-related fixes are in bold):
 - **#7585   Thief: the dark project hangs on 'esc' keypress in game if X in 24bpp mode**
 - **#47407  Hard Truck 2: King of The Road (GOG) movies aren't played**
 - **#49266  Amazon Games installs but won't start (needs WindowsFormsApplicationBase startup code?)**
 - **#51848  Multiple applications have very poor performance after 4261369e5d8 (Secondhand Lands, SPORE)**
 - **#54539  Starcraft Remastered Game Initialization Failed**
 - #52912  t2embed:t2embed fails on Windows with the UTF-8 codepage
 - #52948  gdi32:font - test_EnumFonts() fails on Arial Bold on Windows in Russian
 - #53172  advapi32:registry - test_enum_value() has a pair of rare failures in UTF-8 system locales
 - #53182  shell32:shelllink - A save(NULL, TRUE) fails randomly in test_load_save() on Wine
 - #53236  d3d9:device - test_wndproc() sometimes gets an unexpected WM_DISPLAYCHANGE in Wine
 - #53270  test_WSARecv() fails when using wow64 thunks [Wow64ApcRoutine() overwrites return value set by NtContinue()]
 - #53488  The dxgi:dxgi output is too big on debiant
 - #53526  kernel32:sync - test_timer_queue() occasionally fails to delete the timer on Windows 10
 - #53528  ntdll:info - test_query_kerndebug() fails on Windows 8 to 10 1709
 - #53818  foobar2000 v1.6 crashes shortly after startup on Wine 7.19 or higher
 - #53974  d3drm:d3drm sometimes crashes after failing to create the IDirect3DRMDevice* interface in Wine
 - #53975  d3drm:d3drm sometimes fails to create an immediate mode device in Wine
 - #54003  vbscript:run sometimes fails on Windows UTF-8 locales
 - #54008  d3d9:device sometimes fails to create a D3D object in Wine, crashes
 - #54019  The 64-bit ntdll:wow64 fails on Windows 11
 - #54020  The 32-bit ntdll:wow64 fails on Windows 11
 - #54052  winhttp:notification times out randomly in Wine
 - #54058  user32:input - test_ToAscii() fails in the Hindi UTF-8 locale
 - #54078  ntdll:pipe - test_blocking() sometimes fails in Wine when the pipe is not signaled
 - #54168  kernel32:console - test_wait() sometimes fails on Windows 8+
 - #54298  d3d12:d3d12 - test_desktop_window() fails on Windows 10 1709
 - #54299  d3d12:d3d12 - test_create_device() gets an unexpected 0 refcount on Windows 10 1909+
 - #54313  HS_hevo_gc 8.8.1.1 fails to launch
 - #54379  since wine 8.0 print doesn't work any more
 - #54449  nethack crashes
 - #54491  regedit/regproc.c - export_key() is unable to return TRUE
 - #54495  Motorola Ready For Assistant does not start, needs ext-ms-win-networking-wlanapi-l1-1-0.dll
 - #54504  dbghelp:dbghelp, ntdll:wow64 & psapi:psapi_main fail on Windows 11 due to notepad.exe path remapping
 - #54505  psapi:psapi_main - The 64-bit test_EnumProcessModules() gets unexpected Notepad case on Windows 11
 - #54506  psapi:psapi_main - The 64-bit test_EnumProcessModulesEx() gets pcs-6464 and pcs-6432 failures on Windows 11
 - #54507  psapi:psapi_main - The 32-bit test_EnumProcessModulesEx() gets many pcs-3232 failures due to partial copy errors on Windows 11
 - #54509  psapi:psapi_main - The 64-bit test_EnumProcessModules() gets unexpected third module on Windows 11
 - #54531  jsproxy:jsproxy crashes on Windows 11
 - #54553  mmdevapi:propstore - The 32-bit test_setvalue_on_wow64() fails on Windows 10 2004+
 - #54563  The gif is displaying wrongly, with weird backgrounds of various colors
 - #54593  gdi32:dc - The SetDeviceGammaRamp() tests fails on Windows 10 1909
 - #54605  The 32-bit dbghelp:dbghelp cannot run on Windows <= 10 1607 due to IsWow64Process2() call
 - #54617  KakaoTalk IM text edit window leaves artifacts when the text overflows and scroll bar appears
 - #54621  Wine 8.3 64-bit is missing in the Debian bookworm repo
 - #54637  riched20:txtsrv - test_TxGetNaturalSize fails if system GUI font's glyph widths are wider than expected by the test
 - #54645  TextPad 9.1 installation fails in Wine 6 from Linux Mint repo
 - #54649  windows.perception.stub:perception - Windows 10 1607 does not have ISpatialSurfaceObserverStatics2
 - #54657  kernel32:loader - test_import_resolution() gets bad tls data on Windows 7
 - #54663  ldp.exe crashes on unimplemented function wldap32.dll.ldap_set_dbg_flags
 - #54669  imm32:imm32 - ime_install() fails in some locales on Windows
 - #54690  ldp.exe crashes when attempting to connect to an invalid host

Patch notes can also be seen on [WineHQ](https://www.winehq.org/announce/8.4).

*Cover image credit: SoftLan-Nsk/Fulqrum Publishing*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
