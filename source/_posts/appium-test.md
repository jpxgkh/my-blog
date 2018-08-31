---
title: Appium 自动化测试初体验
date: 2018年8月31日 17:43:16
tags: 自动化测试
---

#### 一、所需前置环境

jdk
安卓sdk（这个可以跟客户端同事要一下，自己安装的话速度很慢）
python 2.7（3.7也可以）
appium-desktop（最新版即可，不要下appium-server，那个已经停止更新维护了）
node


#### 二、配置开发环境

安卓环境配置
安装jdk并配置完环境变量。
安装android并配置环境变量（可请教安卓同事），这里要注意的是，安卓的文件夹下有platform-tools和tools两个文件夹，这两个文件夹也要配置到环境变量中。
验证adb，将手机连接电脑，cmd中输入adb，若有很长一串英文说明，则说明安装成功，若提示“不是内部或外部命令”，则说明安装失败。
连接手机到电脑上，在cmd中输入adb services，如下图所示情况说明安装完成。

在安装时记得安装build-tools，安装完在复制对应的路径添加到环境变量中，成功后可使用aapt，aapt用于查看apk包的包名等之后写脚本会用到的信息，验证是否安装和配置成功的方法同adb。


python环境配置
官网下载安装包，傻瓜式一键安装，最好不要装在c盘吧（这难道不是常识吗）。

配置环境变量，将（盘符）:\python和（盘符）:\python\Scripts，添加到环境变量path下。
在cmd中输入python，若提示“不是内部或外部命令。。。”则说明安装失败。
安装Appium-Python-Client，打开cmd，输入“pip install Appium-Python-Client”。
appium
安装appium-desktop，链接https://github.com/appium/appium-desktop/releases。
安装完打开，点击start server即可（其他两个选项卡和用途参考更目录发的教程）。

最后，在cmd中输入appium-doctor，若提示“不是内部或外部命令。。。”则说明安装失败。
