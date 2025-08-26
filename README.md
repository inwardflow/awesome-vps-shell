# Awesome VPS Shell

分享一些好用的 VPS 脚本

### ⚠ 免责声明

脚本审查过程中难免有疏漏，请自行甄别使用。

如有发现无法使用 / 有后门等情况，请在 issue 中及时提出，非常感谢！

## 目录



## Shell 脚本

### 建站类

* [宝塔面板](https://www.bt.cn/) - 服务器运维面板

```shell
if [ -f /usr/bin/curl ];then curl -sSO https://download.bt.cn/install/install_panel.sh;else wget -O install_panel.sh https://download.bt.cn/install/install_panel.sh;fi;bash install_panel.sh
```

* [mdserver-web](https://github.com/midoks/mdserver-web) - 魔改宝塔 Linux 服务面板

```shell
curl --insecure -fsSL https://raw.githubusercontent.com/midoks/mdserver-web/master/scripts/install.sh | bash
```

* [彩虹 Kangle 一键脚本](http://kangle.cccyun.cn/) 一键脚本 - 虚拟主机销售面板

```shell
yum -y install wget;wget http://kangle.cccyun.cn/start;sh start
```

### 装机类

* [Tools](https://github.com/leitbogioro/Tools) - Linux 一键网络重装脚本

```shell
#下载脚本
wget --no-check-certificate -qO InstallNET.sh 'https://raw.githubusercontent.com/leitbogioro/Tools/master/Linux_reinstall/InstallNET.sh' && chmod a+x InstallNET.sh

# 一键安装 Ubuntu 22.04
bash InstallNET.sh -ubuntu

### Default user name
# For Linux: root
# For Windows: Administrator

### Default password
#For Linux: LeitboGi0ro
#For Windows: Teddysun.com
```

### 网络类

* [TCPA](https://github.com/ivmm/TCPA) - 【网友备份】腾讯单边加速模块TCPA

```shell
wget https://gcore.jsdelivr.net/gh/tc-cdn/tcpa@latest/tcpa.sh && chmod +x tcpa.sh && sh tcpa.sh
#查看是否开启成功
lsmod | grep tcpa
```

* [TCP 加速脚本汇总](https://www.moerats.com/archives/387/) - BBR+BBR魔改+LotServer(锐速)一键脚本

```shell
#过程有2步，第1步安装相应的内核，第2步开启内核对应的加速
wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh
```
