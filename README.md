# trans
a small and fast translator living in macOS menu bar

-------

## 🧾 更新日志 👇👇🏻👇🏼👇🏽👇🏾👇🏿

### 2020/02/05 Updated 中国加油

1. 加入截图翻译功能，右键菜单栏图标或使用快捷键Ctrl+A（百度图片识别接口）
2. 修复了设置窗口同时打开多个的问题
3. 零零散散的小问题

### 2020/01/24 Updated 大噶除夕快乐

1. UI由XIB改为storyboard
2. 增加设置功能，用户可选择使用百度翻译或有道翻译，以及使用自己的APPID和KEY
3. 最低支持版本为 macOS 10.14 Mojave
4. 程序体积在1M以内，由于需要支持Mojave编译后膨胀到10+M，对体积有要求的朋友可以下载Catalina版本或自行修改deployment target编译

## 📓 系列教程 👈👈🏻👈🏼👈🏽👈🏾👈🏿

想入门如何编写macOS应用的同学可以关注一下我的博客，系列教程正在酝酿中，会随着我更新trans过程中新学的知识同步更新：

1. [macOS新手开发教程（一）准备工作
](https://rhinoc.top/macos_1/)
1. [macOS新手开发教程（二）构建菜单栏应用](https://rhinoc.top/macos_2/) 
2. 未完待续……

## 🤐 碎碎念

前几天在macOS的App Store上看到一个叫「小翻译」的应用：
<img src="https://pic.rhinoc.top/mweb/15715563982330.jpg" width="50%">

当时觉得挺简单的，监控剪贴板再随便调用一个在线翻译的API就行了。但是蓝色的图标放菜单太违和了。就想着自己能不能也做一个，于是「trans」就出来了。

和小翻译一样，trans也是一个菜单栏应用，目前支持输入搜索和复制搜索，搜索调用的接口是百度翻译的API。

点击菜单栏的图标可「输入搜索」：

![](https://pic.rhinoc.top/mweb/15717457312566.jpg)

![](https://pic.rhinoc.top/mweb/15717457549055.jpg)

保持后台开启，剪贴板变动的时候触发「复制搜索」，鼠标移到通知可复制翻译结果：

![](https://pic.rhinoc.top/mweb/15715578064917.jpg)

![](https://pic.rhinoc.top/mweb/15717457944937.jpg)


设想的应用场景和优势：
1. 浏览网页、文档时。由于是Application作为载体，所以相比于浏览器的划词翻译有更宽泛的使用场景。
2. 不需要精准翻译和单词管理时。相比欧路词典、有道词典更加轻量化，仅500KB，无论是磁盘还是内存占用都可忽略不计。
3. 希望获得更原生更自然的体验时。使用Swift语言开发的native应用，macOS原生控件。不需要的时候分分钟泯然众应用中。
4. 更安全，更隐私。由于能力不足没有历史记录等记录数据的功能，唯一的网络请求是GET百度翻译的API。
5. 调用百度翻译，相比内置词典有更全和更不准确的词库。

第一次接触macOS开发，由于是兴趣开发所以之后更不更新就随缘了，可能和~~稻米鼠停更他的公众号一样~~就再也不更新了。

梦想中的TO DO：
* [x] 复制翻译
* [x] 输入搜索翻译
* [ ] 设置-开机自启
* [x] 设置-原文语言和目标语言
* [x] 设置-API选择和Token设置
* [ ] 第一次开启应用时不弹Popover
* [x] 输入翻译时的TextFiled显示优化
* [ ] 快捷键翻译
* [x] 截图OCR识别+翻译
* [ ] 类似PC版有道词典的截屏翻译（保留格式那种）
* [ ] 截图翻译快捷键和源自定义
* [ ] 截图翻译支持小语种

图标是在阿里爸爸的iconfont上找的，用Sketch做了个白色描边以适应暗黑模式。