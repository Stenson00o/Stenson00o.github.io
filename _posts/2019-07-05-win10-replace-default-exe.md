---
layout: post
title:	win10修改默认程序
category: 技术
tags: win10
description: win10 用注册表修改默认程序
---
https://www.jianshu.com/p/7b5a7b304c2c?from=timeline&isappinstalled=0
+ 第一步：打开注册表。Win+R(或打开“运行”)，输入“regedit”，并按回车。
+ 第二步：在HKEY_CLASSES_ROOT里找到你想要更改的文件格式类型，如我的.hwt：

+ 第三步：继续在HKEY_CLASSES_ROOT文件夹下查找，找到hwt_auto_file文件夹（小技巧：你可以直接在上面的资源路径输入框里输入，并按回车），并且打开shell\open\command
+ 第四步：修改注册表。右键点击“command”文件夹，选择导出。（原因是数据这一项无法直接修改，要先导出