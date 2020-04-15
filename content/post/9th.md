---
title: "CSS常见布局1：float布局"
date: 2020-04-15T20:30:48+08:00
draft: false
---

**float 布局**：
步骤：

1. 在子元素上添加属性`float:left;`和`width`
2. **给添加 float 属性元素的父元素赋予`clearfix`类，然后再样式表中编辑如下内容**：

```css
.clearfix::after {
  content: "";
  display: block;
  clear: both;
}
```

_这个 CSS 样式可以让父元素包裹住那些因为赋予`float`样式而脱离文档流的元素。_
**很关键，一定要写！**
**很关键，一定要写！**
**很关键，一定要写！**

- 如果图片下面多出来一部分内容如背景色，使用`vertical-align:middle;`即可消去多于内容（没有为什么，目前死记硬背即可。）
- 当 border 因为占页面空间而扰乱了布局时，可以将 border 改为`outline`，这样 border 就不会占据盒模型空间了。
- 如果要做平均分布，在内容中加入一个任意名字的新图层（标签如 div），赋予一个`-margin`属性，可以将空间推宽。（尚未研究明白，后续会继续学习）

**前辈的经验**：

1. 一行的最后一个元素不设`width`值或者留一些空间以备不时之需。
2. float 布局不需要考虑响应式，因为这个布局专为 IE 浏览器准备而手机一般没有 IE 浏览器，只有傻子采用 float 布局做手机页面。
3. IE6/7 存在双倍 margin 的 bug，解决方法：

- 针对 IE6/7 把元素的 margin 改为一半。
- 将元素改为 inline-box 元素（加一个`display:inline-box;`）

4. 只需要给页面加上头尾（`header`和`footer`），即可满足 pc 页面需求。
5. float 布局需要程序猿自己计算各元素宽度，使用起来不灵活。
6. CSS 没有为什么。
