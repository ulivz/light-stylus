# light-stylus

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

方法|描述
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

### effect

方法|描述
---|---
`$rotate(angle)`|`2D`旋转
`$translate(x, y)`|`2D`偏移
`$translate3d(x, y)`|`3D`偏移
`$scale(x, y)`|`2D`缩放
`$scale3d(x, y)`|`3D`缩放
`$transition(time)`|设置过渡效果时长，默认值为`0.3s`

## 内置样式

内置样式的默认前缀为`v`,可以通过修改以下文件来修改`css`前缀和各种默认值： 

```
/node_modules/light-stylus/config.styl
```

内置样式如下：

### Border Radius

css|描述
---|---
v-radius-base|border-radius 6px
v-radius-small|border-radius 6px

### Box Shadow
css|描述
---|---
v-shadow-base|box-shadow: 0 1px 6px rgba(0, 0, 0, .2)
v-shadow-card|box-shadow: 0 1px 1px 0 rgba(0,0,0,.1)
v-shadow-up|box-shadow: 0 -1px 6px rgba(0, 0, 0, .2)
v-shadow-down|box-shadow: 0 1px 6px rgba(0, 0, 0, .2)
v-shadow-left|box-shadow: -1px 0 6px rgba(0, 0, 0, .2)
v-shadow-right|box-shadow: 1px 0 6px rgba(0, 0, 0, .2)

### Color
css|描述
---|---
v-primary| <div style="width:10px; height: 10px; background: #000"></div>
v-info|
v-success|
v-warning|
v-error|
v-bg-primary|
v-bg-info|
v-bg-success|
v-bg-warning|
v-bg-error|

## 自定义
 
