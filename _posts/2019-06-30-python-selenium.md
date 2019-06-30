---
layout: post
title:	python selenium 驱动浏览器
category: 技术
tags: python
description: python selenium 让浏览器通过id name  css-selector 操作浏览器
---

## 安装selenium
```
python3 -m pip install selenium
```
## 下载驱动器driver
driver 下载地址 ：[driver](https://sites.google.com/a/chromium.org/chromedriver/)

##  正确打开姿势
```
from selenium import webdriver


driver = webdriver.Chrome('./chromedriver')
driver.get('https://baidu.com')
```
