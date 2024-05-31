+++
title = "Wine 8.3 Adds Support for Low Fragmentation Heap, Fixes Stuttering with Path of Exile"
date = 2023-03-04T03:54:32Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/wine/8.3.jpg"
tags = ["news", "software update", "wine"]
keywords = ["wine 8.3", "path of exile", "3d sexvilla 2", "what's the secret", "sacred", "escape from tarkov", "saints row the third"]
description = "Plus smart card support and 29 bug fixes."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Wine 8.3 is out and comes with the following:
- support for [Low Fragmentation Heap](https://learn.microsoft.com/en-us/windows/win32/memory/low-fragmentation-heap)
- smart card support with [PCSC-Lite](https://pcsclite.apdu.fr/)
- "more correct" disassembly with bundled [Zydis](https://github.com/zyantific/zydis) library

Along with this are 29 bug fixes. Gaming-related fixes are in bold:

- **3D Sexvilla 2: extremely long loading times**
- **Path of Exile stutters constantly**
- **Setup of game "What's the Secret?" fails to create icon**
- **Sacred: unhandled exception in Wine 7.14**
- **Escape from Tarkov needs DisplayConfigGetDeviceInfo(DISPLAYCONFIG_DEVICE_INFO_GET_TARGET_NAME) implementation**
- **Saints Row: The Third heavy rain causes heavy FPS reductions**
- Untis 2015 (.NET 4.0 app) crashes on startup with Wine-Mono
- Multiple PC/SC applications need winscard.SCardEstablishContext implementation (AusweisApp2 1.x german identity card app, SmartCard test apps, Seneka EBDYS client, Aruba Key)
- Multiple PC/SC applications need winscard.SCardListReaders implementation (Aruba key, SmartCard test apps)
- Freelist scan can result in O(n) time when allocating
- Button not clickable when dpi setting changed in Office 2007 Installer
- Wine heap performs badly when multiple threads are concurrently allocating or freeing memory
- 6.0.1 Introduces error causing Wavelab to close when loading presets
- ntdll:rtlstr test crashes on win32 arch with hi-IN locale
- KeePassXC needs Windows.Security.Credentials.KeyCredentialManager (UWP)
- rouvy: fails to update with server, unimplemented function bthprops.cpl.BluetoothRegisterForAuthenticationEx
- shlwapi:ordinal- test_SHFormatDateTimeA() fails on the mixed locales configuration
- Swift crashes due to unimplemented api-ms-win-core-realtime-l1-1-1.dll.QueryUnbiasedInterruptTimePrecise function
- Missing ntdll.RtlAddressInSectionTable() implementation causes all GraalVM Native Image exes to crash on load
- Hardwar UIM6.0 crashes in 8.0, doesn't in 6.0.3
- dbghelp:dbghelp- The test_loaded_modules() enumeration fails on Windows 10 1607
- riched20:editor- test_EM_GETSELTEXT() fails in the Hindi locale on Windows
- The 64-bit oleaut32:usrmarshal crashes in Wine
- Rich Edit crashes when Ctrl+Right is pressed at past the final paragraph
- riched20:richole- subtest_InsertObject() fails in the Hindi locale on Windows
- SpeedCommander 20 installer crashes on unimplemented function SHELL32.dll.Shell_GetCachedImageIndexW
- kernel32:locale- test_NLSVersion() fails on Windows 10 22H2
- kernel32:locale- The non-breaking space GetNumberFormatEx() test fails on Windows 11
- kernel32:locale- The NtGetNlsSectionPtr() test fails on Windows 11

See the patch notes on [WineHQ](https://www.winehq.org/announce/8.3) for more info.

*Cover image credit: Grinding Gear Games*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
