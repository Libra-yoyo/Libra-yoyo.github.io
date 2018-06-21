---
layout: post
title: 微信小程序的设置底部导航栏
date: 2016-06-02 11:15:06 
tag: 工具
---

微信小程序设置底部导航栏目方法														 
微信小程序底部想要有一个漂亮的导航栏目，不知道怎么制作，于是百度找到了本篇文章，分享给大家。

好了 小程序的头部标题 设置好了，我们来说说底部导航栏是如何实现的。

我们先来看个效果图
这里，我们添加了三个导航图标，因为我们有三个页面，微信小程序最多能加5个。

那他们是怎么出现怎么着色的呢？两步就搞定！

1. 图标准备阿里图标库  http://www.iconfont.cn/collections/show/29

我们进入该网站，鼠标滑到一个喜欢的图标上面  点击下方的 下载按钮

在弹出框中 选择了 俩个不同颜色的 图标  选择64px大小即可，我选择的是png  然后下载下来 起上别名 

将上述起好名字的图标 保存到 小程序 项目目录中 新创建的 images 文件夹中，准备工作就做好了

2. 更改配置文件我们找到项目根目录中的配置文件 app.json 加入如下配置信息

[html] view plain copy print?
"tabBar": {  
   "color": "#a9b7b7",  
   "selectedColor": "#11cd6e",  
   "borderStyle":"white",  
   "list": [{  
     "selectedIconPath": "images/111.png",  
     "iconPath": "images/11.png",  
     "pagePath": "pages/index/index",  
     "text": "首页"  
   }, {  
     "selectedIconPath": "images/221.png",  
     "iconPath": "images/22.png",  
     "pagePath": "pages/logs/logs",  
     "text": "日志"  
   }, {  
     "selectedIconPath": "images/331.png",  
     "iconPath": "images/33.png",  
     "pagePath": "pages/test/test",  
     "text": "开心测试"  
   }]  
 },  
 "tabBar": {
    "color": "#a9b7b7",
    "selectedColor": "#11cd6e",
    "borderStyle":"white",
    "list": [{
      "selectedIconPath": "images/111.png",
      "iconPath": "images/11.png",
      "pagePath": "pages/index/index",
      "text": "首页"
    }, {
      "selectedIconPath": "images/221.png",
      "iconPath": "images/22.png",
      "pagePath": "pages/logs/logs",
      "text": "日志"
    }, {
      "selectedIconPath": "images/331.png",
      "iconPath": "images/33.png",
      "pagePath": "pages/test/test",
      "text": "开心测试"
    }]
  },


解释一下 对应的属性信息 tabBar  指底部的 导航配置属性

color  未选择时 底部导航文字的颜色

selectedColor  选择时 底部导航文字的颜色

borderStyle  底部导航边框的样色（注意 这里如果没有写入样式 会导致 导航框上边框会出现默认的浅灰色线条）

list   导航配置数组

selectedIconPath 选中时 图标路径

iconPath 未选择时 图标路径

pagePath 页面访问地址

text  导航图标下方文字

如果要改变更详细的样式 请参看

https://mp.weixin.qq.com/debug/wxadoc/dev/framework/config.html#tabBar

更多微信小程序教程请扫描二维码关注：H5开发者社区

好了，保存 编译  就可以看到上面的效果了。


文章标签：						 微信小程序						 
