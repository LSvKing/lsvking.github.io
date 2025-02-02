---
title: 技巧：动动鼠标 Windows XP提速十倍
author: lsvking
type: post
date: 2008-02-17T16:48:22+00:00
url: /77
categories:
  - 网络

---
**1.加快系统启动速度**

　　Windows XP的启动速度比Windows 2000要快30%左右，但相对于Windows 98仍然要慢了不少，不过，我们可以通过优化设置，来大大提高Windows XP的启动速度。加快系统启动速度主要有以下方法：尽量减少系统在启动时加载的程序与服务；对磁盘及CPU等硬件进行优化设置；修改默认设置，减少启动等待时间等。这些方法大部分既可减少系统启动的时间，又可以节省系统资源，加快电脑运行速度。

　　**(1)Msconfig**

　　Windows XP的启动速度在系统安装初期还比较快，但随着安装的软件不断增多，系统的启动速度会越来越慢，这是由于许多软件把自己加在了启动程序中，这样开机即需运行，大大降低了启动速度，而且也占用了大量的系统资源。对于这样一些程序，我们可以通过系统配置实用程序Msconfig将它们从启动组中排除出去。

　　选择“开始”菜单中的“运行”命令，在“运行”对话框中键入“Msconfig”，回车后会弹出“系统配置实用程序”对话框，选择其中的“启动”选项卡(如图1)，该选项卡中列出了系统启动时加载的项目及来源，仔细查看每个项目是否需要自动加载，否则清除项目前的复选框，加载的项目越少，启动的速度就越快。设置完成后需要重新启动方能生效。

![][1]
  
　　**(2)Bootvis** 

　　Bootvis是微软提供的一个启动优化工具，可提高Windows XP的启动速度。

　　用BootVis提升Windows XP的启动速度必须按照正确的顺序进行操作，否则将不会起到提速的效果。其正确的操作方法如下：

　　启动Bootvis，从其主窗口(如图2)中选择“工具”菜单下的“选项”命令，在“符号路径”处键入Bootvis的安装路径，如“C:Program FilesBootvis”，单击“保存”退出。

![][2]
  
从“跟踪”菜单中选择“下次引导”命令，会弹出“重复跟踪”对话框，单击“确定”按钮，BootVis将引导Windows XP重新启动，默认的重新启动时间是10秒。

　系统重新启动后，BootVis自动开始运行并记录启动进程，生成启动进程的相关BIN文件，并把这个记录文件自动命名为TRACE\_BOOT\_1\_1。程序记录完启动进程文件后，会重新启动BootVis主界面，在“文件”菜单中选择刚刚生成的启动进程文件“TRACE\_BOOT\_1\_1”。

　窗口中即会出现“CPU使用”、“磁盘I/O”、“磁盘使用”、“驱动程序延迟”等几项具体图例供我们分析，不过最好还是让BootVis程序来自动进行分析：从“跟踪”菜单中选择“系统优化”命令，程序会再次重新启动计算机，并分析启动进程文件，从而使计算机启动得更快。

　**(3)禁用多余的服务**

　Windows XP在启动时会有众多程序或服务被调入到系统的内存中，它们往往用来控制Windows系统的硬件设备、内存、文件管理或者其他重要的系统功能。但这些服务有很多对我们用途不大甚至根本没有用，它们的存在会占用内存和系统资源，所以应该将它们禁用，这样最多可以节省70MB的内存空间，系统速度自然也会有很大的提高。

　选择“开始”菜单中的“运行”命令，在“运行”对话框键入“services.msc”后回车，即可打开“服务”窗口。窗口的服务列表中列出了系统提供的所有服务的名称、状态及启动类型。要修改某个服务，可从列表双击它，会弹出它的属性对话框(如图3)，你可从“常规”选项卡对服务进行修改，通过单击“启动”、“停止”、“暂停”、“恢复”四个按钮来修改服务的状态，并可从“启动类型”下拉列表中修改启动类型，启动类型有“自动”、“手动”、“已禁用”三种。如果要禁止某个服务在启动自动加载，可将其启动类型改为“已禁用”。

![][3]
  
Windows XP提供的所有服务有36个默认是自动启动的，实际上，其中只有8个是必须保留的(见下表)，其他的则可根据自己的需要进行设置，每种服务的作用在软件中有提示。

![][4]
  
　　**(4)修改注册表来减少预读取，减少进度条等待时间**

　　Windows XP在启动过程中会出现一个进度条，我们可以通过修改注册表，让进度条只跑一圈就进入登录画面。

　　选择“开始”菜单中的“运行”命令，在“运行”对话框键入“regedit”命令后回车，即可启动注册表编辑器，在注册表中找HKEY\_LOCAL\_MACHINESYSTEMCurrentControlSetControlSession ManagerMemory ManagementPrefetchParameters，选择其下的EnablePrefetcher键，把它的键值改为“1”即可。

**（５)减少开机磁盘扫描等待时间**

　　当Windows日志中记录有非正常关机、死机引起的重新启动，系统就会自动在启动的时候运行磁盘扫描程序。在默认情况下，扫描每个分区前会等待10秒钟，如果每个分区都要等上10秒才能开始进行扫描，再加上扫描本身需要的时间，会耗费相当长的时间才能完成启动过程。对于这种情况我们可以设置取消磁盘扫描的等待时间，甚至禁止对某个磁盘分区进行扫描。

　　选择“开始→运行”，在运行对话框中键入“chkntfs /t:0”，即可将磁盘扫描等待时间设置为0；如果要在计算机启动时忽略扫描某个分区，比如C盘，可以输入“chkntfs /x c:”命令；如果要恢复对C盘的扫描，可使用“chkntfs /d c:”命令，即可还原所有chkntfs默认设置，除了自动文件检查的倒计时之外。

 [1]: http://uimg.qihoo.com/qhimg/quc//450_314/10/01/85/100185dqe3cc5.ca3ae3.jpg
 [2]: http://uimg.qihoo.com/qhimg/quc//359_288/10/01/66/1001663qe36f4.2c3eeb.jpg
 [3]: http://uimg.qihoo.com/qhimg/quc//400_443/1f/02/d1/1f02d11qe3802.bc3464.jpg
 [4]: http://uimg.qihoo.com/qhimg/quc//447_471/19/02/95/190295eqe2f64.6cf2e2.jpg