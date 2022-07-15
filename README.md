# Padavan-build说明

现在不需要新建Release了，已经更改了脚本，直接fork，修改好之后，点击右上角的 Star 星星按钮即可开始自动编译（自己点击才会编译）。

以下是自编译步骤：作者：zhgw1997 https://www.bilibili.com/read/cv10661068/ 出处：bilibili

第一步：fork两个代码

https://github.com/chongshengB/Padavan-build

https://github.com/hanwckf/rt-n56u

第二部：修改Padavan-build的脚本

进入Padavan-build仓库的workflow文件夹里，修改build-padavan.yml
修改clone的仓库地址和路由器型号，路由器型号名称在rt-n56u仓库的/trunk/config/templates中可以找到。 
删除所有插件配置，所有夹在#######中间的关于自定义插件和功能的代码都删掉；
修改完直接commit即可；

第三步：修改固件配置

进入rt-n56u仓库中
定位到/trunk/config/templates，打开自己的路由器型号配置文件，进行修改
Y为生效，N为不生效，注释掉，也不生效；
原则上来说所有配置都可以不启用，这样就能得到一个相对纯净的固件，减少路由器运行时的内存占用。有些配置是看机型启用的，比如USB设置，没有USB接口的路由器启用配置之后也无法生效。

第四步：修改路由器配置文件

定位到/trunk/user/shared/defaults.h文件，进行修改
在这个文件中可以自定义管理员名称及密码、默认LAN地址、默认WiFi名称及密码、默认NTP服务器等设置。 
修改完之后commit即可

最后一步：

回到Padavan-build，点击右上角的 Star 星星按钮即可开始自动编译（自己点击才会编译）。

其他参照学习：https://www.right.com.cn/FORUM/thread-8104907-1-1.html
