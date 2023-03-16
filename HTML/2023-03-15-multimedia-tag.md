---
title: 多媒体标签
date: 2023-03-15 22:34
---
# 多媒体标签




## 图片标签

`<img src="images/test.jpg" alt="">`

- img 是 image 的缩写
- src 是 source 的缩写，src 的值是图片的路径，可以在本地也可以在云端，图片要存放在项目目录中，且图片后缀名必须带上
- alt 是 alternate 的缩写，是对图片的文本描述，图片加载有问题时会显示，也可以供视力不方便的朋友使用网页朗读器时也会朗读 alt 中的内容

`<img>`标签还有 width 与 height 属性，分别设置图片的高与宽，只设置其中一个值即可，图片会整体缩放

网页上支持的图片格式有：
- `.bmp`
- `.gif`
- `.jpeg(.jpg)`
- `.png`
- `.svg`
- `.webp`

## 超链标签

`<a href="https://www.google.com">去谷歌</a>`
- a 时 anchor（锚）的首字母
- href 属性指的是`hypertext reference(超文本引用)`，其值指链接的路径，可以是相对路径，也可以是绝对路径，可以在本地，也可以在云端

### title属性
用来设置鼠标的悬停文本

### target 属性
点击超链时默认在当前页打开，通过设置 target 值为 blank 可以在新页打开

### 给图片设置超链

```html
<a href="xxx.html" target="blank">
    <img src="images/xxx.jpg">
</a>
```

### 下载链接

指向exe、zip、rar等文件格式的链接，将自动成为下载链接

`<a href="xxx.zip">点击下载</a>`

### 邮件链接

有`mailto:`前缀的链接是邮件链接

`<a href="mailto:me@test.com">给小编发邮件</a>`

### 电话链接

有`tel:`前缀的链接是电话链接

`<a href="tel:12306">打电话买火车票</a>`

## 音频标签

使用`<audio>`标签来插入音频

```html
<audio controls src="音频地址">
    抱歉，您的浏览器不支持 audio 标签，请升级浏览器
</audio>.
```

- controls 属性用来显示播放控件
- 标签对中的内容是对不兼容 audio 标签的浏览器显示的文字
- 声明 loop 属性后，会循环播放音频
- 声明 autoplay 属性后，会自动播放音频

## 视频标签

使用`<video>`标签来插入视频

```html
<video controls src="视频地址">
    抱歉，您的浏览器不支持 video 标签，请升级浏览器
</video>.
```

- controls 属性用来显示播放控件
- 标签对中的内容是对不兼容 video 标签的浏览器显示的文字
- 声明 loop 属性后，会循环播放视频
- 声明 autoplay 属性后，会自动播放视频