+++
title = "Wine 8.6 Adds Fixes for Team Fortress Arcade, Pixel Force: Left 4 Dead, and Hogwarts Legacy"
date = 2023-04-14T20:15:59Z
author = "Mark Dougherty"
authorTwitter = "linuxgamingctr" #do not include @
cover = "/images/wine/8.6.webp"
tags = ["news", "software update", "wine"]
keywords = ["wine", "wine is not an emulator", "wine 8.6", "team fortress arcade", "pixel force left 4 dead", "hogwarts legacy", "matrix awakens megacity"]
description = "25 bugs fixes and an update to the Gecko engine."
showFullContent = false
readingTime = false
draft = false
comments = true
+++
Wine 8.6 is now out. Included in this update is 25 bug fixes, "bundled math library from Musl libc", Gecko updated to 2.47.4, and "improved spool file support in the PostScript driver". Oh, something that caught my eye in the bug fix list, is apparently Watchtower Library 2016 would previously crash when playing a video; this has been fixed. (Kind of curious why someone would use an older version of the program...)

Bug fixes are as follows (game fixes are in bold):
 - **#28586  Team Fortress Arcade & Pixel Force: Left 4 Dead music doesn't play**
 - **#32490  Graphical issues in Inquisitor (red squares painted on the screen)**
 - **#49332  CounterPath Bria Solo crashes after login dialog**
 - **#51178  The Bat! v9.3.4.12: Missing content in TTreeViews on Windows versions higher than 8**
 - **#53781  Multiple apps crash on unimplemented function CFGMGR32.dll.CM_MapCrToWin32Err (Matrix Awakens MegaCity Unreal Engine 5.1 demo, Hogwarts Legacy)**
 - **#54728  Pro Evolution Soccer 2008 demo takes +- 9 minutes to complete extracting 'Pro Evolution Soccer 2008 DEMO.msi' (disabling 'Light' theme works around)**
 - #11436  Pepakura viewer: err:wgl:X11DRV_wglShareLists Could not share display lists, context already created !
 - #18773  Multiple apps need DirectShow MPEG Layer-3 decoder filter / l3codecx.ax (The Westerner, 3D Mark 2001SE)
 - #42372  Watchtower Library 2016 crashes when trying to play a video
 - #49002  Multiple games trigger GL_INVALID_FRAMEBUFFER_OPERATION in wined3d (Free Horror Game "My Place", DiRT Rally 2.0)
 - #52193  schtasks.exe:schtasks fails on Windows 7 when missing privileges
 - #53128  Without elevated privileges schedsvc:rpcapi fails on Windows 7
 - #53269  uiautomationcore:uiautomation fails on Windows 10 1909
 - #53983  Chromium broken sandbox, needs NtQueryInformationProcess with ProcessHandleTable
 - #54106  taskschd:scheduler - test_GetTask() fails on Windows 7 when it has insufficient privileges
 - #54109  schedsvc:rpcapi causes taskschd:scheduler to crash on w7u_adm
 - #54110  CubicSDR crashes on unimplemented function msvcp140.dll.?_Rethrow_future_exception@std@@YAXVexception_ptr@1@@Z
 - #54594  dinput:device8 - test_dik_codes() sometimes gets timeouts on the GitLab CI
 - #54634  schtasks.exe:schtasks causes taskschd:scheduler to crash on w7u_adm and w8adm
 - #54666  Compilation fails with gcc 4.8.4 - error: missing binary operator before token "("
 - #54713  dinput:device8 - test_mouse_keyboard() fails on some Window 7 locales
 - #54772  LDAP Explorer (LEX) fails to connect without SSL
 - #54774  dinput:device8 - test_overlapped_format() sometimes gets a timeout in Wine (GitLab CI)
 - #54781  Wine fails to update existed prefix
 - #54819  DnsQuery_A() mishandles CNAME DNS records

See the patch notes on [WineHQ](https://www.winehq.org/announce/8.6).

*Cover image credit: Warner Bros.*

**WARNING: LGC will be shutting down March 7, 2024. See this [post](https://linuxgamingcentral.com/posts/the-end-of-lgc/) for more details.**
