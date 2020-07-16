# css

css: Cascading Style Sheets 级联样式单或层叠样式表单。

# 语法

## 一个基本结构，三个注意事项

- 选择器 {样式名:样式值;}

1. 分号分割
2. 小写
3. 逗号分隔

# 特性

- 层叠
- 继承

# 选择器

## 通配符选择器

初始化公共属性

- \* {property:value}

## 元素选择器

即 html 标签选择器

## id 选择器

id 的需要唯一

- #id{property:value}

## 类选择器

- .class{property:value}

可以和元素选择器混合使用

- E.class{property:value}

## 属性选择器

- E[attribute]{property:value}
- E[attribute=value]{property:value}
- E[attribute~=value]{property:value} 包含
- E[attribute|=value]{property:value} 开头

## 伪类选择器

处在一定状态的元素 :checked 等,顺序很重要。

- E?:status{property:value}

## 派生选择器

- 父元素 子元素{property:value} 后代选择器 子元素中所有级

* 父元素>子元素{property:value} 子元素选择器 第一级子元素
* 兄弟 1 元素 + 兄弟 2 元素{property:value} 相邻兄弟选择器 俩个元素必须同级且相邻

# 权重

- 通配符选择器的权重：0
- 标签选择器的权重：1
- 类,伪类,属性选择器的权重：10
- id 选择器的权重：100
- 内联样式的权重：1000
- 特殊处理：!important(强制使用)

# 常用属性

## 字体

- font-family 字体主题
- font-size 字体大小
- font-style 字体倾斜
- font-weight 字体粗细

## 文本

- color 颜色
- line-height 行高
- text-align 对齐方式
- direction 方向
- text-indent 缩进
- text-decoration 装饰线
- letter-spacing 间隔
- text-shadow 阴影

## 尺寸

- 宽度和高度 auto,长度,百分比
- 最小宽度和最小高度
- 最大宽度和最大高度

## 列表

- list-style-image 使用图片作为列表项前面的标记
- list-style-position 标记位置
- list-style-type 标记类型，跟 ul 的 type 相同
- list-style

## 背景

- background-color 背景颜色
- background-image 背景图片
- background-repeat 平铺设置
- background-position 初始位置, 左上角为 0
- background-attachment 滚动
- background

# 盒模型

- Box Model width = 2\*margin + 2\*border+ 2\*padding + div

## 内边距 padding

## 边框 border

## 外边距 margin 左右剧中 0 auto

## display

修改元素默认 display 块级和内联

- none,
- block,
- inline 不能设置宽高,
- inline-block 设置宽高时 block
  - 内联元素间隙问题 body {font-size: 0}

# 浮动

## 浮动

- float: left right default none

## 清除浮动

- 原因:元素设置为浮动时引起的父元素内容塌陷，影响布局效果。
- clear: clear 属性用于设置元素哪一侧不允许浮动
  - left
  - right
  - both
  - none 默认值
- overflow: overflow 属性用于设置元素不够容纳内容时的显示方式
  - visible 默认值
  - auto 自动添加滚动条
  - hidden 隐藏超出的内容
  - scroll 一直显示滚动条

## 布局

### 三列布局

1. 实现一个左中右布局
2. 左右俩侧宽度固定
3. 中间内容区宽度能够自适应

#### 双飞翼布局

1. 使用 float 属性让左中右三列浮动
2. 使用负 margin 属性让做鱼俩列与中间列处于同一水平线上
3. 在中间列中增加 div 内容元素，设置 margin 值为左右俩列的宽度
4. 清除浮动，让父元素高度正常显示

# 定位 position
 ## 标准布局 static 默认
 ## 固定布局 fixed 
 ## 相对布局 relative
 ## 绝对布局 absolute
 ## 辅助属性 left right top buttom 
 ## 层级属性 z-index

# 兼容问题

1. 删除浏览器初始化样式。

- body {font-size: 0}
- \*{margin:0; padding:0}
