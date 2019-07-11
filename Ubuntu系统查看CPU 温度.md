在2008年的老旧笔记本上安装了ubuntu19.04桌面版，担心温度太高，想查看一下CPU温度，网上搜索学习了一下。

**Step.1**    Ctrl+Alt+t打开终端，输入：sudo apt-get install lm-sensors
安装完成后，在终端输入： sensors，看是否显示CPU温度信息。显示下面文本信息：

acpitz-acpi-0
Adapter: ACPI interface
temp1:        +69.0°C  (crit = +120.0°C)
temp2:        +69.0°C  (crit = +120.0°C)

coretemp-isa-0000
Adapter: ISA adapter
Core 0:       +70.0°C  (high = +100.0°C, crit = +100.0°C)
Core 1:       +68.0°C  (high = +100.0°C, crit = +100.0°C)

看样子工作正常，接着安装Psensor

**Step.2**     输入： sudo apt-get install psensor
安装完成后，在桌面查看全部应用程序，找到Psensor，执行。

打开菜单“Sensor Preferences” 在Application Indicator标签页勾选2个选项。

打开菜单“首选项”找到Startup标签页，勾选3个选项，可以让系统启动时，自动执行。

参考这位大侠的指导 ： 
https://www.linuxprobe.com/ubuntu-cpu-temperature.html
