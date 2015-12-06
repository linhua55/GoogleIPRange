# GoogleIPRange

整合自[gogotester](https://github.com/azzvx/gogotester)、[checkgoogleip](https://github.com/moonshawdo/checkgoogleip)、[gscan](https://github.com/yinqiwen/gscan)、[XX-Net](https://github.com/XX-net/XX-Net)、[XX-Mini](https://github.com/xyuanmu/XX-Mini)、[Google-IP-Range](https://github.com/Rongronggg9/Google-IP-Range)及自己搜寻的IP库，特别感谢各位开发者。

# 文件说明

[googleip.txt](https://raw.githubusercontent.com/CNMan/GoogleIPRange/master/googleip.txt):在国外VPS上验证后含google证书的IP段

[nogoogleip.txt](https://raw.githubusercontent.com/CNMan/GoogleIPRange/master/nogoogleip.txt):在国外VPS上验证后不含可用google证书的IP段，随时间可能会有部分变动

##建议使用[CheckGoogleIP](https://github.com/moonshawdo/checkgoogleip/)，快速且结果精准。

1、下载[GoAgent](https://github.com/phuslu/goagent/archive/985cbd55e232833a859e7f2940b54f7dcb6cdb14.zip)并解压

2、下载[CheckGoogleIP](https://github.com/moonshawdo/checkgoogleip/archive/master.zip)，解压其中的checkip.bat和checkip.py到goagent的local文件夹

3、下载[googleip.txt](https://raw.githubusercontent.com/CNMan/GoogleIPRange/master/googleip.txt)到goagent的local文件夹

4、运行checkip.bat，等待运行结束生成ip.txt，其中的IP即为筛选出的可用Google IP。

首次使用CheckGoogleIP时[checkip.py](https://github.com/moonshawdo/checkgoogleip/blob/master/checkip.py) 中参数修改建议:

* 第66行:g_maxhandleipcnt = 50 修改为9999999，否则扫到50个可用IP就自动结束了。

其他参数无需改动，ip_tmperror.txt、ip_tmpno.txt请保留，下次扫描会自动略过其中的IP，加快扫描速度。

更多说明见：[https://github.com/moonshawdo/checkgoogleip/blob/master/README.md](https://github.com/moonshawdo/checkgoogleip/blob/master/README.md)

##批量PING可用[PingInfoView](http://www.nirsoft.net/utils/multiple_ping_tool.html)。

##需要补充请直接提交[Pull Request](https://github.com/CNMan/GoogleIPRange/pulls)。

注意剔除以下保留IP地址：

```python
0.0.0.0/8
10.0.0.0/8
100.64.0.0/10
127.0.0.0/8
169.254.0.0/16
172.16.0.0/12
192.0.0.0/24
192.0.2.0/24
192.88.99.0/24
192.168.0.0/16
198.18.0.0/15
198.51.100.0/24
203.0.113.0/24
224.0.0.0/4
240.0.0.0/4
255.255.255.255/32
```

### [VPS推荐](https://cnlic.com/share/vps.html)
### [VPS测速](https://cnlic.com/share/speedtest.html)
### [Debian/Ubuntu VPS 安装 shadowsocks](https://cnlic.com/?p=353)
### [Debian/Ubuntu VPS 安装 PPTP VPN](https://cnlic.com/?p=354)
### [Debian/Ubuntu VPS 安装 Cisco AnyConnect VPN](https://cnlic.com/?p=360)
