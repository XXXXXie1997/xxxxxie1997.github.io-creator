---
title: "HTML入门笔记1"
date: 2020-04-12T14:08:00+08:00
draft: false
---

1. HTML 是李爵士（Tim Berners-Lee，也是 Web 的发明者）和他的同事在 1990 年创立的超文本标记语言。

2. **html 的起手式：**

```html
<!DOCTYPE html>
<html lang="zh-CN">
  <head>
    <title>网页的标题</title>
  </head>
  <body>
    网页的主要内容
  </body>
</html>
```

3. 常用的章节标签：

- `h1~h6`分别表示 1 至 6 级标题
- `section`表示新章节
- `p`为段落
- `header`为网页头部
- `footer`为网页底部
- `main`为网页的主要内容
- `aside`为网页的旁支内容
- `div`将网页内容划分为几个部分

4. 全局属性（指所有标签都能添加的属性）

- `class` --给标签赋予一个类
- `contenteditable` --添加该属性的标签可以在页面中被编辑
- `hidden` --添加该属性的标签内容会被隐藏
- `id` --给标签赋予一个 id
- `style` --给标签设置样式
- `tabindex` --添加该属性的标签内容在页面中可以被 tab 选中，属性值为数字，数字越小越先被选中（0 为最后被选中）
- `tittle` --属性会将完整内容显示在页面上

5. 常用的内容标签：

- `ol+li` --有序列表，li 包裹在 ol 中，是有序列表的内容
- `ul+li` --无序列表，用法同有序
- `dl+dt+dd` --描述列表，dt 为被描述内容，dd 为该内容的描述
- `pre` -- 被 pre 包裹的内容，所有的空格都将保留
- `code` --被 code 包裹的内容会使用等宽字体
- `hr` --水平分割线
- `br` --换行
- `a` --超链接
- `em` --强调语气
- `strong` --强调内容本身
- `quote` --内联引用
- `blockquote` --块引用
