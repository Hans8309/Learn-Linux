在Win7笔记本上安装了ubuntu19.04后，GNU GRUB引导的默认启动项是ubuntu，如果希望默认启动项是windows，修改方法如下：

**step1.**  进入Ubuntu系统，按键 Ctrl+Alt+t 打开终端，输入  sudo gedit  /etc/default/grub

**step2.**  打开grub文件以后，第一行代码为 GRUB_DEFAULT=0（以#开头的是注释行，不算代码），意思就是启动菜单顶部的为默认启动项，将0改为4，保存，退出。
（启动菜单中一般共五项，windows位于最后，我的ubuntu19.04 +win7是这样的。）      
默认启动时间是10s，可以这样修改：在GRUB_DEFAULT=0这一行下面，代码是GRUB_TIMEOUT=10，修改数字，保存，退出。
（千万别忘了执行第三步，更新grub文件）

**step3.**  然后在终端中输入 sudo update-grub，也就是更新grub.cfg文件，使刚才的改动生效。

重启电脑，试试修改是否成功。  

--------------------------------------------------------------------------------------------------------

双系统体验后，想删除ubuntu系统的话，
1. 启动电脑进入win7系统， 下载软件MbrFix，将软件MbrFix.exe放在c:盘根目录，方便执行。
2. CMD命令打开终端 ，切换到c:盘根目录，列表找到MbrFix.exe.
3. 输入命令：MbrFix /drive 0 fixmbr /yes 然后按回车键.
4. 重新启动电脑，发现ubuntu的启动选项菜单消失了，直接进入windows的启动菜单选项。
5. 进入win7系统后，用磁盘管理把Ubuntu的分区删除合并即可。


2019.07.14
