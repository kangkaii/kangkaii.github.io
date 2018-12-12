## 上网配置

- 分成2个步骤
1. 下载客户端并安装
2. 新增配置，并选择需要的配置。


---


### pc端

- 下载并安装shadowsocks 客户端
- windows [下载链接](https://github.com/shadowsocks/shadowsocks-windows/releases/download/4.1.2/Shadowsocks-4.1.2.zip)
- 安装，解压到需要安装的文件夹
- 比如想安装到D盘ss文件夹下。建议d盘内新建文件夹ss后，使用解压工具，解压到ss文件夹即可。如下图

![image](https://upload-images.jianshu.io/upload_images/5625942-c3bc3a41ef115625.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
- 双击运行此程序即可。注：会在ss文件夹下生成其余配置文件，无需处理。
- 自动弹出下图界面，为**编辑服务器的窗口**，桌面右下角也会出现小飞机图标，至此，客户端安装结束。

![image](https://upload-images.jianshu.io/upload_images/5625942-72973ac0329e4adf.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![image](https://upload-images.jianshu.io/upload_images/5625942-06e7d169e9f68d18.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 接下来就是配置服务器
1. 编辑服务器的窗口配置，需要填写服务器地址，端口号等。比较麻烦，暂不介绍。
2. **推荐采用二维码扫描或者链接导入！**

- **使用二维码导入**
- 打开二维码，置于屏幕中心。找到运行中的小飞机，右击展示菜单，选择**服务器**,再次展开菜单后，选择最后倒数第二项，只要屏幕中心有二维码就可以。



- **复制url导入**
- 复制url，使其存在于剪切板中。找到运行中的小飞机，右击展示菜单，选择**服务器**,再次展开菜单后，选择最后一项，从剪切板导入url（只要你复制了url即可）

![image](https://upload-images.jianshu.io/upload_images/5625942-51b3a6ae7deed399.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

3. 上述两种方式成功后都会弹出编辑服务器窗口，关掉即可。

4. 配置已经ok。检测是否成功网址：`google.com`

**发现打不开？自查2点：**
1. 找到运行中的小飞机，右击展示菜单，第一项，一定要勾选启用系统代理。

![image](https://upload-images.jianshu.io/upload_images/5625942-d1a4215573a85868.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
2. 找到运行中的小飞机，右击展示菜单，选择**服务器**,再次展开菜单后，按照下图对号方式选择，不要选择未配置的服务器（这也是切换服务器的方式，可能存在某个服务器哪天突然挂掉，需要手动切换）

![image](https://upload-images.jianshu.io/upload_images/5625942-cf1941b6e2a4cd81.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


---

## 安卓
- 移动端配置要比pc端轻松很多很多

- [下载链接1](https://github.com/shadowsocks/shadowsocks-android/releases/download/v4.6.2/shadowsocks--universal-4.6.2.apk)

- [下载链接2](https://github.com/shadowsocks/shadowsocks-android/releases/download/v4.6.2/shadowsocks-arm64-v8a-4.6.2.apk)

- 建议使用uc等浏览器打开下载链接，然后正常安装即可。
- 软件初始页面如下（包含一些简单介绍）

![image](https://upload-images.jianshu.io/upload_images/5625942-a947b6ebcd3b7e9e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 使用新增配置按钮，新增配置

![image](https://upload-images.jianshu.io/upload_images/5625942-024d13c7ea48cd30.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 还是使用扫描二维码导入或者从剪切板导入，不建议手动配置。
- 完成后，可以看到页面有配置好的服务器待选择。
- 选择合适服务器后，打开开关，手机上方信号栏，出现`v-p-n`图标后，尝试打开`google.com`
- 如果不能打开，再新增一个服务器试试，新增完成后，记得切换到刚新增的服务器。

---
## ios 
**目前正在寻找合适的软件，AppStore中国区能用的基本都下架了。明天更新下**

---
### url 与 二维码

来源：https://free-ss.site/
```
ss://cmM0LW1kNTpRTEJrVVpAMTkzLjM4LjEzNy44NDo1NTM1NA==

ss://YWVzLTI1Ni1jZmI6c3N4LnJlLTUxMjg5NTE4QDY4LjE4My4yMjQuMjM2OjE5ODQ2

ss://YWVzLTI1Ni1jZmI6c3N4LnJlLTY2NDI5NTM2QDE1OS44OS4xMzguMTIwOjE5OTQ5

ss://cmM0LW1kNTo5dWhpN2Z0aUAxNTQuODUuMzYuMjE3OjEwNTU=

ss://YWVzLTI1Ni1jZmI6dGdkYWlsaUAxOTQuMTQ3LjM1Ljk1OjIzMzM=

ss://cmM0LW1kNTpodHRwOi8vdC5jbi9SRDBEN3N4QDQ1LjYyLjIzNS40MDo0NDM=

ss://YWVzLTI1Ni1jZmI6c3M4LnBtLTE0NzMxNzQwQDEwNy4xNzAuMjMyLjE2ODoxNDAxMQ==

ss://YWVzLTI1Ni1jZmI6aXN4Lnl0LTM3Mzc4NzcxQDIwNi4xODkuMTUzLjI2OjEyNzE4

ss://YWVzLTI1Ni1jZmI6aXN4Lnl0LTY3MjY4MzY1QDEwNC4xMzEuMTM0LjIxNToxODc1MQ==

ss://YWVzLTI1Ni1jZmI6aXN4Lnl0LTc1NTUwNzY3QDE5Mi4yNDEuMjA1LjE2MzoxOTI0Nw==

ss://YWVzLTI1Ni1nY206d0dRNHZBN0RANDYuMTcuNDMuMjoyMjEwMA==

ss://YWVzLTI1Ni1jZmI6c3M4LnBtLTQ2MTM4NzQxQDE2Ny45OS43Ny4xNzg6MTQzODg=

ss://Y2hhY2hhMjA6bGVuZ3l1ZTMxMkAyNjA0OmE4ODA6MjpkMDo6MjAzOToyMDAxOjY3ODk=

ss://YWVzLTI1Ni1jZmI6aWxvdmV0Z0A1NC4yNDguMjA3LjEzMzo5MDA5

ss://YWVzLTI1Ni1jZmI6c3N4LnJlLTY2NTUzMTU0QDEwNC4xMzEuMTM2LjE1NToxMzA4OA==

ss://YWVzLTEyOC1nY206Y2ZhbmNoZW5ANDUuNjIuMTIxLjk3OjM5MTM0
```
![image.png](https://upload-images.jianshu.io/upload_images/5625942-d89241524c1f7887.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![image.png](https://upload-images.jianshu.io/upload_images/5625942-6af9fbd83ef5811a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![image.png](https://upload-images.jianshu.io/upload_images/5625942-3f1a35dcb7ec9bbe.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![image.png](https://upload-images.jianshu.io/upload_images/5625942-09391a28a7a68d4b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![image.png](https://upload-images.jianshu.io/upload_images/5625942-294b4abfa4cca870.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![image.png](https://upload-images.jianshu.io/upload_images/5625942-fbc0c6c6c811d39f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![image.png](https://upload-images.jianshu.io/upload_images/5625942-58fdccf7feb83995.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![image.png](https://upload-images.jianshu.io/upload_images/5625942-31f951c501b84a76.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![image.png](https://upload-images.jianshu.io/upload_images/5625942-e5ace5e2b5b1c302.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![image.png](https://upload-images.jianshu.io/upload_images/5625942-c3d3e8f371f3ac22.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![image.png](https://upload-images.jianshu.io/upload_images/5625942-e7282608262ef097.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![image.png](https://upload-images.jianshu.io/upload_images/5625942-65717467256aa9b6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![image.png](https://upload-images.jianshu.io/upload_images/5625942-3e7974de1b373635.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
