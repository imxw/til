---
title: HTML 基础
date: 2023-03-13 10:27
---

HTML(HyperText Mark Language): 超文本标记语言，用来定义 web 的内容，web 样式由 CSS 定义，web 中的动作由 JavaScript 定义

## 基本格式
```html
<!DOCTYPE html>
<html>
	<head>
    	<meta charset="utf-8" />
      	<title> 页面标题 </title>
    </head>
  	<body>
    	<p>Hello, World!</p>
    </body>
</html>
```
- `<!DOCTYPE>`: 定义文档类型
- `<html>`: 定义一个 HTML 文档
- `<title>`: 为文档定义一个标题
- `<body>`: 定义文档的主体
- `<meta>`: 定义关于文档的元数据元素
- `<head>`: 定义文档相关的配置信息（元数据），内容对用户不可见，包括文档标题、引用的文档样式和脚本等
## 标签与元素
上节中的`<html>`、`<body>`、`<p>`等被称为标签，即所谓的标记（markup），用来注明文本、图片以及其他内容

一个标签的实例被称为元素，如`<p>Hello World!</p>`即是一个元素，`<p>`是这一元素的开始标签，`</p>`是其结束标签，`Hello World!`是其内容。

不包含任何内容的元素称为空元素，如`<img>`元素（`<img src="xxx" />`）。
HTML 就是由一系列元素组成。

### 元素属性

`<tag attr1="v1" attr2="v2">content</tag>`

- 全局属性：所有标签都有的属性
    - id 定义元素的唯一 id
    - class 定义元素的类名，可以定义多个，可以方便为其指定样式
    - style 规定元素的行内样式
    - title 描述元素的额外信息
- 标签属性：部分标签的独有属性，无需记忆，用时查即可

## 常用标签
- 注释：`<!-- 我是注释 -->`
- 标题: `<h1> 标题一 </h1>`，一共有 6 级标题，即 h1~h6
- 换行: `<br/>`
- 段落: `<p>我是一个段落</p>`
- 删除文本：`<del>我被删除了</del>`
- 斜体: `<i>斜体</i>`
- 下划线: `<u>下划线文本</u>`
- 超链接
    - `<a href="https://www.baidu.com">百度</a>`，在当前页打开，即`target=self`
    - `<a href="https://www.baidu.com" target=_blank>百度</a>`，在新的页面打开
- 图片: `<img src=xxx><img>`，src 可为相对路径，也可以为绝对路径
- 列表 `<li>元素</li>`表示列表中一项
    - 有序列表 `<ol>xxx</ol>`
    - 无序列表 `<ul>xxx</ul>`
- 表格
    - `<table></table>`来包裹整个表格
    - `<thead></thead>`来包裹表格头
    - `<td></td>` 表示一个单元格(table data)
    - `<tr></tr>`表示一个单元行(table row)，用来包裹单元格
    - `<th>`表示一个单元头的标题，用于`<thead></thead>`中
- 表单
    - `form`
    - `input`
- 块标签
    -  `<div></div>`定义文档中的一个分隔区块或者一个区域部分，每个 div 独占行
    - `<span></span>`行级别，span 中的内容都在同一行

## 元素 id
用来标识该元素的唯一身份，可以在其他地方引用。

如通过 a 标签跳转到指定位置

```html
<p>
<a href="#C4">查看章节 4</a>
</p>

<h2>章节 1</h2>
<p>这边显示该章节的内容……</p>

<h2>章节 2</h2>
<p>这边显示该章节的内容……</p>

<h2>章节 3</h2>
<p>这边显示该章节的内容……</p>

<h2><a id="C4">章节 4</a></h2>
<p>这边显示该章节的内容……</p>
```

id 也是 js 操作元素的重要依据之一

```javascript
document.getElementById('C4')
<a id=​"C4">​章节 4​</a>​
```

## 元素的样式

通过元素的 style 属性可以控制该元素的样式。

如将 p 元素中的内容加大字体，颜色设置为红色

```html
<p style="color:red;font-size:20px;">段落内容</p>
```

语法格式为: `key:value;`，每个样式条目由分号分开，从而为一个元素添加多个样式

## 脚本
有了元素和样式，我们得到的还是一个静态页面。页面加载完成后，如何动态修改元素呢？这就用到 js 了

使用`<script>`标签来定义脚本，该元素中即可以包含脚本语句，也可以通过`src`属性指向外部脚本文件

```html
// 通过src 网络引入
<script src="https://cdn.jsdelivr.net/npm/vue@2.6.14"></script>

// 通过本地文件引入
<script>
  import axios from 'axios';
</script>
```