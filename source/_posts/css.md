---
title: Css-flex布局
tags: 
    - C3
categories:
    - C3
date: 2021-08-01 22:10:00
top_img: ../../img/bz-a.jpg
cover: ../../img/bz-c.jpg
---

## css提高篇.

### flex布局

``` Flex
$ flex布局是什么？
Flex 是 Flexible Box 的缩写，意为"弹性布局"，用来为盒状模型提供最大的灵活性.
采用 Flex 布局的元素，称为 Flex 容器（flex container），简称"容器"。它的所有子元素自动成为容器成员，称为 Flex 项目（flex item），简称"项目".


```
More info: [flex](https://www.ruanyifeng.com/blog/2015/07/flex-grammar.html)

### flex-direction
``` 
flex-direction属性决定主轴的方向（即项目的排列方向).
取值：
row（默认值）：主轴为水平方向，起点在左端。
row-reverse：主轴为水平方向，起点在右端。
column：主轴为垂直方向，起点在上沿。
column-reverse：主轴为垂直方向，起点在下沿。

```
### flex-wrap
```
默认情况下，项目都排在一条线（又称"轴线"）上。flex-wrap属性定义，如果一条轴线排不下，如何换行。
取值：
nowrap（默认）：不换行。
wrap：换行，第一行在上方。
wrap-reverse：换行，第一行在下方。
```
### flex-flow
```
flex-flow属性是flex-direction属性和flex-wrap属性的简写形式，默认值为row nowrap。

```

### justify-content
```
justify-content属性定义了项目在主轴上的对齐方式。
取值：
flex-start（默认值）：左对齐
flex-end：右对齐
center： 居中
space-between：两端对齐，项目之间的间隔都相等。
space-around：每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍。
```
### align-items
```
align-items属性定义项目在交叉轴上如何对齐。
取值：
flex-start：交叉轴的起点对齐。
flex-end：交叉轴的终点对齐。
center：交叉轴的中点对齐。
baseline: 项目的第一行文字的基线对齐。
stretch（默认值）：如果项目未设置高度或设为auto，将占满整个容器的高度。
```
### align-content
```
align-content属性定义了多根轴线的对齐方式。如果项目只有一根轴线，该属性不起作用。
取值：
flex-start：与交叉轴的起点对齐。
flex-end：与交叉轴的终点对齐。
center：与交叉轴的中点对齐。
space-between：与交叉轴两端对齐，轴线之间的间隔平均分布。
space-around：每根轴线两侧的间隔都相等。所以，轴线之间的间隔比轴线与边框的间隔大一倍。
stretch（默认值）：轴线占满整个交叉轴。
```
###  flex-shrink
```
flex-shrink属性定义了项目的缩小比例，默认为1，即如果空间不足，该项目将缩小。
flex-shrink：0,不随着屏幕的缩小而缩小.
```
