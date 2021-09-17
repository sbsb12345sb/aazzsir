# AutoApiSecret-加密版

AutoApi系列：AutoApi、AutoApiSecret、AutoApiSR、AutoApiS

# 置顶 #

* 本项目是建立在[原教程 已失效](https://blog.432100.xyz/index.php/archives/50/)可以正确调用api的**假设**上的，核心是paran/黑幕大佬的py脚本。
* 本项目只是提供一个自动、免费、无需额外设备的脚本运行方式，换句话说，**借用github的电脑/服务器来干活**。（因为原教程需要服务器/超长时间运转的设备，大部分人都不具备，本项目应运而生）
* 本项目运行依赖**github action**服务，此功能github固有而**非私人提供**的服务器，且整个运行过程只涉及你与github。
* 请务必先阅读理解[原教程 已失效](https://blog.432100.xyz/index.php/archives/50/)的**原理说明、设计理念**。
* **不保证一定能续期！不保证一定能续期！不保证一定能续期**！或者说，**只是增大续订可能性**。过期前、后30天都可能续期！！！
* 若理解并接受上述说明，请接着操作；**若否，请点击浏览器右上角 X 。**

### 项目说明 ###

* 利用github action实现**定时自动调用api**，保持E5开发活跃。
* **免费，不需要额外设备/服务器**，部署完不用管啦。
* 加密版，隐藏应用id+机密，保护账号安全。

### 特别说明/Thanks ###

* 原教程博主-黑幕（酷安id-Paran）已失效：https://blog.432100.xyz/index.php/archives/50/   

* 普通版地址：已失效 https://github.com/wangziyingwen/AutoApi

* 加密版地址（推荐）：已失效 https://github.com/wangziyingwen/AutoApiSecret

* 模仿人为应用开发版（包含升级步骤）：已失效 https://github.com/wangziyingwen/AutoApiSR

* 超级版地址：已失效 https://github.com/wangziyingwen/AutoApiS

* **常见错误及解决办法/更新日志**：已失效 https://github.com/wangziyingwen/Autoapi-test

* 网页获取refresh_token小工具（不建议使用）：已失效 https://github.com/wangziyingwen/GetAutoApiToken

* 视频教程：（我操作很慢，自行倍速/快进）

  * 在线/下载地址：https://kino-onemanager.herokuapp.com/Video/AutoApi%E6%95%99%E7%A8%8B.mp4?preview

  * B站：https://www.bilibili.com/video/av95688306/

    ​      

### 区别 ###  已失效

   [普通版（弃用）] 已失效 (https://github.com/wangziyingwen/AutoApi)：密钥暴露，不在乎的话可以使用

   [加密版（推荐）]已失效 (https://github.com/wangziyingwen/AutoApiSecret)：应用id机密加密隐藏，提高安全性

   [模仿人为应用开发版（半弃用）]已失效 (https://github.com/wangziyingwen/AutoApiSR)：顾名思义，加密版的升级版。由于超级版兼容模拟版的功能，此版本处于一种尴尬位置。（当然也可以正常使用）

   [超级版（不建议）]已失效 (https://github.com/wangziyingwen/AutoApiS)：进一步升级版，增加自定义参数、模式。按目前情况，微软续订要求很低，暂时不需要使用此项目。

   **以上推荐/不建议等只是个人意见，请自行选择版本，可同时使用**。

--------------------------------------------------------------

### 步骤 ###

   *** **有错误/问题请看**:    

* 第一步，先大致浏览[原教程](https://blog.432100.xyz/index.php/archives/50/)，了解如何获取应用id、机密、refresh_token 3样东西，以方便接下来的操作。

* 第二步，登陆/新建github账号，回到本项目页面，点击右上角fork本项目的代码到你自己的账号，然后你账号下会出现一个一模一样的项目，接下来的操作均在你的这个项目下进行。（看不到图片/图裂请科学上网）

  ![image](https://user-images.githubusercontent.com/38358681/133702634-de33fef2-8324-418e-a939-eb3e9b6d6adf.png)

* 根据[原教程](https://blog.432100.xyz/index.php/archives/50/)获取应用id、机密、refresh_token（自己复制保存，注意区分id机密，别弄混了）

  然后在线编辑你项目里的1.txt，将整个refresh_token覆盖粘贴进去（里面是我的数据，先删掉或者覆盖掉）。（千万不要改1.py）

    > refresh_token位置如图下。复制refresh_token紧接着的双引号里的内容（红竖线框起来的），不要把双引号复制进去。复制进1.txt后，留意结尾不要留空格或者空行

    (![image](https://user-images.githubusercontent.com/38358681/133702570-3162f730-6461-4571-8a3a-1d6557a9d49d.png))

* 第三步，依次点击上栏Setting > Secrets > Add a new secret，新建两个secret如图：CONFIG_ID、CONFIG_KEY。

  内容分别如下: ( 把你的应用id改成你的应用id , 你的应用机密改成你的机密，单引号不要动 )
  ![image](https://user-images.githubusercontent.com/38358681/133703066-fe22bf8a-0c13-4af2-a0e8-3f92080a3eee.png)
![image](https://user-images.githubusercontent.com/38358681/133703073-139b2f69-1a15-4d10-9352-8cc64469bced.png)
![image](https://user-images.githubusercontent.com/38358681/133703085-d8fdfd44-9fb5-4639-a090-ec413fd16177.png)
![image](https://user-images.githubusercontent.com/38358681/133703188-992b5c21-66bf-4373-adfb-8acdcf5faa8f.png)


  CONFIG_ID

  ```shell
  id=r'你的应用id'
  ```
![image](https://user-images.githubusercontent.com/38358681/133703133-99d84f26-a292-4c82-ac41-3f48375dad03.png)

  CONFIG_KEY

  ```shell
  secret=r'你的应用机密'
  ```

  ![image](https://user-images.githubusercontent.com/38358681/133706592-0d9ee9aa-0ce2-404b-b678-f289ac362cbb.png)
  
  最终格式应该是类似这样的：

  ![image](https://user-images.githubusercontent.com/38358681/133706615-b1008dde-698e-4646-b896-5f0bbfed0871.png)

* 第四步，进入你的个人设置页面(右上角头像 Settings，不是仓库里的 Settings)，选择 Developer settings > Personal access tokens > Generate new token,

  ![image](https://user-images.githubusercontent.com/38358681/133706713-44a93b36-8322-46d3-aa16-1518cff4dbd9.png)
  ![image](https://user-images.githubusercontent.com/38358681/133706781-dd99ed88-9c32-47fa-913c-1028a77c6623.png)

  设置名字为GITHUB_TOKEN , 然后勾选 repo , admin:repo_hook , workflow 等选项，最后点击Generate token即可。

  ![image](https://user-images.githubusercontent.com/38358681/133706863-b8af17d2-cb9e-4d06-9ea3-d7c818162cf6.png)
  ![image](https://user-images.githubusercontent.com/38358681/133706893-3e783cd1-44e3-4f54-a892-a921e81839d2.png)

* 第五步，点击右上角星星/star立马调用一次，再点击上面的Action就能看到每次的运行日志，看看运行状况
![image](https://user-images.githubusercontent.com/38358681/133706934-8397a403-d2fd-4068-96ce-966421380716.png)

（必需点进去Test Api看下，api有没有调用到位，有没有出错。外面的Auto Api打勾只能说明运行是正常的，我们还需要确认10个api调用成功了，就像图里的一样。如果少了几个api，要么是注册应用的时候赋予api权限没弄好；要么是没登录激活onedrive，登录激活一下）

  ![image](https://user-images.githubusercontent.com/38358681/133706983-35467abc-9f1e-4a94-81c4-707d40ed34da.png)

* 第六步，没出错的话，就搞定啦！！再看看下面的定时次数要不要修改，不打算改就忽略。

  **然后第二天回来确认下是否自动运行了（ation里是否多出来几个）**,是的话就不用管了，完结。

  我设定的每3小时自动运行一次，每次调用3轮（点击右上角星星/star也可以立马调用一次），你们自行斟酌修改（我也不知道保持活跃要调用多少次、多久）：

  * 定时自动启动修改地方：（在.github/workflow/AutoApiSecret.yml文件里，自行百度cron定时任务格式，最短每5分钟一次）

  ![image](https://user-images.githubusercontent.com/38358681/133707061-0a3ba554-0981-4251-9be0-4d41cbb46f47.png)

  * 每次轮数修改地方：（在1.py最后面）

  ![image](https://user-images.githubusercontent.com/38358681/133707124-caa308b6-380c-4074-9348-b84a83d9d709.png)

------------------------------------------------------------

### 题外话 ###

> Api调用
>   你们可以自己去graph浏览器看一下，学着自己修改要调用什么api(最重要的是调用outlook、onedrive)
>   https://developer.microsoft.com/zh-CN/graph/graph-explorer/preview

### GithubAction介绍 ###

提供的虚拟环境：

· 2-core CPU
· 7 GB RAM 内存
· 14 GB SSD 硬盘空间

使用限制：

* 每个仓库只能同时支持20个 workflow 并行。
* 每小时可以调用1000次 GitHub API 。
* 每个 job 最多可以执行6个小时。
* 免费版的用户最大支持20个 job 并发执行，macOS 最大只支持5个。
* 私有仓库每月累计使用时间为2000分钟，超过后$ 0.008/分钟，公共仓库则无限制。

（我们这里用的公共仓库，按理，你们可以设定无限循环调用，然后6小时启动一次，保证24小时全天候调用）

### 最后 ###

  教程很直白了，应该都会弄吧！

  代码小白，多包涵！有问题/修改建议可以点击上方issues发布一下，或者PY给我:
  jing207@qq.com

  Q群：[56865213](https://jq.qq.com/?_wv=1027&k=jiLznNS2)  （项目相关讨论）

  tg群：[OneDrive E5](https://t.me/jing207_yzy)   （**非项目相关**讨论！**tg可能不会及时在线回答问题**，任何项目相关的问题或出错请进Q群/邮箱/issue）



  最后的最后，再次感谢黑幕/paran大佬

  ————wangziyingwen/酷安id-卷腿毛菌
