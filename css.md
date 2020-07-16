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

# 定位 position
 ## 标准布局 static 默认
 ## 固定布局 fixed 
 ## 相对布局 relative
 ## 绝对布局
 ## 辅助属性
 ## 层级属性

# 兼容问题

1. 删除浏览器初始化样式。
