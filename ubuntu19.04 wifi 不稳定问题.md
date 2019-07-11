2019年7月在2008年购买的笔记本HP V3743TU上安装了ubuntu 19.04 ，CPU是intel pentium 1.6G双核，2G内存。前几年换的一个128G固态硬盘。
在Win7 64位系统上安装了 ubuntu 19.04 ，跑起来感觉有点吃力，启动有点慢，wifi过一会儿就断线了。网上搜了几个方法，试了一下，问题终于解决了。

**Step.1**  按键 Ctrl+Alt+t 进入终端窗口，输入： sudo iwconfig   出现下列文本提示:
lo        no wireless extensions.

wls5      IEEE 802.11  ESSID:"AC86U_5G"

          Mode:Managed  Frequency:5.785 GHz  Access Point: 0C:9D:92:4B:0F:14
          
          Bit Rate=36 Mb/s   Tx-Power=14 dBm
          
          Retry short limit:7   RTS thr:off   Fragment thr:off
          
          Encryption key:off
          
          Power Management:on
          
          Link Quality=56/70  Signal level=-54 dBm
          
          Rx invalid nwid:0  Rx invalid crypt:0  Rx invalid frag:0
          
          Tx excessive retries:0  Invalid misc:81   Missed beacon:0
          

ens3      no wireless extensions.


**Step.2**   记住第二行最前面的 wls5(这是我电脑无线网卡的名称，每个WiFi设备不一样）
输入： sudo iwconfig wls5 power off   
这样就关闭了WiFi网卡的自动电源管理，这样WiFi就不会自动进入节电模式而断开。

**Step.3**  再次输入： sudo iwconfig，可以看到 Power Management:off
