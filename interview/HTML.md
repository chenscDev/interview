# HTML

DOCTYPE是做什么用的?
文档声明描述DTD

# CSS基础

### 实现垂直居中的几种方式?;
### 左边固定宽度右边自适应?
### 分别在左右两侧显示div的几种方式?
### Css九宫格实现?
### 写一个循环播放的动画?

## 盒模型的理解?

### 两种:一种是标准盒模型,一种是ie盒模型
```
  /* 标准模型 */
  box-sizing:content-box;
  标准模型中，盒模型的宽高只是内容（content）的宽高
  /*IE模型*/
  box-sizing:border-box;
  IE模型中盒模型的宽高是内容(content)+填充(padding)+边框(border)的总宽高。
  
```

## @BFC --- 基本概念:
``
  基本概念:其全英文拼写为 Block Formatting Context 直译为“块级格式化上下文”。 BFC的作用是决定了元素如何对其内容进行定位，以及与其他元素的关系和相互作用。其通俗理解可以理解为一个BFC块就是一个独立的单位，其互不打扰。
``
## @BFC --- 原理规则:
``
  BFC元素垂直方向的边距会发生重叠;
  BFC区域不会与float box发生重叠;
  BFC在页面上是一个独立的容器,容器里元素与容器外元素互不影响;
  计算BFC高度的时候,float元素也会参与计算.
``
## @如何创建BFC:
``
  float值不为none;
  position的默认值不为static或者relative;
  display属性与table相关;
  Overflow:hidden;
``


## 移动端适配则怎么做的,能说出来几种?
``
响应式布局: 使用媒体查询
百分比布局: 使用百分比适应屏幕
Flex布局: 使用flex自动适应屏幕尺寸
rem或 em适配:
这两个都是相对单位,由浏览器转换像素值,不同的是rem相对根节点,em相对父节点;
动态适配: 窗口宽度 * 设计稿宽度 / rem倍数
Meta标签:属性 viewport min-scale max-scale no-scaleble
``