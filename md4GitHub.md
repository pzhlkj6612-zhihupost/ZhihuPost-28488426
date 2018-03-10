![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-8f57d9b5ad89d66f66d20f6b9e7afb32.jpg)

禁止转载。

禁止转载是指“禁止转载本文内容”，可以通过超链接的方式分享本文。

<br/>

本文章内容由我的这篇文章转移而来：

[https://github.com/pzhlkj6612/ZhihuPost-23656301](https://github.com/pzhlkj6612/ZhihuPost-23656301)

本文章也存在于GitHub仓库：

[https://github.com/pzhlkj6612/ZhihuPost-28488426](https://github.com/pzhlkj6612/ZhihuPost-28488426)

<br/>

注意：

* 本文可能不会持续更新；
* 本文仅适用于Windows用户；
* 以下内容有难度。

----

# 目录

* 无法定位程序输入点RemoveDLLDirectory
* 鉴定时间超出
* \* 更新助手出现一个错误
* 丢失MSVC****.dll
* 丢失libmmd.dll
* Missing serial number
* “除了主程序，其他都打得开”
* \* “启动界面一闪而过”
* 脚注
* 其他

标\*的表示该部分内容未经过充分测试，请谨慎参考。

----

# 无法定位程序输入点RemoveDLLDirectory

安装Cinema4D R18时出错：

>MAXON-Inst.exe – 无法找到入口    
>(X) 无法定位程序输入点 RemoveDllDirectory于动态链接库KERNEL32.dll上。

![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-8ebd181febc4464cbfb9a37ceafc3fd2.jpg)

解决方法：

* 《[Cinema4D R18安装程序KERNEL32.dll报错解决方法](https://github.com/pzhlkj6612/ZhihuPost-23656301)》

<br/>

# 鉴定时间超出

安装或更新Cinema4D R18时出错：

> MAXON 在线更新器    
> 鉴定时间超出,更新不能开始并已经取消.

![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-958c5afeb9cc2bcc936601a27ce22ad5.jpg)

解决方法：

* 单击“Retry”，注意UAC提示（在这里，你需要点`Yes`）：

![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-de95d6fc28359f75ad955f9603798c2a.jpg)

<br/>

# 更新助手出现一个错误

安装Cinema4D R18时出错：

> MAXON 在线更新器    
> (X) 更新助手出现一个错误, line 420

![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-52a23d59f3e277877eec7ca8c7dc5a1a.jpg)

解决方法：

* 不要在网络驱动器中运行安装程序。

<br/>

# 丢失MSVC****.dll

运行Cinema4D R18时出错，类似于：

> CINEMA 4D.exe - 系统错误    
> (X) 无法启动此程序，因为计算机中丢失MSVCP120.dll。尝试重新安装该程序以解决此问题。

![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-1f80c197b434c9492934643e218ba295.jpg)

解决方法：

挂载或解压Cinema4D R18的镜像文件[0]，找到路径`.\bin\data\redist`下的`vcredist_x64_2013.exe`文件[1]，双击以安装。

<br/>

有可能会出现以下情况，但最终Cinema4D能够运行：

> CINEMA 4D.exe - 系统错误    
> (X) 无法启动此程序，因为计算机中丢失MSVCR110.dll。尝试重新安装该程序以解决此问题。

![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-cb65780fef410ba0128374e2a5148267.jpg)

不要忽略这个问题！

解决方法：

* 挂载或解压Cinema4D R18的镜像文件[0]，找到路径“.\bin\data\redist”下的“vcredist_x64_2012.exe”文件[2]，双击以安装。

<br/>

# 丢失libmmd.dll

运行Cinema4D R18时出错：

> CINEMA 4D.exe – 系统错误    
> (X) 无法启动此程序，因为计算机中丢失libmmd.dll。尝试重新安装该程序以解决此问题。

![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-deca1c73ddff6096f2bb5caf8be85c79.jpg)

解决方法：

* 挂载或解压Cinema4D R18的镜像文件[0]，找到路径`.\bin\data\redist`下的`w_ccompxe_redist_intel64_2015.2.179.msi`文件[3]，双击以安装。
安装程序会添加相关的环境变量，并在这个目录释放`libmmd.dll`：

```
C:\Program Files (x86)\Common Files\Intel\Shared Libraries\redist\intel64\compiler
```

<br/>

例外情况：

（4楼）http://tieba.baidu.com/p/3861775818?pid=70743381356#70743381356

<br/>

# Missing serial number

运行“绿色版”Cinema4D R18时出错：

> CINEMA 4D    
> Missing serial number for 'CINEMA 4D'!

![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-3103b8982b359757cd5b71855ca0a108.jpg)

临时解决方法：

* 单击“OK”，在弹出的“Registration”窗口中进行注册；

可能会造成的问题：

* 该Cinema 4D R18未经过正确的安装过程，可能会有潜在的问题，在将来暴露出来。

长期解决方法：

* 清理当前的Cinema 4D R18，并学习使用Cinema4D R18的镜像文件进行正确的软件安装。

# “除了主程序，其他都打得开”

运行Cinema4D R18主程序时没有反应，进程“CINEMA 4D.exe”只出现在后台，没有界面；

运行Team Render Client/Team Render Server正常（Commandline不确定）；

现象参考：

* （视频中前13秒）http://www.bilibili.com/video/av7450404/

临时解决方法：

* 进入Cinema4D的程序目录（Cinema4D被安装到的位置，参考“‘启动界面一闪而过’”部分“解决方法”的附图），找到路径`.\resource\libs\win64`下的`mesa`文件夹，将其改名或移出原位置（不要直接删掉），再运行Cinema4D R18主程序。

![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-e5187b4d6c3a4fd4a7b65163a305af5a.jpg)

可能会造成的问题：

![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-286f9c0ca8c418937f18891d0948467a.jpg)

长期解决方法：

* 从Cinema4D官网上下载R18的更新：https://www.maxon.net/en-us/support/downloads/#c25195

（R18.057更新的相关信息：http://tieba.baidu.com/p/5217877841）

![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-bc0266a0413e88d96ac9ff1047286c68.jpg)

运行Team Render Client或Team Render Server，菜单栏-`Help`-`Manual Installation`-`Continue`-`✔ I have...`-`Continue`-`✔ Automatically restart...&✔ Delete downloaded...`-`Continue`，注意UAC提示：

![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-810e2ea598e0ffb68f387ecead1ec51b.jpg)

* 照此操作，路径`.\resource\libs\win64\mesa`下的`opengl32.dll`文件也会被更新。

相关知识：

* [Mesa\(OpenGL\)](https://en.wikipedia.org/wiki/Mesa_(computer_graphics))

来源：

* [https://www.maxon.net/en/products/infosites/system-requirements/](https://www.maxon.net/en/products/infosites/system-requirements/)
* [https://www.c4dcafe.com/ipb/forums/topic/97279-c4d-doesnt-work-on-ryzen/](https://www.c4dcafe.com/ipb/forums/topic/97279-c4d-doesnt-work-on-ryzen/)
* [https://community.amd.com/thread/213128](https://community.amd.com/thread/213128)
* （129楼）[http://tieba.baidu.com/p/4859025376?pid=105008275284#105008275284](http://tieba.baidu.com/p/4859025376?pid=105008275284#105008275284)
* （26楼）[http://tieba.baidu.com/p/4861947833?pid=105188842741#105188842741](http://tieba.baidu.com/p/4861947833?pid=105188842741#105188842741)

<br/>

# “启动界面一闪而过”

运行Cinema4D R18主程序时，启动界面出现“Initializing Plugins...”后消失，进程`CINEMA 4D.exe`也随之消失；

运行Commandline正常；

运行Team Render Client/Team Render Server时，启动界面卡在“Initializing Plugins...”；

![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-e1a2f1238e44e93ae74ab6bc13448659.jpg)

解决方法：

* 使用默认的安装路径（`C:\Program Files\MAXON\CINEMA 4D R18`），或者使用其它的全英文路径。

![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-b3b32b2a29b7813fae0aeb84f7bae7c3.jpg)

----

# 脚注

**[0] 挂载或解压Cinema4D R18的镜像文件**

* 对于Windows 8/8.1/10：

右键单击Cinema4D R18的镜像文件，单击`挂载`；

![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-d7cf159a73a8758b0a6544dc41778528.jpg)

或执行以下命令（`.\X.iso`是Cinema4D R18的镜像文件的绝对路径）；

``` Powershell
explorer ".\X.iso"
```

![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-469aac419a1bc6d3a90bdcc87104b049.jpg)

* 对于Windows 7：

使用Daemon Tools Lite等软件挂载镜像；

![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-24791609880005bbbc124e648021418d.jpg)

或使用WinRAR等软件解压镜像文件：

![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-319e4a801b2a2892598d884f28ea30b7.jpg)

<br/>

**[1] vcredist_x64_2013.exe**

> Size: 6.86 MB (7,194,312 bytes)    
> MD5: 96B61B8E069832E6B809F24EA74567BA    
> SHA-1: 8BF41BA9EEF02D30635A10433817DBB6886DA5A2

**[2] vcredist_x64_2012.exe**

> Size: 6.85 MB (7,186,992 bytes)    
> MD5: 3C03562B5AF9ED347614053D459D7778    
> SHA-1: 1A5D93DDDBC431AB27B1DA711CD3370891542797

**[3] w_ccompxe_redist_intel64_2015.2.179.msi**

> Size: 9.40 MB (9,863,168 bytes)    
> MD5: 484BE36C04E189B5A0F66C40B1BA08F8    
> SHA-1: 1F64EC94CD6A936729CB8A64994ECFB26829398B

----

# 其他

* Cinema4D、Premiere Pro入门推荐doyoudo：[http://www.doyoudo.com/](http://www.doyoudo.com/)
* 能集成到Explorer shell里的Hashtab，个人免费：[http://implbits.com/products/hashtab/](http://implbits.com/products/hashtab/)

<br/>

**强烈建议你使用当前最新版本的CINEMA 4D以及最新版本的正式版操作系统；**

**不懂再问。**

----

待更新的：

* 0xc000007b

> CINEMA 4D.exe - 应用程序错误    
> (X)应用程序无法正常启动(0xc000007b)。请单击“确定”关闭应用程序。

![](https://raw.githubusercontent.com/pzhlkj6612/ZhihuPost-28488426/master/pic_zhimg_com/v2-82ed43868b3bb7565dc3596b8199ae53.jpg)

来源：[https://stackoverflow.com/questions/44635135/cinema4d-the-application-was-unable-to-start-correctly-0xc000007b](https://stackoverflow.com/questions/44635135/cinema4d-the-application-was-unable-to-start-correctly-0xc000007b)

猜测：Visual C++ Redistributable Package

----

[@黄子博](http://www.zhihu.com/people/17084edb97de7106c56c624e23c073aa) 先导、全程协助，

贴吧用户[@hry31580](http://tieba.baidu.com/home/main/?un=hry31580) （c4d吧小吧主）的主题帖的指引，

<br/>

[@墨子 2200MHz](http://www.zhihu.com/people/faf758840a7dfc528c4f620cdddf1460) 测试、整理。

<br/>

原文章发布于：2016.11.14

原文章修改于：2017.08.16

<br/>

修改于：22:21 2018/01/03

禁止转载。