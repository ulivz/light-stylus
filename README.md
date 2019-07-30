# light-stylus

[![Greenkeeper badge](https://badges.greenkeeper.io/ulivz/light-stylus.svg)](https://greenkeeper.io/)

A simple and commonly used style(stylus) library

## Quick Start

- 安装
```
npm i -S light-stylus
```

- 在你的项目中导入
```js
import 'light-stylus/src/index.styl'
```

## Mixins

### layout

mixin|description
---|---
`$clearfix()`|清除浮动
`$clearfix-another()`|采用`overflow`清除浮动
`$flex-container()`|`flex`的容器
`$flex-fixed-width(width)`|固定宽度的`flex item`
`$flex-dynamic-width()`|动态宽度的`flex item`
`$absolute-center()`|绝对水平居中
`$single-line-center(height, fontSize)`|单行文字水平居中（应用于父元素）
`$multi-line-center-parent(width, height)`|多行文字水平居中（应用于父元素）
`$multi-line-center-child()`|多行文字水平居中（应用于子元素）
`$text-overflow-ellipsis(lines)`|一行或多行文字溢出显示省略号

### effect

mixin|description
---|---
`$rotate(angle)`|`2D`旋转
`$translate(x, y)`|`2D`偏移
`$translate3d(x, y)`|`3D`偏移
`$scale(x, y)`|`2D`缩放
`$scale3d(x, y)`|`3D`缩放
`$transition(time)`|设置过渡效果时长，默认值为`0.3s`

## 内置样式

内置样式的默认前缀为`v`，部分内置样式如下：

### Border Radius

css|default
---|---
`.v-radius-base`|`border-radius 6px`
`.v-radius-small`|`border-radius 4px`

### Box Shadow
css|default
---|---
`.v-shadow-base`|`box-shadow: 0 1px 6px rgba(0, 0, 0, .2)`
`.v-shadow-card`|`box-shadow: 0 1px 1px 0 rgba(0,0,0,.1)`
`.v-shadow-up`|`box-shadow: 0 -1px 6px rgba(0, 0, 0, .2)`
`.v-shadow-down`|`box-shadow: 0 1px 6px rgba(0, 0, 0, .2)`
`.v-shadow-left`|`box-shadow: -1px 0 6px rgba(0, 0, 0, .2)`
`.v-shadow-right`|`box-shadow: 1px 0 6px rgba(0, 0, 0, .2)`

### Color
css|default
---|---
`.v-primary`| `#3399ff`
`.v-info`| `#2db7f5`
`.v-success`| `#00cc66`
`.v-warning`| `#ff9900`
`.v-error`| `#ff3300`
`.v-bg-primary `| `#3399ff`
`.v-bg-info`| `#2db7f5`
`.v-bg-success `| `#00cc66`
`.v-bg-warning `| `#ff9900`
`.v-bg-erro`| `#ff3300`

## Transform
css|description
---|---
`.v-rotate-reverse`| 旋转`180°`

## Box
css|description
---|---
`.v-content-box`| 普通盒模型
`.v-border-box`| 怪异盒模型

## Text Overflow
css|description
---|---
`.v-text-ellipsis-1`| `1`行文字溢出显示省略号
`.v-text-ellipsis-2`| `2`行文字溢出显示省略号

## @media
css|default
---|---
`@media (min-width: $screen-xs)`|`480px`
`@media (min-width: $screen-sm)`|`768px`
`@media (min-width: $screen-md)`|`992px`
`@media (min-width: $screen-lg)`|`1200px`


## 自定义

可以通过修改以下文件来修改`css`前缀和各种默认值： 

```
/node_modules/light-stylus/config.styl
```

默认配置如下：

```stylus
$css-prefix = v

/* Colors
   ========================================================================== */
$primary-color          = #3399ff
$info-color             = #2db7f5
$success-color          = #00cc66
$warning-color          = #ff9900
$error-color            = #ff3300

/* Font Size
   ========================================================================== */
$font-size-xxl          = 20px
$font-size-xl           = 18px
$font-size-l            = 16px
$font-size-m            = 14px
$font-size-s            = 12px
$font-size-xs           = 10px

/* Font Family
   ========================================================================== */
$font-family            = "Helvetica Neue",Helvetica,"PingFang SC","Hiragino Sans GB","Microsoft YaHei","Microsoft YaHei UI", "Microsoft YaHei UI Light",Arial,sans-serif

/* Border Radius
   ========================================================================== */
$border-radius-base     = 6px
$border-radius-small    = 4px


/* Media Query
   ========================================================================== */
// Extra small screen / phone
$screen-xs              = 480px
$screen-xs-min          = $screen-xs
$screen-xs-max          = ($screen-xs-min - 1)

// Small screen / tablet
$screen-sm              = 768px
$screen-sm-min          = $screen-sm
$screen-sm-max          = ($screen-sm-min - 1)

// Medium screen / desktop
$screen-md              = 992px
$screen-md-min          = $screen-md
$screen-md-max          = ($screen-md-min - 1)

// Large screen / wide desktop
$screen-lg              = 1200px
$screen-lg-min          = $screen-lg
$screen-lg-max          = ($screen-lg-min - 1)


/* Animation
   ========================================================================== */
$transition-time        = .3s


/* Box Shadow
   ========================================================================== */
$shadow-color           = rgba(0, 0, 0, .2)
$shadow-base            = $shadow-down
$shadow-card            = 0 1px 1px 0 rgba(0,0,0,.1)
$shadow-up              = 0 -1px 6px $shadow-color
$shadow-down            = 0 1px 6px $shadow-color
$shadow-left            = -1px 0 6px $shadow-color
$shadow-right           = 1px 0 6px $shadow-color
```