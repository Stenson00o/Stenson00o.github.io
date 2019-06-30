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
{% highlight python %}
from selenium import webdriver


driver = webdriver.Chrome('./chromedriver')
driver.get('https://baidu.com')
{% endhighlight %}
## 通过id name 查找元素
```
# driver.find_element_by_id('kw').send_keys("shei zhi dao")
driver.find_element_by_name('wd').send_keys("垃圾百度")
driver.find_element_by_id('su').click() # "按回车查找"

```
## 8 大 查找方式
```
find_element_by_id
find_element_by_name
find_element_by_xpath
find_element_by_link_text
find_element_by_partial_link_text
find_element_by_tag_name
find_element_by_class_name
find_element_by_css_selector
```

## 官方文档
https://selenium-python.readthedocs.io/locating-elements.html

