终端登录到服务器，在终端（黑框框）里输入如下命令：

bash <(curl -sL https://raw.githubusercontent.com/wwb7700/55/master/centos_install_ss.sh)
按回车键，屏幕出现“请设置SS的密码（不输入则随机生成）” 的提示，按照提示设置密码（SS的密码，例如1234abcd，不是服务器后台的密码）、端口（SS的端口，例如2345，不能是22和80）并选择加密方式。

接下来屏幕上开始疯狂出现一堆你看得懂也可能看不懂的东西，如果安装过程卡住，请耐心等待几分钟；期间网络断开（windows上表现为黑框框中或者顶部标题出现disconnected字样，mac表现为终端出现“closed by remote host”或”broken pipe”），请重新连接后再次执行命令。脚本执行成功后会输出SS配置

到此服务端配置完毕，服务器可能会自动重启，windows终端出现“disconnected”，mac出现“closed by remote host”说明服务器重启了，如果没提示重启则不需要。

SS一键脚本做了如下事情：

更新系统到最新版
安装bbr加速模块
安装SS并设置开机启动


其他
1. 查看ss程序运行状态/配置参数：bash <(curl -sL https://raw.githubusercontent.com/wwb7700/55/master/centos_install_ss.sh) info

2. SS管理命令：启动：systemctl start shadowsocks-libev；停止：systemctl stop shadowsocks-libev；重启：systemctl restart shadowsocks-libev

3.  更改密码、端口、加密方式最简单方法：重新运行一次安装脚本

4. 更新SS到最新版：重新运行一键脚本

5. 卸载SS：bash <(curl -sL https://raw.githubusercontent.com/wwb7700/55/master/centos_install_ss.sh) uninstall
