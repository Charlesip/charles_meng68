# 1、序

​	文章编写时间是2021/11/20，对应的最新Cemu的版本为*`Cemu 1.25.6 (2021-10-15)`*，这次折腾的主要原因是听说Cemu大幅提升了效率，于是想在PC上体验一下4K60FPS的塞尔达。整个文章记录的是**纯净版**的安装过程，包括游戏和UI的汉化选择的都是基于Nintendo的官方汉化，所以对网络条件有一定的科学的要求。

​	新版的Cemu我甚至没修改Nvidia的控制面板，三缓之类的都没开、显卡运行在节能模式下（GTX1070）阴影设为300%（Cemu官方推荐的最大值），依然可以实现稳定的4K40FPS，`注：神庙内4k可以跑到60FPS，1080p的话可以跑到144FPS，但是高刷开启之后会有些小问题，我就没开了：比如用摇杆选择东西的时候光标跑太快刹不住车。60对我来说已经很好`可见效率较之前还是有很大提升的（现在还支持光追滤镜了，但是我还没折腾）

# 2、安装Cemu

## 	2.1Cemu的下载与安装

**[Cemu官网](https://cemu.info/)**

## 	2.2Cemu的调试

# 3、下载游戏

下载游戏使用**[FunKiiU](https://github.com/llakssz/FunKiiU)**

```English
https://cemu.info/python FunKiiU.py -title 【**Title ID**】 -key 【**Title key**】
```

可以使用[**Wii U Title Key**](https://utik.91wii.com/)这个网站搜索游戏名称找到Title ID以及Title key

# 4、安装游戏

安装游戏首先要使用**[CDecrypt](https://github.com/VitaSmith/cdecrypt)**进行**格式转换**

将CDecrypt解压到任意文件夹，将刚刚下载好的文件夹拖到cdecrypt.exe上，会开始自动转换

# 5、优化性能
