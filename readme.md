# [突破天翼云盘下载限制](https://github.com/oneNorth7/Cloud189_popper)

<img src="https://gitee.com/oneNorth7/pics/raw/master/picgo/icon.jpeg" alt="天翼云盘" style="zoom: 50%;" />

## 原创声明

​    该脚本是受已失效的 [免登录下载天翼云盘分享文件](https://greasyfork.org/zh-CN/scripts/401709-免登录下载天翼云盘分享文件) 脚本的启发，突破原理是通过**自行阅读分析**官网代码获得的，目前好像没看到有人分享类似的脚本；虽然无法实现免登录下载，但突破下载限制也是另一种收获，毕竟我的云盘容量不是很大不支持太多的转存○(＾皿＾)っHiahia....。

## 痛点问题

<img src="https://gitee.com/oneNorth7/pics/raw/master/picgo/下载限制.jpg" alt="下载限制" style="zoom: 80%;" />

​    天翼云盘**不限下载速度**的特色让人心生向往，但网页版**不支持文件夹、多文件、大于50M的文件**下载，需要**转存**后通过**客户端**下载的限制让很多人望而却步，本人在找寻免登录下载的过程中发现了突破这一限制的方法，此脚本也应运而生。

## 功能描述

- [x] **突破50M文件大小**的下载限制

- [x] **突破多文件**的下载限制

- [x] **突破文件夹**的下载限制

## 使用说明

**必须登录云盘网页版！！！**

**必须登录云盘网页版！！！**

**必须登录云盘网页版！！！**

​    重要的事情说三遍，注册云盘帐号只是分分钟的事情（**移动、电信、联通手机号**均可）。

​    上面也说到一开始的想法是想找寻免登录下载的方法，可惜官方现在加上了登录Cookie的验证，这条路已经被封死了。**另外本人郑重声明：本脚本不存在任何盗取个人Cookie的行为，欢迎大家监督**。

* 脚本延迟加载后，下载按钮会变成绿色的**直接下载**，转存按钮旁“烦人”的提示信息会被隐藏，**多文件页面**点选文件后出现绿色的**直接下载**按钮（下载文件一路绿灯，畅通无阻2333）；
* **多文件分享页面**的文件右侧的**小下载按钮**支持**直接下载**该文件（文件夹只有转存按钮），个人主页文件夹或文件右侧的**小下载按钮**支持**直接下载**该文件或文件夹；
* 点选文件后若没有出现绿色的**直接下载**按钮，可以尝试点选其他文件或取消或再选中；若千点万点还不出来也可以点击脚本的菜单项【**突破限制**】或者刷新页面。
* 个人主页自动生成的文件夹（如*同步盘，我的图片*等等）的**直接下载**按钮是**禁用**状态的，不支持下载该文件夹，可进入目录下载
* 目前存在的小bug可参考下面的临时解决方案

## 使用建议

* 强烈建议**单文件下载**，官方返回的**单文件下载链接**支持IDM**多线程**和**续传**下载，速度奇快，文件名也正确；
* 打包下载返回的压缩包名固定为”【打包下载】天翼云盘.zip“，并且该链接不支持IDM多线程和续传下载，速度也降下来了（演示图片里下载文件夹第一次就失败了，第二次才下载成功，打开后发现文件下载不全，只下载了顶级文件夹里的文件，顶级的文件没有在里面；之后下载了层级不深的文件夹就全在压缩包里了，这打包的下载链接还有待深入研究 emmm）
* 有大批量下载文件或文件夹需求的还是建议选择官方客户端下载；

## 功能演示

* 超过50M的单文件分享页面
![单文件突破大小限制](https://gitee.com/oneNorth7/pics/raw/master/picgo/单文件突破大小限制.gif)

* 多文件分享页面
![多文件打包下载](https://gitee.com/oneNorth7/pics/raw/master/picgo/多文件打包下载.gif)

* 个人主页
![个人主页打包下载](https://gitee.com/oneNorth7/pics/raw/master/picgo/个人主页打包下载.gif)

* 目录下单文件下载（点击文件右侧的小下载按钮）
![目录下单文件下载](https://gitee.com/oneNorth7/pics/raw/master/picgo/目录下单文件下载.gif)

## 临时解决方案

* 个人主页下载时，*全部文件* 下的任何文件夹或文件夹下的任意文件被**直接下载**了，重新进入该文件夹时目录导航条中的 *返回上一级* 和 *全部文件* 会消失不见，这时可以直接点击左侧的 *全部文件* 返回，之后这个bug会暂时消失，但再次**直接下载**还是会出现以上问题；这个bug只影响浏览文件，不影响文件下载。

具体操作可参考以下动图：
![个人主页下载小bug](https://gitee.com/oneNorth7/pics/raw/master/picgo/个人主页下载小bug.gif)

* 点击**全选**按钮**不能**直接下载，提供以下临时解决方案：

1. **多文件分享页面**可以全选后点击任意文件前的选框，再点该文件选框（注意**不是**全选按钮）进行全选，最后再点**直接下载**，第二步误点全选按钮**请重新操作**；有上级目录的直接返回上一级下载单个文件夹；
2. **个人主页**直接返回上一级目录下载单一文件夹；不支持返回上级目录（系统生成目录）的可先下载单一文件，成功弹出下载界面后**取消下载**，之后参考多文件分享页面的第一个解决方法

## 关注赞赏

**关注我，不迷路**~~

<img src="https://gitee.com/oneNorth7/pics/raw/master/picgo/oneNorth7.png" style="zoom: 67%;" />

**原创不易，您的支持是我坚持创作的动力**~~

<img src="https://gitee.com/oneNorth7/pics/raw/master/picgo/reward_qrcode.png" style="zoom: 33%;" />

