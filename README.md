# xiufu-sys



怎么使用dism命令修复win10系统?除了SFC外，Win10系统还有一个命令可以联机修复系统，那就是Dism命令了，那么要怎么修复呢?
　　工作原理：
　　DISM可以联网将你当前的系统文件和官方的原镜像进行比对，然后恢复不一样的文件。
　　命令使用方法：
　　1、按下WIN+X然后选择命令提示符管理员;

　　2、打开后依次执行下面两条命令：
　　DISM.exe /Online /Cleanup-image /Scanhealth
　　DISM.exe /Online /Cleanup-image /Restorehealth

　　第一条命令是扫描你全部系统文件并和官方系统文件对比。
　　第二条命令是把那些不同的系统文件还原成系统官方源文件，跟重装差不多。
　　若要使用你自己的一些来源，不使用 Windows 更新来修复一个联机映像，则键入：
　　Dism /Online /Cleanup-Image /RestoreHealth /Source:c：testmountwindows /LimitAccess
　　在命令中有/online的需要在联网下操作，Win10系统会自动从官方镜像来恢复受损文件。
　　以上就是Win10使用Dism命令自动检查异常文件修复系统的方法了，如果你的系统出现了未知的故障，可以尝试用Dism命令来检查文件修复系统。
