---
title: "CSS选择器的使用"
date: 2021-08-13T21:01:17+08:00
slug: css-select-tool
image: css.png
draft: false
tags: [css]
categories: blog
---

# CSS选择器的使用

## CSS 元素选择器

元素选择器根据元素名称来选择 HTML 元素。

**实例：**使页面上的所有 <p> 元素带有红色文本颜色：

```css
p {
  color: red;
}
```

------

## CSS id 选择器

id 选择器使用 HTML 元素的 id 属性来选择特定元素。

元素的 id 在页面中是唯一的，因此 id 选择器用于选择一个唯一的元素！

要选择具有特定 id 的元素，请写一个井号（＃），后跟该元素的 id。

**注意：**id 名称不能以数字开头。

**实例**

这条 CSS 规则将应用于 id="testid" 的 HTML 元素：

```css
#testid {
  color: red;
}
```

------

## CSS 通用选择器

通用选择器（*）选择页面上的所有的 HTML 元素。

**实例**

下面的 CSS 规则会影响页面上的每个 HTML 元素：

```css
* {
  padding: 0
}
```

------

## CSS 分组选择器

分组选择器选取所有具有相同样式定义的 HTML 元素。

```css
h1 {
  text-align: center;
  color: red;
}

h2 {
  text-align: center;
  color: red;
}
```

------

## CSS 类选择器

```html
<p class=test>
    test text
</p>
```

下面是类选择器的使用

```css
.test {
    color:pink
}
```

