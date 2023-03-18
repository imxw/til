---
title: 选择器基础
date: 2023-03-18 21:25
---
# 选择器基础

CSS 既然是给 HTML 增加样式的，那么如何给特点 HTML元素设置样式呢，这就用到了选择器。

## 标签选择器

也叫元素选择器、类型选择器，直接使用元素标签名作为选择器，将会选择页面上所有该标签，由于其覆盖非常大，所以常用于标签的初始化

```css
ul {
    /* 去掉无序列表的小圆点*/
    list-style: none;
}

a {
    /* 去掉超级链接的下划线*/
    text-decoration: none;
}
```

## class 选择器
使用 class 属性作为元素选择器

基本样式：

```css
.red {
  color: #f33;
}

.yellow-bg {
  background: #ffa;
}

.fancy {
  font-weight: bold;
  text-shadow: 4px 4px 3px #77f;
}
```

##  id 选择器

标签可以有 id 属性，是这个元素的唯一标识。id 选择器即使用 id 属性作为元素选择器。

基本样式：

```html
<!--选择 id 为 para1 的标签-->
#para1 {
    color: red;
}

<p id="para1"> 我是一个段落 </p>
```
