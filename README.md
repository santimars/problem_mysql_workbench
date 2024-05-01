# problem_mysql_workbench

```
Translated Report (Full Report Below)
-------------------------------------

Process:               MySQLWorkbench [842]
Path:                  /Applications/MySQLWorkbench.app/Contents/MacOS/MySQLWorkbench
Identifier:            com.oracle.workbench.MySQLWorkbench
Version:               8.0.34.CE (1)
Code Type:             ARM-64 (Native)
Parent Process:        launchd [1]
User ID:               501

Date/Time:             2024-05-01 14:47:18.2119 -0500
OS Version:            macOS 14.4.1 (23E224)
Report Version:        12
Anonymous UUID:        754A81E0-E986-50D2-0D2E-B0250A89C2B5


Time Awake Since Boot: 69 seconds

System Integrity Protection: enabled

Crashed Thread:        0  Dispatch queue: com.apple.main-thread

Exception Type:        EXC_BAD_ACCESS (SIGSEGV)
Exception Codes:       KERN_INVALID_ADDRESS at 0x00000000000000e0
Exception Codes:       0x0000000000000001, 0x00000000000000e0

Termination Reason:    Namespace SIGNAL, Code 11 Segmentation fault: 11
Terminating Process:   exc handler [842]

VM Region Info: 0xe0 is not in any region.  Bytes before following region: 4311039776
      REGION TYPE                    START - END         [ VSIZE] PRT/MAX SHRMOD  REGION DETAIL
      UNUSED SPACE AT START
--->  
      __TEXT                      100f54000-100fa8000    [  336K] r-x/r-x SM=COW  /Applications/MySQLWorkbench.app/Contents/MacOS/MySQLWorkbench

Thread 0 Crashed::  Dispatch queue: com.apple.main-thread
0   libmforms.dylib               	       0x102c1c098 mforms::ToolBar::find_item(std::__1::basic_string<char, std::__1::char_traits<char>, std::__1::allocator<char>> const&) + 28
1   libmforms.dylib               	       0x102c1c344 mforms::ToolBar::get_item_checked(std::__1::basic_string<char, std::__1::char_traits<char>, std::__1::allocator<char>> const&) + 12
2   WBExtras                      	       0x101a27a50 -[WBSidebarPanel splitViewDidResizeSubviews:] + 360
3   CoreFoundation                	       0x18c38ab1c __CFNOTIFICATIONCENTER_IS_CALLING_OUT_TO_AN_OBSERVER__ + 148
4   CoreFoundation                	       0x18c41edb8 ___CFXRegistrationPost_block_invoke + 88
5   CoreFoundation                	       0x18c41ed00 _CFXRegistrationPost + 440
6   CoreFoundation                	       0x18c359648 _CFXNotificationPost + 768
7   Foundation                    	       0x18d475464 -[NSNotificationCenter postNotificationName:object:userInfo:] + 88
8   AppKit                        	       0x1903c73f0 -[NSSplitView _sendDidResizeNotificationsIfNecessary] + 256
9   AppKit                        	       0x1903c61f8 -[NSSplitView _restoreFromAutosaveName] + 236
10  AppKit                        	       0x18fcd4c8c -[NSSplitView setAutosaveName:] + 96
11  MySQLWorkbench                	       0x100f8caa0 -[WBModelOverviewPanel init] + 556
12  MySQLWorkbench                	       0x100f8b6d8 -[MainWindowController(MainWindowControllerModel) handleModelCreated] + 28
13  MySQLWorkbench                	       0x100f5f730 -[MainWindowController refreshGUI:argument1:argument2:] + 376
14  MySQLWorkbench                	       0x100f6bd8c windowRefreshGui(wb::RefreshType, std::__1::basic_string<char, std::__1::char_traits<char>, std::__1::allocator<char>> const&, void*, MainWindowController*) + 28
15  libwbprivate.be.dylib         	       0x103a85040 std::__1::function<void (wb::RefreshType, std::__1::basic_string<char, std::__1::char_traits<char>, std::__1::allocator<char>>, void*)>::operator()(wb::RefreshType, std::__1::basic_string<char, std::__1::char_traits<char>, std::__1::allocator<char>>, void*) const + 48
16  libwbprivate.be.dylib         	       0x103a84e24 wb::WBContext::flush_idle_tasks(bool) + 288
17  MySQLWorkbench                	       0x100f6d4f4 -[WBMainController flushIdleTasks:] + 68
18  Foundation                    	       0x18d57829c __NSFirePerformWithOrder + 296
19  CoreFoundation                	       0x18c395254 __CFRUNLOOP_IS_CALLING_OUT_TO_AN_OBSERVER_CALLBACK_FUNCTION__ + 36
20  CoreFoundation                	       0x18c395140 __CFRunLoopDoObservers + 536
21  CoreFoundation                	       0x18c39476c __CFRunLoopRun + 776
22  CoreFoundation                	       0x18c393e0c CFRunLoopRunSpecific + 608
23  HIToolbox                     	       0x196b2f000 RunCurrentEventLoopInMode + 292
24  HIToolbox                     	       0x196b2ee3c ReceiveNextEventCommon + 648
25  HIToolbox                     	       0x196b2eb94 _BlockUntilNextEventMatchingListInModeWithFilter + 76
26  AppKit                        	       0x18fbec970 _DPSNextEvent + 660
27  AppKit                        	       0x1903dedec -[NSApplication(NSEventRouting) _nextEventMatchingEventMask:untilDate:inMode:dequeue:] + 700
28  AppKit                        	       0x18fbdfcb8 -[NSApplication run] + 476
29  AppKit                        	       0x18fbb6f54 NSApplicationMain + 880
30  dyld                          	       0x18bf2e0e0 start + 2360

Thread 1:
0   libsystem_pthread.dylib       	       0x18c2b1d20 start_wqthread + 0

Thread 2:
0   libsystem_pthread.dylib       	       0x18c2b1d20 start_wqthread + 0

Thread 3:
0   libsystem_pthread.dylib       	       0x18c2b1d20 start_wqthread + 0

Thread 4:
0   libsystem_pthread.dylib       	       0x18c2b1d20 start_wqthread + 0

Thread 5:: GRTDispatcher
0   libsystem_kernel.dylib        	       0x18c2799ec __psynch_cvwait + 8
1   libsystem_pthread.dylib       	       0x18c2b7588 _pthread_cond_wait + 1272
2   libglib-2.0.0.dylib           	       0x101d1aab0 g_cond_wait_until + 128
3   libglib-2.0.0.dylib           	       0x101c96cbc g_async_queue_pop_intern_unlocked + 180
4   libglib-2.0.0.dylib           	       0x101c96e28 g_async_queue_timeout_pop + 56
5   libwbpublic.be.dylib          	       0x1023654f4 bec::GRTDispatcher::worker_thread(void*) + 204
6   libglib-2.0.0.dylib           	       0x101cf2064 g_thread_proxy + 68
7   libsystem_pthread.dylib       	       0x18c2b6f94 _pthread_start + 136
8   libsystem_pthread.dylib       	       0x18c2b1d34 thread_start + 8

Thread 6:
0   libsystem_pthread.dylib       	       0x18c2b1d20 start_wqthread + 0

Thread 7:: com.apple.NSEventThread
0   libsystem_kernel.dylib        	       0x18c2761f4 mach_msg2_trap + 8
1   libsystem_kernel.dylib        	       0x18c288b24 mach_msg2_internal + 80
2   libsystem_kernel.dylib        	       0x18c27ee34 mach_msg_overwrite + 476
3   libsystem_kernel.dylib        	       0x18c276578 mach_msg + 24
4   CoreFoundation                	       0x18c396058 __CFRunLoopServiceMachPort + 160
5   CoreFoundation                	       0x18c39491c __CFRunLoopRun + 1208
6   CoreFoundation                	       0x18c393e0c CFRunLoopRunSpecific + 608
7   AppKit                        	       0x18fd15cb4 _NSEventThread + 144
8   libsystem_pthread.dylib       	       0x18c2b6f94 _pthread_start + 136
9   libsystem_pthread.dylib       	       0x18c2b1d34 thread_start + 8


Thread 0 crashed with ARM Thread State (64-bit):
    x0: 0x0000000000000000   x1: 0x000000016eea9358   x2: 0x0000000000000000   x3: 0x000000016eea9368
    x4: 0x0000000000000069   x5: 0x0000000000000046   x6: 0x7261626564695365   x7: 0x0000000101a36a7f
    x8: 0x0000000000000000   x9: 0x00000001ec755b70  x10: 0x000000012d0d3af8  x11: 0x00000000000001ff
   x12: 0x0000000000000170  x13: 0x000000013287f6f0  x14: 0x20000001f3ff818f  x15: 0x00000001f3ff8188
   x16: 0x0000000102c1c338  x17: 0x000000000000003c  x18: 0x0000000000000000  x19: 0x0000600002346740
   x20: 0x0000600001d4c0f0  x21: 0x0000600001d4c118  x22: 0x0000000000000000  x23: 0x0000000000000000
   x24: 0x00000001340bee30  x25: 0x0000000000041400  x26: 0x0000000101a4a000  x27: 0x00000115000000db
   x28: 0x0000000000000060   fp: 0x000000016eea9320   lr: 0x0000000102c1c344
    sp: 0x000000016eea92c0   pc: 0x0000000102c1c098 cpsr: 0x60001000
   far: 0x00000000000000e0  esr: 0x92000006 (Data Abort) byte read Translation fault

Binary Images:
       0x114b2c000 -        0x114b33fff com.oracle.workbench.wb-editors (*) <6d8b6907-2761-3b6b-81b4-ee28cc146748> /Applications/MySQLWorkbench.app/Contents/PlugIns/wb.model.editors.mwbplugin/Contents/MacOS/wb.model.editors
       0x114eac000 -        0x114ecbfff com.oracle.workbench.deb-editors (*) <a27d8f74-c337-3a95-b8c2-c6f708830480> /Applications/MySQLWorkbench.app/Contents/PlugIns/db.mysql.editors.mwbplugin/Contents/MacOS/db.mysql.editors
       0x114814000 -        0x114817fff com.oracle.workbench.printing (*) <1f2617bd-1db7-3dc0-8bf6-cb7a435e1f8d> /Applications/MySQLWorkbench.app/Contents/PlugIns/wb.printing.mwbplugin/Contents/MacOS/wb.printing
       0x114bdc000 -        0x114beffff wb.model.snippets.wbp.dylib (*) <9054eeb5-beb3-3845-92b3-a7f1102733ec> /Applications/MySQLWorkbench.app/Contents/PlugIns/wb.model.snippets.wbp.dylib
       0x114f4c000 -        0x114f73fff db.search.wbp.dylib (*) <78db9fba-1251-34dc-a743-2dc2d6a65230> /Applications/MySQLWorkbench.app/Contents/PlugIns/db.search.wbp.dylib
       0x114e14000 -        0x114e3bfff db.mysql.diff.reporting.wbp.dylib (*) <332816be-477f-3a37-891f-507fd01d8293> /Applications/MySQLWorkbench.app/Contents/PlugIns/db.mysql.diff.reporting.wbp.dylib
       0x1150f0000 -        0x1151a3fff db.mysql.wbp.dylib (*) <4d3735f9-0343-34ee-b432-287c144ddb0d> /Applications/MySQLWorkbench.app/Contents/PlugIns/db.mysql.wbp.dylib
       0x114b64000 -        0x114b7ffff wb.model.editors.wbp.dylib (*) <e5d76ac9-b1aa-3ca4-8a21-87b5b2073a75> /Applications/MySQLWorkbench.app/Contents/PlugIns/wb.model.editors.mwbplugin/Contents/Frameworks/wb.model.editors.wbp.dylib
       0x114c34000 -        0x114c8bfff db.mysql.editors.wbp.dylib (*) <5b5a57d6-e760-3df3-9201-345d1757ee26> /Applications/MySQLWorkbench.app/Contents/PlugIns/db.mysql.editors.mwbplugin/Contents/Frameworks/db.mysql.editors.wbp.dylib
       0x114abc000 -        0x114acbfff wb.printing.wbp.dylib (*) <61f7d454-8b66-39b3-94d6-2095484699ff> /Applications/MySQLWorkbench.app/Contents/PlugIns/wb.printing.mwbplugin/Contents/Frameworks/wb.printing.wbp.dylib
       0x114070000 -        0x11407bfff _sqlite3.cpython-39-darwin.so (*) <2db52fb4-00a3-3e35-8372-ec55e5d4fab4> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/_sqlite3.cpython-39-darwin.so
       0x114830000 -        0x11485bfff _cairo.so (*) <02af61c2-161c-3468-8b22-c52ae9b95067> /Applications/MySQLWorkbench.app/Contents/Resources/libraries/_cairo.so
       0x114700000 -        0x114703fff termios.cpython-39-darwin.so (*) <2592ffd1-df81-35f3-aa35-013170489709> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/termios.cpython-39-darwin.so
       0x113ed0000 -        0x113ee7fff _ctypes.cpython-39-darwin.so (*) <3c182d92-da01-38b0-b343-f0813217d500> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/_ctypes.cpython-39-darwin.so
       0x113c90000 -        0x113c93fff _opcode.cpython-39-darwin.so (*) <66ca7c81-bd5b-3576-acf9-d9fed6883152> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/_opcode.cpython-39-darwin.so
       0x113f18000 -        0x113f1ffff binascii.cpython-39-darwin.so (*) <3c91b78c-c101-32db-9512-ccfab1641e1f> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/binascii.cpython-39-darwin.so
       0x113f00000 -        0x113f07fff _json.cpython-39-darwin.so (*) <1fb00e27-9534-3d35-90c2-6da88d0c1e16> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/_json.cpython-39-darwin.so
       0x113c78000 -        0x113c7ffff _csv.cpython-39-darwin.so (*) <6a8ed529-7ace-3c08-a1f8-294ec2f6af27> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/_csv.cpython-39-darwin.so
       0x1124dc000 -        0x1124effff _datetime.cpython-39-darwin.so (*) <89a859d3-4a8e-3dd3-987c-0ce334345fa9> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/_datetime.cpython-39-darwin.so
       0x113b60000 -        0x113b67fff _sha512.cpython-39-darwin.so (*) <04661a52-e6d0-3062-b3ff-ee07bdac8cbf> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/_sha512.cpython-39-darwin.so
       0x113b4c000 -        0x113b4ffff _random.cpython-39-darwin.so (*) <b5f80988-f517-3c1e-83ec-7882c2daeee9> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/_random.cpython-39-darwin.so
       0x113b38000 -        0x113b3bfff _bisect.cpython-39-darwin.so (*) <e5aff6c8-6d03-35a3-8343-31859b7ae7f4> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/_bisect.cpython-39-darwin.so
       0x113940000 -        0x113947fff _lzma.cpython-39-darwin.so (*) <d4638419-b686-3ff2-8281-0141a75e66b6> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/_lzma.cpython-39-darwin.so
       0x106b80000 -        0x106b83fff _bz2.cpython-39-darwin.so (*) <5d7a9a2b-8239-3af7-8694-46e65545c835> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/_bz2.cpython-39-darwin.so
       0x106144000 -        0x10614bfff zlib.cpython-39-darwin.so (*) <3cce4ca0-1955-3d66-9d68-775bfb18769c> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/zlib.cpython-39-darwin.so
       0x102298000 -        0x10229bfff _posixsubprocess.cpython-39-darwin.so (*) <672d19a9-2c25-36ec-81ca-8cb0b75d81c7> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/_posixsubprocess.cpython-39-darwin.so
       0x101fc8000 -        0x101fcbfff grp.cpython-39-darwin.so (*) <d2a7b18d-4649-3a48-a44d-1c4729d3da03> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/grp.cpython-39-darwin.so
       0x1140a8000 -        0x11418ffff _mforms.so (*) <8de2031b-4240-33b7-87bc-bd3aeebe4f02> /Applications/MySQLWorkbench.app/Contents/Resources/libraries/_mforms.so
       0x1068dc000 -        0x1068e7fff array.cpython-39-darwin.so (*) <d224b585-e162-3920-a484-c1c3ada4a786> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/array.cpython-39-darwin.so
       0x102088000 -        0x10208ffff select.cpython-39-darwin.so (*) <f604fc0e-59ce-38f1-b1f2-ab48423ee75b> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/select.cpython-39-darwin.so
       0x1036d0000 -        0x1036dbfff math.cpython-39-darwin.so (*) <4e93a936-89b3-3cac-8f23-27d367bf6e0c> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/math.cpython-39-darwin.so
       0x102278000 -        0x102287fff _socket.cpython-39-darwin.so (*) <6edcc00a-6122-32e2-ae84-9a01f7f73585> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/_socket.cpython-39-darwin.so
       0x10140c000 -        0x101423fff _pickle.cpython-39-darwin.so (*) <33440dec-f7a8-3e66-814d-49c78fea71d4> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/_pickle.cpython-39-darwin.so
       0x102070000 -        0x102077fff _struct.cpython-39-darwin.so (*) <dff0099a-5e8d-382c-9758-2b121955c5ad> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/_struct.cpython-39-darwin.so
       0x101724000 -        0x101727fff _queue.cpython-39-darwin.so (*) <1583437f-22ee-3516-a077-1168943b102e> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/_queue.cpython-39-darwin.so
       0x101c6c000 -        0x101c73fff utilities.grt.dylib (*) <659b4e7d-5ce4-30ac-8626-aef3e904a442> /Applications/MySQLWorkbench.app/Contents/PlugIns/utilities.grt.dylib
       0x11395c000 -        0x1139d7fff db.mysql.sqlparser.grt.dylib (*) <a54d1446-a5f2-3a42-b504-85dd4f1f5f86> /Applications/MySQLWorkbench.app/Contents/PlugIns/db.mysql.sqlparser.grt.dylib
       0x113ca4000 -        0x113debfff sql.parser.dylib (*) <998b194b-9093-3c25-aecb-d6180bd4c9ee> /Applications/MySQLWorkbench.app/Contents/Frameworks/sql.parser.dylib
       0x11244c000 -        0x112483fff wb.model.grt.dylib (*) <1178847c-381d-32ef-a834-d796a5545a46> /Applications/MySQLWorkbench.app/Contents/PlugIns/wb.model.grt.dylib
       0x103924000 -        0x10393bfff db.mysql.query.grt.dylib (*) <d3aecaa9-3662-3f85-9026-2a19aadbbd1a> /Applications/MySQLWorkbench.app/Contents/PlugIns/db.mysql.query.grt.dylib
       0x112510000 -        0x112573fff db.mysql.grt.dylib (*) <81973f7e-1cbf-30e9-9bff-a302eebb163e> /Applications/MySQLWorkbench.app/Contents/PlugIns/db.mysql.grt.dylib
       0x1125e4000 -        0x11264bfff db.mysql.parser.grt.dylib (*) <c50d3e4d-4f46-3fda-8a7f-04f757f0b0e1> /Applications/MySQLWorkbench.app/Contents/PlugIns/db.mysql.parser.grt.dylib
       0x10162c000 -        0x101633fff _heapq.cpython-39-darwin.so (*) <a56dfd47-634f-3ba9-af0d-e9d009a462ef> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/lib/python3.9/lib-dynload/_heapq.cpython-39-darwin.so
       0x101238000 -        0x101243fff libobjc-trampolines.dylib (*) <e8a1b184-0349-3c61-a119-6543eb038317> /usr/lib/libobjc-trampolines.dylib
       0x101528000 -        0x101563fff libwbbase.dylib (*) <bd9c1be4-e5d9-32e5-9e40-8487c5dc18aa> /Applications/MySQLWorkbench.app/Contents/Frameworks/libwbbase.dylib
       0x10173c000 -        0x1017bbfff libgrt.dylib (*) <ebb94cb4-f8db-3a07-b7c4-472d2b4a769d> /Applications/MySQLWorkbench.app/Contents/Frameworks/libgrt.dylib
       0x1018ac000 -        0x1018f7fff libmysql.canvas.dylib (*) <167fa6a7-c381-37e2-9dee-69d8c6571de1> /Applications/MySQLWorkbench.app/Contents/Frameworks/libmysql.canvas.dylib
       0x1014bc000 -        0x1014cffff libcdbc.dylib (*) <2c84b355-7576-32d1-ba8a-a501ea4ec2d4> /Applications/MySQLWorkbench.app/Contents/Frameworks/libcdbc.dylib
       0x1022b0000 -        0x102523fff libwbpublic.be.dylib (*) <35a65e83-1bdb-394a-9b5a-b1dc08b426b3> /Applications/MySQLWorkbench.app/Contents/Frameworks/libwbpublic.be.dylib
       0x103978000 -        0x103e0ffff libwbprivate.be.dylib (*) <512189f4-7b6f-3623-b9f2-48dd3e7aeaf4> /Applications/MySQLWorkbench.app/Contents/Frameworks/libwbprivate.be.dylib
       0x102b64000 -        0x102c8bfff libmforms.dylib (*) <84f32e12-5f91-308c-b8e4-210a9ebde344> /Applications/MySQLWorkbench.app/Contents/Frameworks/libmforms.dylib
       0x102fd8000 -        0x10324bfff com.apple.python3 (3.9.6) <d4245580-3b32-3926-8c75-88dcc420ad80> /Applications/MySQLWorkbench.app/Contents/Frameworks/Python3.framework/Versions/3.9/Python3
       0x10478c000 -        0x1049c3fff libparsers.dylib (*) <04ca2b4d-8e94-3e70-91f2-ca74a8be1915> /Applications/MySQLWorkbench.app/Contents/Frameworks/libparsers.dylib
       0x104e4c000 -        0x105293fff libmysqlcppconn.9.8.1.0.dylib (*) <cf10b83b-8779-3b5c-b4a8-7be80b49d470> /Applications/MySQLWorkbench.app/Contents/Frameworks/libmysqlcppconn.9.8.1.0.dylib
       0x1019fc000 -        0x101a3ffff WBExtras (*) <89d968aa-dbe5-39b4-a43b-c3efceb5ceb7> /Applications/MySQLWorkbench.app/Contents/Frameworks/WBExtras.framework/Versions/A/WBExtras
       0x101650000 -        0x10169bfff libssh.4.8.7.dylib (*) <644a2312-68f8-31f2-b3cd-2497a6bce099> /Applications/MySQLWorkbench.app/Contents/Frameworks/libssh.4.8.7.dylib
       0x101c8c000 -        0x101dbbfff libglib-2.0.0.dylib (*) <5e4c67c1-640c-3814-abab-5ca5d0ab9514> /Applications/MySQLWorkbench.app/Contents/Frameworks/libglib-2.0.0.dylib
       0x1032d4000 -        0x10340ffff com.sun.Scintilla (3.7.0) <042ff29e-2345-34b0-a29c-98ca50ee21e3> /Applications/MySQLWorkbench.app/Contents/Frameworks/Scintilla.framework/Versions/A/Scintilla
       0x1016d4000 -        0x10170ffff libpcre.1.dylib (*) <acd2b7e0-3887-3810-95a9-5bdfa97ac38e> /Applications/MySQLWorkbench.app/Contents/Frameworks/libpcre.1.dylib
       0x101498000 -        0x10149bfff libgmodule-2.0.0.dylib (*) <38e0aadc-02a2-32ab-9d38-a888305b2c9e> /Applications/MySQLWorkbench.app/Contents/Frameworks/libgmodule-2.0.0.dylib
       0x101e2c000 -        0x101edbfff libcairo.2.dylib (*) <25460f6c-c479-36fb-b709-5b9990673945> /Applications/MySQLWorkbench.app/Contents/Frameworks/libcairo.2.dylib
       0x101b74000 -        0x101bcffff libpixman-1.0.dylib (*) <333fd1e7-e6c6-3b06-8f44-5b403ec8b1cb> /Applications/MySQLWorkbench.app/Contents/Frameworks/libpixman-1.0.dylib
       0x101aec000 -        0x101b17fff libpng16.16.dylib (*) <a14d8e18-558c-3f0d-9270-b2a66b99cbaf> /Applications/MySQLWorkbench.app/Contents/Frameworks/libpng16.16.dylib
       0x1020a0000 -        0x10210bfff libantlr4-runtime.dylib (*) <418f4566-4c26-30b2-98ca-bfd73eb1e8dc> /Applications/MySQLWorkbench.app/Contents/Frameworks/libantlr4-runtime.dylib
       0x101fdc000 -        0x10203bfff libssl.3.dylib (*) <86b29dea-8ee0-31ed-8f98-646ebc524c69> /Applications/MySQLWorkbench.app/Contents/Frameworks/libssl.3.dylib
       0x105690000 -        0x1058d3fff libcrypto.3.dylib (*) <da795c5f-c195-32ad-bd4a-031774375e97> /Applications/MySQLWorkbench.app/Contents/Frameworks/libcrypto.3.dylib
       0x1015cc000 -        0x1015d7fff libmtemplate.dylib (*) <57ca515c-a3b4-34f6-a2c4-8d483f79ec7d> /Applications/MySQLWorkbench.app/Contents/Frameworks/libmtemplate.dylib
       0x106b9c000 -        0x1076dffff libgdal.31.0.3.dylib (*) <82df1e14-804a-3eb0-af49-7a5460308a3e> /Applications/MySQLWorkbench.app/Contents/Frameworks/libgdal.31.0.3.dylib
       0x101b34000 -        0x101b43fff libvsqlitepp.3.dylib (*) <6363a4a0-944b-33dc-9fc6-68d938d554e9> /Applications/MySQLWorkbench.app/Contents/Frameworks/libvsqlitepp.3.dylib
       0x1036f8000 -        0x103857fff libsqlite3.so (*) <d0dd3b94-ba4c-3dc1-8d1f-162c5318b724> /Applications/MySQLWorkbench.app/Contents/Frameworks/libsqlite3.so
       0x10615c000 -        0x10653ffff libmysqlclient.21.dylib (*) <ef665193-7175-3901-97d8-ef8b98358507> /Applications/MySQLWorkbench.app/Contents/Frameworks/libmysqlclient.21.dylib
       0x107d58000 -        0x107ffbfff libproj.25.9.1.1.dylib (*) <bd4f0502-ddd4-357f-bca6-028ad6bc4856> /Applications/MySQLWorkbench.app/Contents/Frameworks/libproj.25.9.1.1.dylib
       0x101bfc000 -        0x101c0ffff libwbssh.dylib (*) <d2cf22e5-6fcb-3208-8f8f-19d0a4e5dbc0> /Applications/MySQLWorkbench.app/Contents/Frameworks/libwbssh.dylib
       0x10150c000 -        0x101513fff libpcrecpp.0.dylib (*) <ed072509-20f0-3e70-9ab6-d90c6560fcce> /Applications/MySQLWorkbench.app/Contents/Frameworks/libpcrecpp.0.dylib
       0x101c38000 -        0x101c4bfff libzip.5.5.dylib (*) <9d841c3e-faee-36ef-a9cb-7f06a58d3185> /Applications/MySQLWorkbench.app/Contents/Frameworks/libzip.5.5.dylib
       0x100f54000 -        0x100fa7fff com.oracle.workbench.MySQLWorkbench (8.0.34.CE) <8d3ca0e1-2f98-38db-b9c2-cb44d7c98967> /Applications/MySQLWorkbench.app/Contents/MacOS/MySQLWorkbench
       0x18c318000 -        0x18c7f0fff com.apple.CoreFoundation (6.9) <33908a83-098f-3437-973e-fb848c4f39df> /System/Library/Frameworks/CoreFoundation.framework/Versions/A/CoreFoundation
       0x18d46c000 -        0x18e0c9fff com.apple.Foundation (6.9) <1b93a4d2-db73-3f3b-a726-c8eacc5128e0> /System/Library/Frameworks/Foundation.framework/Versions/C/Foundation
       0x18fbb2000 -        0x190eeefff com.apple.AppKit (6.9) <8b85317d-d56a-3370-8b78-da6c1d0fb53c> /System/Library/Frameworks/AppKit.framework/Versions/C/AppKit
       0x196afc000 -        0x196dbffff com.apple.HIToolbox (2.1.1) <c315e2a3-3fd1-3a2b-b205-b8b492b0f506> /System/Library/Frameworks/Carbon.framework/Versions/A/Frameworks/HIToolbox.framework/Versions/A/HIToolbox
       0x18bf28000 -        0x18bfb09db dyld (*) <f6dd3ec2-85a4-3ab1-8486-b189cd980ebe> /usr/lib/dyld
               0x0 - 0xffffffffffffffff ??? (*) <00000000-0000-0000-0000-000000000000> ???
       0x18c2b0000 -        0x18c2bcfff libsystem_pthread.dylib (*) <45239f06-cc53-36d0-9933-7776ac7ea2fa> /usr/lib/system/libsystem_pthread.dylib
       0x18c275000 -        0x18c2afffb libsystem_kernel.dylib (*) <2a91fd2c-4cef-3211-a025-7a1c0a8c2db5> /usr/lib/system/libsystem_kernel.dylib

External Modification Summary:
  Calls made by other processes targeting this process:
    task_for_pid: 0
    thread_create: 0
    thread_set_state: 0
  Calls made by this process:
    task_for_pid: 0
    thread_create: 0
    thread_set_state: 0
  Calls made by all processes on this machine:
    task_for_pid: 0
    thread_create: 0
    thread_set_state: 0

VM Region Summary:
ReadOnly portion of Libraries: Total=1.2G resident=0K(0%) swapped_out_or_unallocated=1.2G(100%)
Writable regions: Total=1.9G written=0K(0%) resident=0K(0%) swapped_out=0K(0%) unallocated=1.9G(100%)

                                VIRTUAL   REGION 
REGION TYPE                        SIZE    COUNT (non-coalesced) 
===========                     =======  ======= 
Accelerate framework               256K        2 
Activity Tracing                   256K        1 
CG image                           144K        7 
ColorSync                          624K       30 
CoreAnimation                     1680K       59 
CoreGraphics                        32K        2 
CoreUI image data                  960K       12 
Foundation                          16K        1 
Image IO                            16K        1 
Kernel Alloc Once                   32K        1 
MALLOC                             1.6G       60 
MALLOC guard page                  192K       12 
STACK GUARD                        128K        8 
Stack                            259.8M       11 
VM_ALLOCATE                       14.7M       68 
__AUTH                            1666K      338 
__AUTH_CONST                      27.8M      539 
__CTF                               824        1 
__DATA                            20.0M      602 
__DATA_CONST                      30.9M      620 
__DATA_DIRTY                      1709K      193 
__FONT_DATA                          4K        1 
__LINKEDIT                       575.5M       77 
__OBJC_RO                         71.7M        1 
__OBJC_RW                         2195K        1 
__TEXT                           666.2M      637 
dyld private memory                272K        2 
mapped file                      272.5M       39 
shared memory                      848K       13 
===========                     =======  ======= 
TOTAL                              3.5G     3339 



-----------
Full Report
-----------

{"app_name":"MySQLWorkbench","timestamp":"2024-05-01 14:47:20.00 -0500","app_version":"8.0.34.CE","slice_uuid":"8d3ca0e1-2f98-38db-b9c2-cb44d7c98967","build_version":"1","platform":1,"bundleID":"com.oracle.workbench.MySQLWorkbench","share_with_app_devs":0,"is_first_party":0,"bug_type":"309","os_version":"macOS 14.4.1 (23E224)","roots_installed":0,"name":"MySQLWorkbench","incident_id":"B46D6B09-7A15-4E05-9835-D4AE63700CC7"}
{
  "uptime" : 69,
  "procRole" : "Foreground",
  "version" : 2,
  "userID" : 501,
  "deployVersion" : 210,
  "modelCode" : "Mac14,12",
  "coalitionID" : 1073,
  "osVersion" : {
    "train" : "macOS 14.4.1",
    "build" : "23E224",
    "releaseType" : "User"
  },
  "captureTime" : "2024-05-01 14:47:18.2119 -0500",
  "codeSigningMonitor" : 1,
  "incident" : "B46D6B09-7A15-4E05-9835-D4AE63700CC7",
  "pid" : 842,
  "translated" : false,
  "cpuType" : "ARM-64",
  "roots_installed" : 0,
  "bug_type" : "309",
  "procLaunch" : "2024-05-01 14:47:13.5402 -0500",
  "procStartAbsTime" : 1563941443,
  "procExitAbsTime" : 1675794433,
  "procName" : "MySQLWorkbench",
  "procPath" : "\/Applications\/MySQLWorkbench.app\/Contents\/MacOS\/MySQLWorkbench",
  "bundleInfo" : {"CFBundleShortVersionString":"8.0.34.CE","CFBundleVersion":"1","CFBundleIdentifier":"com.oracle.workbench.MySQLWorkbench"},
  "storeInfo" : {"deviceIdentifierForVendor":"CB36A7AE-5709-56FD-BDC0-7E5E26B5E94A","thirdParty":true},
  "parentProc" : "launchd",
  "parentPid" : 1,
  "coalitionName" : "com.oracle.workbench.MySQLWorkbench",
  "crashReporterKey" : "754A81E0-E986-50D2-0D2E-B0250A89C2B5",
  "codeSigningID" : "com.oracle.workbench.MySQLWorkbench",
  "codeSigningTeamID" : "VB5E2TV963",
  "codeSigningFlags" : 570495745,
  "codeSigningValidationCategory" : 6,
  "codeSigningTrustLevel" : 4294967295,
  "instructionByteStream" : {"beforePC":"2f\/\/l\/17wahKuAAU\/8MB0fpnAqn4XwOp9lcEqfRPBan9ewap\/YMBkQ==","atPC":"FyBOqf8CCOuABwBU8wMBqvQDAKr4IwCRGQNAsugCQPkBgQCR4CMAkQ=="},
  "sip" : "enabled",
  "vmRegionInfo" : "0xe0 is not in any region.  Bytes before following region: 4311039776\n      REGION TYPE                    START - END         [ VSIZE] PRT\/MAX SHRMOD  REGION DETAIL\n      UNUSED SPACE AT START\n--->  \n      __TEXT                      100f54000-100fa8000    [  336K] r-x\/r-x SM=COW  \/Applications\/MySQLWorkbench.app\/Contents\/MacOS\/MySQLWorkbench",
  "exception" : {"codes":"0x0000000000000001, 0x00000000000000e0","rawCodes":[1,224],"type":"EXC_BAD_ACCESS","signal":"SIGSEGV","subtype":"KERN_INVALID_ADDRESS at 0x00000000000000e0"},
  "termination" : {"flags":0,"code":11,"namespace":"SIGNAL","indicator":"Segmentation fault: 11","byProc":"exc handler","byPid":842},
  "vmregioninfo" : "0xe0 is not in any region.  Bytes before following region: 4311039776\n      REGION TYPE                    START - END         [ VSIZE] PRT\/MAX SHRMOD  REGION DETAIL\n      UNUSED SPACE AT START\n--->  \n      __TEXT                      100f54000-100fa8000    [  336K] r-x\/r-x SM=COW  \/Applications\/MySQLWorkbench.app\/Contents\/MacOS\/MySQLWorkbench",
  "extMods" : {"caller":{"thread_create":0,"thread_set_state":0,"task_for_pid":0},"system":{"thread_create":0,"thread_set_state":0,"task_for_pid":0},"targeted":{"thread_create":0,"thread_set_state":0,"task_for_pid":0},"warnings":0},
  "faultingThread" : 0,
  "threads" : [{"triggered":true,"id":8956,"threadState":{"x":[{"value":0},{"value":6155834200},{"value":0},{"value":6155834216},{"value":105},{"value":70},{"value":8241976980680561509},{"value":4322454143},{"value":0},{"value":8262081392,"objc-selector":"isHidden"},{"value":5050809080},{"value":511},{"value":368},{"value":5142738672},{"value":2305843017602269583,"symbolLocation":2305843009213693959,"symbol":"OBJC_CLASS_$_NSView"},{"value":8388575624,"symbolLocation":0,"symbol":"OBJC_CLASS_$_NSView"},{"value":4341220152,"symbolLocation":0,"symbol":"mforms::ToolBar::get_item_checked(std::__1::basic_string<char, std::__1::char_traits<char>, std::__1::allocator<char>> const&)"},{"value":60},{"value":0},{"value":105553153255232},{"value":105553146986736},{"value":105553146986776},{"value":0},{"value":0},{"value":5168164400},{"value":267264},{"value":4322533376},{"value":1189705941211},{"value":96}],"flavor":"ARM_THREAD_STATE64","lr":{"value":4341220164},"cpsr":{"value":1610616832},"fp":{"value":6155834144},"sp":{"value":6155834048},"esr":{"value":2449473542,"description":"(Data Abort) byte read Translation fault"},"pc":{"value":4341219480,"matchesCrashFrame":1},"far":{"value":224}},"queue":"com.apple.main-thread","frames":[{"imageOffset":753816,"symbol":"mforms::ToolBar::find_item(std::__1::basic_string<char, std::__1::char_traits<char>, std::__1::allocator<char>> const&)","symbolLocation":28,"imageIndex":50},{"imageOffset":754500,"symbol":"mforms::ToolBar::get_item_checked(std::__1::basic_string<char, std::__1::char_traits<char>, std::__1::allocator<char>> const&)","symbolLocation":12,"imageIndex":50},{"imageOffset":178768,"symbol":"-[WBSidebarPanel splitViewDidResizeSubviews:]","symbolLocation":360,"imageIndex":54},{"imageOffset":469788,"symbol":"__CFNOTIFICATIONCENTER_IS_CALLING_OUT_TO_AN_OBSERVER__","symbolLocation":148,"imageIndex":76},{"imageOffset":1076664,"symbol":"___CFXRegistrationPost_block_invoke","symbolLocation":88,"imageIndex":76},{"imageOffset":1076480,"symbol":"_CFXRegistrationPost","symbolLocation":440,"imageIndex":76},{"imageOffset":267848,"symbol":"_CFXNotificationPost","symbolLocation":768,"imageIndex":76},{"imageOffset":37988,"symbol":"-[NSNotificationCenter postNotificationName:object:userInfo:]","symbolLocation":88,"imageIndex":77},{"imageOffset":8475632,"symbol":"-[NSSplitView _sendDidResizeNotificationsIfNecessary]","symbolLocation":256,"imageIndex":78},{"imageOffset":8471032,"symbol":"-[NSSplitView _restoreFromAutosaveName]","symbolLocation":236,"imageIndex":78},{"imageOffset":1191052,"symbol":"-[NSSplitView setAutosaveName:]","symbolLocation":96,"imageIndex":78},{"imageOffset":232096,"symbol":"-[WBModelOverviewPanel init]","symbolLocation":556,"imageIndex":75},{"imageOffset":227032,"symbol":"-[MainWindowController(MainWindowControllerModel) handleModelCreated]","symbolLocation":28,"imageIndex":75},{"imageOffset":46896,"symbol":"-[MainWindowController refreshGUI:argument1:argument2:]","symbolLocation":376,"imageIndex":75},{"imageOffset":97676,"symbol":"windowRefreshGui(wb::RefreshType, std::__1::basic_string<char, std::__1::char_traits<char>, std::__1::allocator<char>> const&, void*, MainWindowController*)","symbolLocation":28,"imageIndex":75},{"imageOffset":1101888,"symbol":"std::__1::function<void (wb::RefreshType, std::__1::basic_string<char, std::__1::char_traits<char>, std::__1::allocator<char>>, void*)>::operator()(wb::RefreshType, std::__1::basic_string<char, std::__1::char_traits<char>, std::__1::allocator<char>>, void*) const","symbolLocation":48,"imageIndex":49},{"imageOffset":1101348,"symbol":"wb::WBContext::flush_idle_tasks(bool)","symbolLocation":288,"imageIndex":49},{"imageOffset":103668,"symbol":"-[WBMainController flushIdleTasks:]","symbolLocation":68,"imageIndex":75},{"imageOffset":1098396,"symbol":"__NSFirePerformWithOrder","symbolLocation":296,"imageIndex":77},{"imageOffset":512596,"symbol":"__CFRUNLOOP_IS_CALLING_OUT_TO_AN_OBSERVER_CALLBACK_FUNCTION__","symbolLocation":36,"imageIndex":76},{"imageOffset":512320,"symbol":"__CFRunLoopDoObservers","symbolLocation":536,"imageIndex":76},{"imageOffset":509804,"symbol":"__CFRunLoopRun","symbolLocation":776,"imageIndex":76},{"imageOffset":507404,"symbol":"CFRunLoopRunSpecific","symbolLocation":608,"imageIndex":76},{"imageOffset":208896,"symbol":"RunCurrentEventLoopInMode","symbolLocation":292,"imageIndex":79},{"imageOffset":208444,"symbol":"ReceiveNextEventCommon","symbolLocation":648,"imageIndex":79},{"imageOffset":207764,"symbol":"_BlockUntilNextEventMatchingListInModeWithFilter","symbolLocation":76,"imageIndex":79},{"imageOffset":239984,"symbol":"_DPSNextEvent","symbolLocation":660,"imageIndex":78},{"imageOffset":8572396,"symbol":"-[NSApplication(NSEventRouting) _nextEventMatchingEventMask:untilDate:inMode:dequeue:]","symbolLocation":700,"imageIndex":78},{"imageOffset":187576,"symbol":"-[NSApplication run]","symbolLocation":476,"imageIndex":78},{"imageOffset":20308,"symbol":"NSApplicationMain","symbolLocation":880,"imageIndex":78},{"imageOffset":24800,"symbol":"start","symbolLocation":2360,"imageIndex":80}]},{"id":9015,"frames":[{"imageOffset":7456,"symbol":"start_wqthread","symbolLocation":0,"imageIndex":82}],"threadState":{"x":[{"value":6156398592},{"value":6147},{"value":6155862016},{"value":0},{"value":409604},{"value":18446744073709551615},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0}],"flavor":"ARM_THREAD_STATE64","lr":{"value":0},"cpsr":{"value":4096},"fp":{"value":0},"sp":{"value":6156398592},"esr":{"value":1442840704,"description":" Address size fault"},"pc":{"value":6646603040},"far":{"value":0}}},{"id":9016,"frames":[{"imageOffset":7456,"symbol":"start_wqthread","symbolLocation":0,"imageIndex":82}],"threadState":{"x":[{"value":6156972032},{"value":4867},{"value":6156435456},{"value":0},{"value":409604},{"value":18446744073709551615},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0}],"flavor":"ARM_THREAD_STATE64","lr":{"value":0},"cpsr":{"value":4096},"fp":{"value":0},"sp":{"value":6156972032},"esr":{"value":1442840704,"description":" Address size fault"},"pc":{"value":6646603040},"far":{"value":0}}},{"id":9017,"frames":[{"imageOffset":7456,"symbol":"start_wqthread","symbolLocation":0,"imageIndex":82}],"threadState":{"x":[{"value":6157545472},{"value":19715},{"value":6157008896},{"value":0},{"value":409604},{"value":18446744073709551615},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0}],"flavor":"ARM_THREAD_STATE64","lr":{"value":0},"cpsr":{"value":4096},"fp":{"value":0},"sp":{"value":6157545472},"esr":{"value":1442840704,"description":" Address size fault"},"pc":{"value":6646603040},"far":{"value":0}}},{"id":9020,"frames":[{"imageOffset":7456,"symbol":"start_wqthread","symbolLocation":0,"imageIndex":82}],"threadState":{"x":[{"value":6158118912},{"value":30983},{"value":6157582336},{"value":0},{"value":409604},{"value":18446744073709551615},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0}],"flavor":"ARM_THREAD_STATE64","lr":{"value":0},"cpsr":{"value":4096},"fp":{"value":0},"sp":{"value":6158118912},"esr":{"value":1442840704,"description":" Address size fault"},"pc":{"value":6646603040},"far":{"value":0}}},{"id":9022,"name":"GRTDispatcher","threadState":{"x":[{"value":260},{"value":0},{"value":0},{"value":0},{"value":0},{"value":160},{"value":0},{"value":999998000},{"value":1025},{"value":0},{"value":105553174198552},{"value":2},{"value":0},{"value":0},{"value":0},{"value":0},{"value":305},{"value":8559717352},{"value":0},{"value":105553174198528},{"value":105553162781056},{"value":1},{"value":999998000},{"value":0},{"value":0},{"value":1025},{"value":1280},{"value":0},{"value":1}],"flavor":"ARM_THREAD_STATE64","lr":{"value":6646625672},"cpsr":{"value":2684358656},"fp":{"value":6159265232},"sp":{"value":6159265088},"esr":{"value":1442840704,"description":" Address size fault"},"pc":{"value":6646372844},"far":{"value":0}},"frames":[{"imageOffset":18924,"symbol":"__psynch_cvwait","symbolLocation":8,"imageIndex":83},{"imageOffset":30088,"symbol":"_pthread_cond_wait","symbolLocation":1272,"imageIndex":82},{"imageOffset":584368,"symbol":"g_cond_wait_until","symbolLocation":128,"imageIndex":56},{"imageOffset":44220,"symbol":"g_async_queue_pop_intern_unlocked","symbolLocation":180,"imageIndex":56},{"imageOffset":44584,"symbol":"g_async_queue_timeout_pop","symbolLocation":56,"imageIndex":56},{"imageOffset":742644,"symbol":"bec::GRTDispatcher::worker_thread(void*)","symbolLocation":204,"imageIndex":48},{"imageOffset":417892,"symbol":"g_thread_proxy","symbolLocation":68,"imageIndex":56},{"imageOffset":28564,"symbol":"_pthread_start","symbolLocation":136,"imageIndex":82},{"imageOffset":7476,"symbol":"thread_start","symbolLocation":8,"imageIndex":82}]},{"id":9027,"frames":[{"imageOffset":7456,"symbol":"start_wqthread","symbolLocation":0,"imageIndex":82}],"threadState":{"x":[{"value":6159839232},{"value":0},{"value":6159302656},{"value":0},{"value":278532},{"value":18446744073709551615},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0},{"value":0}],"flavor":"ARM_THREAD_STATE64","lr":{"value":0},"cpsr":{"value":4096},"fp":{"value":0},"sp":{"value":6159839232},"esr":{"value":0,"description":" Address size fault"},"pc":{"value":6646603040},"far":{"value":0}}},{"id":9028,"name":"com.apple.NSEventThread","threadState":{"x":[{"value":268451845},{"value":21592279046},{"value":8589934592},{"value":272691768590336},{"value":0},{"value":272691768590336},{"value":2},{"value":4294967295},{"value":18446744073709550527},{"value":63491},{"value":0},{"value":1},{"value":63491},{"value":77706},{"value":0},{"value":0},{"value":18446744073709551569},{"value":8559701520},{"value":0},{"value":4294967295},{"value":2},{"value":272691768590336},{"value":0},{"value":272691768590336},{"value":6160408680},{"value":8589934592},{"value":21592279046},{"value":21592279046},{"value":4412409862,"symbolLocation":14902,"symbol":"SAFEDataset::Open(GDALOpenInfo*)"}],"flavor":"ARM_THREAD_STATE64","lr":{"value":6646434596},"cpsr":{"value":4096},"fp":{"value":6160408528},"sp":{"value":6160408448},"esr":{"value":1442840704,"description":" Address size fault"},"pc":{"value":6646358516},"far":{"value":0}},"frames":[{"imageOffset":4596,"symbol":"mach_msg2_trap","symbolLocation":8,"imageIndex":83},{"imageOffset":80676,"symbol":"mach_msg2_internal","symbolLocation":80,"imageIndex":83},{"imageOffset":40500,"symbol":"mach_msg_overwrite","symbolLocation":476,"imageIndex":83},{"imageOffset":5496,"symbol":"mach_msg","symbolLocation":24,"imageIndex":83},{"imageOffset":516184,"symbol":"__CFRunLoopServiceMachPort","symbolLocation":160,"imageIndex":76},{"imageOffset":510236,"symbol":"__CFRunLoopRun","symbolLocation":1208,"imageIndex":76},{"imageOffset":507404,"symbol":"CFRunLoopRunSpecific","symbolLocation":608,"imageIndex":76},{"imageOffset":1457332,"symbol":"_NSEventThread","symbolLocation":144,"imageIndex":78},{"imageOffset":28564,"symbol":"_pthread_start","symbolLocation":136,"imageIndex":82},{"imageOffset":7476,"symbol":"thread_start","symbolLocation":8,"imageIndex":82}]}],
  "usedImages" : [
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4642226176,
    "CFBundleIdentifier" : "com.oracle.workbench.wb-editors",
    "size" : 32768,
    "uuid" : "6d8b6907-2761-3b6b-81b4-ee28cc146748",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/PlugIns\/wb.model.editors.mwbplugin\/Contents\/MacOS\/wb.model.editors",
    "name" : "wb.model.editors",
    "CFBundleVersion" : "1.0"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4645896192,
    "CFBundleIdentifier" : "com.oracle.workbench.deb-editors",
    "size" : 131072,
    "uuid" : "a27d8f74-c337-3a95-b8c2-c6f708830480",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/PlugIns\/db.mysql.editors.mwbplugin\/Contents\/MacOS\/db.mysql.editors",
    "name" : "db.mysql.editors",
    "CFBundleVersion" : "1.0"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4638982144,
    "CFBundleIdentifier" : "com.oracle.workbench.printing",
    "size" : 16384,
    "uuid" : "1f2617bd-1db7-3dc0-8bf6-cb7a435e1f8d",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/PlugIns\/wb.printing.mwbplugin\/Contents\/MacOS\/wb.printing",
    "name" : "wb.printing",
    "CFBundleVersion" : "1.0"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4642947072,
    "size" : 81920,
    "uuid" : "9054eeb5-beb3-3845-92b3-a7f1102733ec",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/PlugIns\/wb.model.snippets.wbp.dylib",
    "name" : "wb.model.snippets.wbp.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4646551552,
    "size" : 163840,
    "uuid" : "78db9fba-1251-34dc-a743-2dc2d6a65230",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/PlugIns\/db.search.wbp.dylib",
    "name" : "db.search.wbp.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4645273600,
    "size" : 163840,
    "uuid" : "332816be-477f-3a37-891f-507fd01d8293",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/PlugIns\/db.mysql.diff.reporting.wbp.dylib",
    "name" : "db.mysql.diff.reporting.wbp.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4648271872,
    "size" : 737280,
    "uuid" : "4d3735f9-0343-34ee-b432-287c144ddb0d",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/PlugIns\/db.mysql.wbp.dylib",
    "name" : "db.mysql.wbp.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4642455552,
    "size" : 114688,
    "uuid" : "e5d76ac9-b1aa-3ca4-8a21-87b5b2073a75",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/PlugIns\/wb.model.editors.mwbplugin\/Contents\/Frameworks\/wb.model.editors.wbp.dylib",
    "name" : "wb.model.editors.wbp.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4643307520,
    "size" : 360448,
    "uuid" : "5b5a57d6-e760-3df3-9201-345d1757ee26",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/PlugIns\/db.mysql.editors.mwbplugin\/Contents\/Frameworks\/db.mysql.editors.wbp.dylib",
    "name" : "db.mysql.editors.wbp.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4641767424,
    "size" : 65536,
    "uuid" : "61f7d454-8b66-39b3-94d6-2095484699ff",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/PlugIns\/wb.printing.mwbplugin\/Contents\/Frameworks\/wb.printing.wbp.dylib",
    "name" : "wb.printing.wbp.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4630970368,
    "size" : 49152,
    "uuid" : "2db52fb4-00a3-3e35-8372-ec55e5d4fab4",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/_sqlite3.cpython-39-darwin.so",
    "name" : "_sqlite3.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4639096832,
    "size" : 180224,
    "uuid" : "02af61c2-161c-3468-8b22-c52ae9b95067",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Resources\/libraries\/_cairo.so",
    "name" : "_cairo.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4637851648,
    "size" : 16384,
    "uuid" : "2592ffd1-df81-35f3-aa35-013170489709",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/termios.cpython-39-darwin.so",
    "name" : "termios.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4629266432,
    "size" : 98304,
    "uuid" : "3c182d92-da01-38b0-b343-f0813217d500",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/_ctypes.cpython-39-darwin.so",
    "name" : "_ctypes.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4626907136,
    "size" : 16384,
    "uuid" : "66ca7c81-bd5b-3576-acf9-d9fed6883152",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/_opcode.cpython-39-darwin.so",
    "name" : "_opcode.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4629561344,
    "size" : 32768,
    "uuid" : "3c91b78c-c101-32db-9512-ccfab1641e1f",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/binascii.cpython-39-darwin.so",
    "name" : "binascii.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4629463040,
    "size" : 32768,
    "uuid" : "1fb00e27-9534-3d35-90c2-6da88d0c1e16",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/_json.cpython-39-darwin.so",
    "name" : "_json.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4626808832,
    "size" : 32768,
    "uuid" : "6a8ed529-7ace-3c08-a1f8-294ec2f6af27",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/_csv.cpython-39-darwin.so",
    "name" : "_csv.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4602052608,
    "size" : 81920,
    "uuid" : "89a859d3-4a8e-3dd3-987c-0ce334345fa9",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/_datetime.cpython-39-darwin.so",
    "name" : "_datetime.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4625661952,
    "size" : 32768,
    "uuid" : "04661a52-e6d0-3062-b3ff-ee07bdac8cbf",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/_sha512.cpython-39-darwin.so",
    "name" : "_sha512.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4625580032,
    "size" : 16384,
    "uuid" : "b5f80988-f517-3c1e-83ec-7882c2daeee9",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/_random.cpython-39-darwin.so",
    "name" : "_random.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4625498112,
    "size" : 16384,
    "uuid" : "e5aff6c8-6d03-35a3-8343-31859b7ae7f4",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/_bisect.cpython-39-darwin.so",
    "name" : "_bisect.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4623433728,
    "size" : 32768,
    "uuid" : "d4638419-b686-3ff2-8281-0141a75e66b6",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/_lzma.cpython-39-darwin.so",
    "name" : "_lzma.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4407689216,
    "size" : 16384,
    "uuid" : "5d7a9a2b-8239-3af7-8694-46e65545c835",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/_bz2.cpython-39-darwin.so",
    "name" : "_bz2.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4396957696,
    "size" : 32768,
    "uuid" : "3cce4ca0-1955-3d66-9d68-775bfb18769c",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/zlib.cpython-39-darwin.so",
    "name" : "zlib.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4331241472,
    "size" : 16384,
    "uuid" : "672d19a9-2c25-36ec-81ca-8cb0b75d81c7",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/_posixsubprocess.cpython-39-darwin.so",
    "name" : "_posixsubprocess.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4328292352,
    "size" : 16384,
    "uuid" : "d2a7b18d-4649-3a48-a44d-1c4729d3da03",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/grp.cpython-39-darwin.so",
    "name" : "grp.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4631199744,
    "size" : 950272,
    "uuid" : "8de2031b-4240-33b7-87bc-bd3aeebe4f02",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Resources\/libraries\/_mforms.so",
    "name" : "_mforms.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4404920320,
    "size" : 49152,
    "uuid" : "d224b585-e162-3920-a484-c1c3ada4a786",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/array.cpython-39-darwin.so",
    "name" : "array.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4329078784,
    "size" : 32768,
    "uuid" : "f604fc0e-59ce-38f1-b1f2-ab48423ee75b",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/select.cpython-39-darwin.so",
    "name" : "select.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4352442368,
    "size" : 49152,
    "uuid" : "4e93a936-89b3-3cac-8f23-27d367bf6e0c",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/math.cpython-39-darwin.so",
    "name" : "math.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4331110400,
    "size" : 65536,
    "uuid" : "6edcc00a-6122-32e2-ae84-9a01f7f73585",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/_socket.cpython-39-darwin.so",
    "name" : "_socket.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4315987968,
    "size" : 98304,
    "uuid" : "33440dec-f7a8-3e66-814d-49c78fea71d4",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/_pickle.cpython-39-darwin.so",
    "name" : "_pickle.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4328980480,
    "size" : 32768,
    "uuid" : "dff0099a-5e8d-382c-9758-2b121955c5ad",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/_struct.cpython-39-darwin.so",
    "name" : "_struct.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4319232000,
    "size" : 16384,
    "uuid" : "1583437f-22ee-3516-a077-1168943b102e",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/_queue.cpython-39-darwin.so",
    "name" : "_queue.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4324769792,
    "size" : 32768,
    "uuid" : "659b4e7d-5ce4-30ac-8626-aef3e904a442",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/PlugIns\/utilities.grt.dylib",
    "name" : "utilities.grt.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4623548416,
    "size" : 507904,
    "uuid" : "a54d1446-a5f2-3a42-b504-85dd4f1f5f86",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/PlugIns\/db.mysql.sqlparser.grt.dylib",
    "name" : "db.mysql.sqlparser.grt.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4626989056,
    "size" : 1343488,
    "uuid" : "998b194b-9093-3c25-aecb-d6180bd4c9ee",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/sql.parser.dylib",
    "name" : "sql.parser.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4601462784,
    "size" : 229376,
    "uuid" : "1178847c-381d-32ef-a834-d796a5545a46",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/PlugIns\/wb.model.grt.dylib",
    "name" : "wb.model.grt.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4354883584,
    "size" : 98304,
    "uuid" : "d3aecaa9-3662-3f85-9026-2a19aadbbd1a",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/PlugIns\/db.mysql.query.grt.dylib",
    "name" : "db.mysql.query.grt.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4602265600,
    "size" : 409600,
    "uuid" : "81973f7e-1cbf-30e9-9bff-a302eebb163e",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/PlugIns\/db.mysql.grt.dylib",
    "name" : "db.mysql.grt.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4603133952,
    "size" : 425984,
    "uuid" : "c50d3e4d-4f46-3fda-8a7f-04f757f0b0e1",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/PlugIns\/db.mysql.parser.grt.dylib",
    "name" : "db.mysql.parser.grt.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4318216192,
    "size" : 32768,
    "uuid" : "a56dfd47-634f-3ba9-af0d-e9d009a462ef",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/lib\/python3.9\/lib-dynload\/_heapq.cpython-39-darwin.so",
    "name" : "_heapq.cpython-39-darwin.so"
  },
  {
    "source" : "P",
    "arch" : "arm64e",
    "base" : 4314071040,
    "size" : 49152,
    "uuid" : "e8a1b184-0349-3c61-a119-6543eb038317",
    "path" : "\/usr\/lib\/libobjc-trampolines.dylib",
    "name" : "libobjc-trampolines.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4317151232,
    "size" : 245760,
    "uuid" : "bd9c1be4-e5d9-32e5-9e40-8487c5dc18aa",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libwbbase.dylib",
    "name" : "libwbbase.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4319330304,
    "size" : 524288,
    "uuid" : "ebb94cb4-f8db-3a07-b7c4-472d2b4a769d",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libgrt.dylib",
    "name" : "libgrt.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4320837632,
    "size" : 311296,
    "uuid" : "167fa6a7-c381-37e2-9dee-69d8c6571de1",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libmysql.canvas.dylib",
    "name" : "libmysql.canvas.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4316708864,
    "size" : 81920,
    "uuid" : "2c84b355-7576-32d1-ba8a-a501ea4ec2d4",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libcdbc.dylib",
    "name" : "libcdbc.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4331339776,
    "size" : 2572288,
    "uuid" : "35a65e83-1bdb-394a-9b5a-b1dc08b426b3",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libwbpublic.be.dylib",
    "name" : "libwbpublic.be.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4355227648,
    "size" : 4816896,
    "uuid" : "512189f4-7b6f-3623-b9f2-48dd3e7aeaf4",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libwbprivate.be.dylib",
    "name" : "libwbprivate.be.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4340465664,
    "size" : 1212416,
    "uuid" : "84f32e12-5f91-308c-b8e4-210a9ebde344",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libmforms.dylib",
    "name" : "libmforms.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4345135104,
    "CFBundleShortVersionString" : "3.9.6",
    "CFBundleIdentifier" : "com.apple.python3",
    "size" : 2572288,
    "uuid" : "d4245580-3b32-3926-8c75-88dcc420ad80",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Python3.framework\/Versions\/3.9\/Python3",
    "name" : "Python3",
    "CFBundleVersion" : "3.9.6"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4369989632,
    "size" : 2326528,
    "uuid" : "04ca2b4d-8e94-3e70-91f2-ca74a8be1915",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libparsers.dylib",
    "name" : "libparsers.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4377067520,
    "size" : 4489216,
    "uuid" : "cf10b83b-8779-3b5c-b4a8-7be80b49d470",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libmysqlcppconn.9.8.1.0.dylib",
    "name" : "libmysqlcppconn.9.8.1.0.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4322213888,
    "size" : 278528,
    "uuid" : "89d968aa-dbe5-39b4-a43b-c3efceb5ceb7",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/WBExtras.framework\/Versions\/A\/WBExtras",
    "name" : "WBExtras",
    "CFBundleVersion" : "1.0"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4318363648,
    "size" : 311296,
    "uuid" : "644a2312-68f8-31f2-b3cd-2497a6bce099",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libssh.4.8.7.dylib",
    "name" : "libssh.4.8.7.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4324900864,
    "size" : 1245184,
    "uuid" : "5e4c67c1-640c-3814-abab-5ca5d0ab9514",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libglib-2.0.0.dylib",
    "name" : "libglib-2.0.0.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4348264448,
    "CFBundleShortVersionString" : "3.7.0",
    "CFBundleIdentifier" : "com.sun.Scintilla",
    "size" : 1294336,
    "uuid" : "042ff29e-2345-34b0-a29c-98ca50ee21e3",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/Scintilla.framework\/Versions\/A\/Scintilla",
    "name" : "Scintilla",
    "CFBundleVersion" : "3.7.0"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4318904320,
    "size" : 245760,
    "uuid" : "acd2b7e0-3887-3810-95a9-5bdfa97ac38e",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libpcre.1.dylib",
    "name" : "libpcre.1.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4316561408,
    "size" : 16384,
    "uuid" : "38e0aadc-02a2-32ab-9d38-a888305b2c9e",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libgmodule-2.0.0.dylib",
    "name" : "libgmodule-2.0.0.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4326604800,
    "size" : 720896,
    "uuid" : "25460f6c-c479-36fb-b709-5b9990673945",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libcairo.2.dylib",
    "name" : "libcairo.2.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4323753984,
    "size" : 376832,
    "uuid" : "333fd1e7-e6c6-3b06-8f44-5b403ec8b1cb",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libpixman-1.0.dylib",
    "name" : "libpixman-1.0.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4323196928,
    "size" : 180224,
    "uuid" : "a14d8e18-558c-3f0d-9270-b2a66b99cbaf",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libpng16.16.dylib",
    "name" : "libpng16.16.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4329177088,
    "size" : 442368,
    "uuid" : "418f4566-4c26-30b2-98ca-bfd73eb1e8dc",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libantlr4-runtime.dylib",
    "name" : "libantlr4-runtime.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4328374272,
    "size" : 393216,
    "uuid" : "86b29dea-8ee0-31ed-8f98-646ebc524c69",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libssl.3.dylib",
    "name" : "libssl.3.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4385734656,
    "size" : 2375680,
    "uuid" : "da795c5f-c195-32ad-bd4a-031774375e97",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libcrypto.3.dylib",
    "name" : "libcrypto.3.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4317822976,
    "size" : 49152,
    "uuid" : "57ca515c-a3b4-34f6-a2c4-8d483f79ec7d",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libmtemplate.dylib",
    "name" : "libmtemplate.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4407803904,
    "size" : 11812864,
    "uuid" : "82df1e14-804a-3eb0-af49-7a5460308a3e",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libgdal.31.0.3.dylib",
    "name" : "libgdal.31.0.3.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4323491840,
    "size" : 65536,
    "uuid" : "6363a4a0-944b-33dc-9fc6-68d938d554e9",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libvsqlitepp.3.dylib",
    "name" : "libvsqlitepp.3.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4352606208,
    "size" : 1441792,
    "uuid" : "d0dd3b94-ba4c-3dc1-8d1f-162c5318b724",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libsqlite3.so",
    "name" : "libsqlite3.so"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4397056000,
    "size" : 4079616,
    "uuid" : "ef665193-7175-3901-97d8-ef8b98358507",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libmysqlclient.21.dylib",
    "name" : "libmysqlclient.21.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4426399744,
    "size" : 2768896,
    "uuid" : "bd4f0502-ddd4-357f-bca6-028ad6bc4856",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libproj.25.9.1.1.dylib",
    "name" : "libproj.25.9.1.1.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4324311040,
    "size" : 81920,
    "uuid" : "d2cf22e5-6fcb-3208-8f8f-19d0a4e5dbc0",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libwbssh.dylib",
    "name" : "libwbssh.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4317036544,
    "size" : 32768,
    "uuid" : "ed072509-20f0-3e70-9ab6-d90c6560fcce",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libpcrecpp.0.dylib",
    "name" : "libpcrecpp.0.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4324556800,
    "size" : 81920,
    "uuid" : "9d841c3e-faee-36ef-a9cb-7f06a58d3185",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/Frameworks\/libzip.5.5.dylib",
    "name" : "libzip.5.5.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64",
    "base" : 4311040000,
    "CFBundleShortVersionString" : "8.0.34.CE",
    "CFBundleIdentifier" : "com.oracle.workbench.MySQLWorkbench",
    "size" : 344064,
    "uuid" : "8d3ca0e1-2f98-38db-b9c2-cb44d7c98967",
    "path" : "\/Applications\/MySQLWorkbench.app\/Contents\/MacOS\/MySQLWorkbench",
    "name" : "MySQLWorkbench",
    "CFBundleVersion" : "1"
  },
  {
    "source" : "P",
    "arch" : "arm64e",
    "base" : 6647021568,
    "CFBundleShortVersionString" : "6.9",
    "CFBundleIdentifier" : "com.apple.CoreFoundation",
    "size" : 5083136,
    "uuid" : "33908a83-098f-3437-973e-fb848c4f39df",
    "path" : "\/System\/Library\/Frameworks\/CoreFoundation.framework\/Versions\/A\/CoreFoundation",
    "name" : "CoreFoundation",
    "CFBundleVersion" : "2420"
  },
  {
    "source" : "P",
    "arch" : "arm64e",
    "base" : 6665191424,
    "CFBundleShortVersionString" : "6.9",
    "CFBundleIdentifier" : "com.apple.Foundation",
    "size" : 12967936,
    "uuid" : "1b93a4d2-db73-3f3b-a726-c8eacc5128e0",
    "path" : "\/System\/Library\/Frameworks\/Foundation.framework\/Versions\/C\/Foundation",
    "name" : "Foundation",
    "CFBundleVersion" : "2420"
  },
  {
    "source" : "P",
    "arch" : "arm64e",
    "base" : 6706372608,
    "CFBundleShortVersionString" : "6.9",
    "CFBundleIdentifier" : "com.apple.AppKit",
    "size" : 20172800,
    "uuid" : "8b85317d-d56a-3370-8b78-da6c1d0fb53c",
    "path" : "\/System\/Library\/Frameworks\/AppKit.framework\/Versions\/C\/AppKit",
    "name" : "AppKit",
    "CFBundleVersion" : "2487.50.124"
  },
  {
    "source" : "P",
    "arch" : "arm64e",
    "base" : 6823067648,
    "CFBundleShortVersionString" : "2.1.1",
    "CFBundleIdentifier" : "com.apple.HIToolbox",
    "size" : 2899968,
    "uuid" : "c315e2a3-3fd1-3a2b-b205-b8b492b0f506",
    "path" : "\/System\/Library\/Frameworks\/Carbon.framework\/Versions\/A\/Frameworks\/HIToolbox.framework\/Versions\/A\/HIToolbox",
    "name" : "HIToolbox"
  },
  {
    "source" : "P",
    "arch" : "arm64e",
    "base" : 6642892800,
    "size" : 559580,
    "uuid" : "f6dd3ec2-85a4-3ab1-8486-b189cd980ebe",
    "path" : "\/usr\/lib\/dyld",
    "name" : "dyld"
  },
  {
    "size" : 0,
    "source" : "A",
    "base" : 0,
    "uuid" : "00000000-0000-0000-0000-000000000000"
  },
  {
    "source" : "P",
    "arch" : "arm64e",
    "base" : 6646595584,
    "size" : 53248,
    "uuid" : "45239f06-cc53-36d0-9933-7776ac7ea2fa",
    "path" : "\/usr\/lib\/system\/libsystem_pthread.dylib",
    "name" : "libsystem_pthread.dylib"
  },
  {
    "source" : "P",
    "arch" : "arm64e",
    "base" : 6646353920,
    "size" : 241660,
    "uuid" : "2a91fd2c-4cef-3211-a025-7a1c0a8c2db5",
    "path" : "\/usr\/lib\/system\/libsystem_kernel.dylib",
    "name" : "libsystem_kernel.dylib"
  }
],
  "sharedCache" : {
  "base" : 6642139136,
  "size" : 4189880320,
  "uuid" : "a53b7d2f-a773-3524-8828-248b33ef0b4e"
},
  "vmSummary" : "ReadOnly portion of Libraries: Total=1.2G resident=0K(0%) swapped_out_or_unallocated=1.2G(100%)\nWritable regions: Total=1.9G written=0K(0%) resident=0K(0%) swapped_out=0K(0%) unallocated=1.9G(100%)\n\n                                VIRTUAL   REGION \nREGION TYPE                        SIZE    COUNT (non-coalesced) \n===========                     =======  ======= \nAccelerate framework               256K        2 \nActivity Tracing                   256K        1 \nCG image                           144K        7 \nColorSync                          624K       30 \nCoreAnimation                     1680K       59 \nCoreGraphics                        32K        2 \nCoreUI image data                  960K       12 \nFoundation                          16K        1 \nImage IO                            16K        1 \nKernel Alloc Once                   32K        1 \nMALLOC                             1.6G       60 \nMALLOC guard page                  192K       12 \nSTACK GUARD                        128K        8 \nStack                            259.8M       11 \nVM_ALLOCATE                       14.7M       68 \n__AUTH                            1666K      338 \n__AUTH_CONST                      27.8M      539 \n__CTF                               824        1 \n__DATA                            20.0M      602 \n__DATA_CONST                      30.9M      620 \n__DATA_DIRTY                      1709K      193 \n__FONT_DATA                          4K        1 \n__LINKEDIT                       575.5M       77 \n__OBJC_RO                         71.7M        1 \n__OBJC_RW                         2195K        1 \n__TEXT                           666.2M      637 \ndyld private memory                272K        2 \nmapped file                      272.5M       39 \nshared memory                      848K       13 \n===========                     =======  ======= \nTOTAL                              3.5G     3339 \n",
  "legacyInfo" : {
  "threadTriggered" : {
    "queue" : "com.apple.main-thread"
  }
},
  "logWritingSignature" : "e65855980280c2fa12e348252feb0dab74a6ae82",
  "trialInfo" : {
  "rollouts" : [
    {
      "rolloutId" : "648a2601f74c42732876cb5b",
      "factorPackIds" : {
        "SIRI_TEXT_TO_SPEECH" : "6621b75997ed0c66d039bde8"
      },
      "deploymentId" : 240000158
    },
    {
      "rolloutId" : "60da5e84ab0ca017dace9abf",
      "factorPackIds" : {

      },
      "deploymentId" : 240000008
    }
  ],
  "experiments" : [
    {
      "treatmentId" : "2dffbe18-a39a-4f33-ada9-2cce30af39ca",
      "experimentId" : "6384d56b96e8d228551ec182",
      "deploymentId" : 400000023
    },
    {
      "treatmentId" : "a34d22a1-a1a5-4126-a477-0c499e502c6a",
      "experimentId" : "65835bc103dc58766bab2d27",
      "deploymentId" : 400000011
    }
  ]
}
}

Model: Mac14,12, BootROM 10151.101.3, proc 10:6:4 processors, 16 GB, SMC 
Graphics: Apple M2 Pro, Apple M2 Pro, Built-In
Display: Philips, 1360 x 768, Main, MirrorOff, Online
Memory Module: LPDDR5, Micron
AirPort: spairport_wireless_card_type_wifi (0x14E4, 0x4388), wl0: Jan 13 2024 06:19:25 version 23.30.42.0.41.51.132 FWID 01-b1f1a4ed
AirPort: 
Bluetooth: Version (null), 0 services, 0 devices, 0 incoming serial ports
Network Service: Ethernet, Ethernet, en0
Network Service: iPad, Ethernet, en10
Network Service: Wi-Fi, AirPort, en1
USB Device: USB31Bus
USB Device: USB3.0 Hub
USB Device: USB3.0 Hub
USB Device: USB3.0 Card Reader
USB Device: USB2.0 Hub
USB Device: USB Receiver
USB Device: USB2.0 Hub
USB Device: USB Receiver
USB Device: USB31Bus
USB Device: USB31Bus
USB Device: USB31Bus
USB Device: USB31Bus
USB Device: iPad
Thunderbolt Bus: Mac mini, Apple Inc.
Thunderbolt Bus: Mac mini, Apple Inc.
Thunderbolt Bus: Mac mini, Apple Inc.
Thunderbolt Bus: Mac mini, Apple Inc.

```
