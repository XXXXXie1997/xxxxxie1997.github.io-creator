---
title: "HTML常用标签"
date: 2020-04-13T10:29:25+08:00
draft: false
---

a 标签的用法
img 标签的用法
table 标签的用法
其他感想

1. a 标签：

   a 标签为超链接，它的作用是可以跳转到外部页面或跳转至页面内部的锚点。
   a 标签可加入的属性：

- `href`指定连接方向，（值可为外部连接，也可为内部 id 以及邮箱、电话等）。
- `target`通过赋予值可以决定跳转在哪里打开，默认值为`_self`即当前页面（`_blank`为空白页打开，`_top`在顶层页面打开，`_parent`在父级页面打开）。也可通过给 iframe 命名达到在 iframe 中打开的效果。
- `download`赋予该属性的连接会被下载。

2. img 标签：

   img 标签用于发出一个 get 请求，向用户展示一张图片。
   可加入的属性：

- `src`图片路径（这个属性必须有，否则会报错）。
- `alt`在图片加载失败后，会显示 alt 中的内容。
- `height 和 width`决定图片的高和宽，值可以为固定像素，也可以为百分比（宽和高如果只写一个值，另一个值会根据图片原始比例自动适应，_两个都写可能导致图片变形_）。
- （响应式：`img {max-width:100%}`意为最大宽度为屏幕的 100%，大小会自动适应，可用于移动端页面开发。）

table 标签：

table 为表格标签，一般由`thead tbody tfoot`组成。（都不写的话内容会自动写入 tbody）
大致格式为：

```html
<thead>
  <tr>
    <th></th>
    <th>横表头1</th>
    <th>横表头2</th>
    <th>横表头3</th>
  </tr>
</thead>
<tbody>
  <tr>
    <th>竖表头1</th>
    <td>值1.1</td>
    <td>值1.2</td>
    <td>值1.3</td>
  </tr>
  <tr>
    <th>竖表头2</th>
    <td>值2.1</td>
    <td>值2.2</td>
    <td>值2.3</td>
  </tr>
</tbody>
```

可以得到一个 4 x 3 的表格

- `table-layout`用于定义单元格布局的算法。（值为`auto`时根据内容自动计算布局、值为`fixed`时会尽量等宽）
- `border collapse:collapse`样式属性，用于合并表格（去掉单元格边距）
- `border spacing:0px`设置单元格间隔为 0

form 标签：

作用为发送 get 或 post 请求，然后刷新页面。
可添加属性：

- `action="/xxx"`向 xxx 页面发送 get 请求（如果添加`method="post"`即为发送 post 请求）。
- `autocomplete`自动填充，用法比较复杂以后会继续学习。
- `target="a"`将表单内容提交至 a 页面。
- **一个 form 表单必须有一个名为`type="submit"`的 input 或 botton 标签，这个表单才可以正常提交。**

input 标签：

这个标签有很多的 type 属性值，在这里举几个例子：

- `type="text"`文本框
- `type="color"`选择颜色
- `type="password"`密码，输入的文本会被隐藏
- `type="gender"`单选
- `type="checkbox"`多选
- `type="file"`上传文件，如果赋予`multiple`属性，则可以同时上传多个文件
- `type="hidden"`隐藏输入（一般用于 JS 拉去数据提交）

还有很多标签以及属性有些生涩难懂，还需要多多练习，温故而知新。
