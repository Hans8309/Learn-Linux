# SSH远程连接ubuntu系统

安装好ubuntu desktop版本，系统默认没有安装ssh服务，需要手动安装。

**Step.1**
Ctrl+Alt+t 打开终端窗口，输入命令： sudo apt-get install openssh-server

**Step.2**
在Windows远程控制主机上，下载MobaXterm控制软件.  
打开[MobaXterm官网](https://mobaxterm.mobatek.net/)
进入[Download页面](https://mobaxterm.mobatek.net/download.html) 下载免费的家庭版Home Edition.  
下载免安装的 Portable 版本最好，不需要安装，单文件使用非常方便.
MobaXterm Portable v11.0 文件大小23.8M.不算太大.  
打开MobaXterm软件，建立 New session，选择SSH，填写远程ubuntu主机的IP地址，按ok按钮即可进入终端控制窗口。
