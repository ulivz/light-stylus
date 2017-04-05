# light-stylus

## Quick Start

- install:
```
npm i -S light-stylus
```

- import in your project:
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

## Custom
 
```
/node_modules/light-stylus/config.styl
```