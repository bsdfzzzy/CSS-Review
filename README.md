# CSS-Review
  * <font size="20px">现在是基础部分</font>
  * <font size="20px">[进阶部分](https://github.com/bsdfzzzy/CSS-Review/blob/master/deeper.md)</font>

##目录
 * [选择器](#选择器)
   * [类选择器](#类选择器)
   * [ID选择器](#ID选择器)
   * [伪类选择器](#伪类选择器)
 * [格式（可读性）](#格式（可读性）)
 * [文本样式](#文本样式)
 * [颜色](#颜色)
 * [内容](#内容)
 * [列表](#列表)
 * [盒模型](#盒模型)
 * [布局](#布局)
 * [表格](#表格)
 * [媒体](#媒体)

##选择器
  * ### 类选择器
  
  * ### ID选择器
  
  * ### 伪类选择器
    - :link
    
      > 选择为被点击过的链接
    - :visited
     
      > 选择被点击过的链接
    - :active
     
      > 选择被激活的元素
    - :hover
     
      > 鼠标指上的元素
    - :focus
     
      > 获得焦点的元素
    - :first-child
     
      > 获取第一个子元素
    - :nth-child
     
      > :nth-child(an+b)匹配子元素中前面有an+b-1个兄弟元素的元素
    - :nth-last-child
     
      > :nth-last-child(an+b)匹配子元素中后面有an+b-1个兄弟元素的元素
    - :nth-of-type
    
      > :nth-of-type(an+b)匹配子元素中位置为an+b-1的和：前面同样选择器的元素
    - :first-of-type
    
      > 匹配子元素中第一个元素和：前面同样选择器的元素
    - :last-of-type
    
      > 匹配子元素中最后一个元素和：前面同样选择器的元素
    - :empty
    
      > 匹配没有子元素的元素
    - :target
    
      > 用id选择器匹配链接中的href="#XXX"的链接
    - :checked
    
      > 表示radio、checkbox、option等选中时候的状态
    - :enabled
    
      > 表示任何启用（被激活或获取焦点）的元素
    - :disabled
    
      > 表示任何被禁用的元素

##格式（可读性）


##文本样式
  * font-family
    - 使用一个字体名和一个字体族名 `font-family: Gill Sans Extrabold, sans-serif;`
    - 只是用一个字体名 `font-family: sans-serif;`
  * font-size
    - 绝对大小值 `xx-small`、`x-small`、`small`、`medium`、`large`、`x-large`、`xx-large`
    - 相对大小值 `larger`、`smaller`
    - 长度值
      - `px`  大小固定
      - `em`  1em是父元素设置的font-size的大小;如果没有任何地方设置font-size的话，它将等于浏览器默认字体大小
    - 百分比值 `80%`、`inherit`
  * line-height
    - `normal` 取决于用户代理，桌面浏览器使用默认值，约为1.2，取决于font-family
    - `<number>` number乘以font-size值
    - `<length>` 3em, 10px
    - `<percentage>`
    - `inherit`
    - `initial`
    - `unset`
  * text-decoration
    - 初始值： `text-decoration-line: none` `text-decoration-style: solid` `text-decoration-color: currentColol`
    - `underline red`
    - `none`
    - `underline wavy red`
    - `inherit`
    - `initial`
    - `unset`
  * font-style
    - `normal`
    - `italic` 手写倾斜
    - `oblique` 一般字体的倾斜
  * font-weight
    - `normal` 等于400
    - `bold` 等于700
    - `lighter`
    - `bolder`
    - `X00`
    - `inherit`
  * font-variant
    - `small-caps`
    - `common-ligatures small-caps`
  * font
    - style | variant | weight | size/line-height | family
    - `font: italic small-caps bolder 16px/3 cursive;`

##颜色
  * rgb( 0 ~ 256, 0 ~ 256, 0 ~ 256, 透明度 )

##内容
  * content
    - :before
    - :after
  * background
    - `background-image: none` `background-position: 0% 0%` `background-size: auto auto` `background-repeat: repeat` `background-origin: padding-box` `background-clip: border-box` `background-attachment: scroll` `background-color: transparent`
    - `background-attachment` 决定背景是在视口中固定的还是随包含它的区块滚动的
      - `scroll`、`fixed`、`local`、`inherit`
    - `background-clip` 设置元素的背景（背景图片或颜色）是否延伸到边框下面
      - `border-box`、`padding-box`、`content-box`、`inherit`
    - `background-color`
    - `background-image`
      - `url(http://www.example.com/bck.png);`
    - `background-position` 指定背景图片的初始位置
      - `top`、`bottom`、`left`、`right`、`center`、`25% 75%`、`0px 0px, center`
    - `background-repeat` 指定背景图片是否以平铺效果重复出现，以及重复的方式
      - `repeat-x`、`repeat-y`、`repeat`、`space`、`round`、`no-repeat`、`双值语法：水平 垂直`
    - `background-size` 设置背景图片大小
      - `cover`、`contain`
      - 一个值指定图片的宽度，高度为auto `50%`、`3em`
      - 两个值指定宽度和高度 `5em 25%`
      - 逗号分隔的多个值设置多重背景 `auto, auto`、`50%, 25%, 25%`、`6px, auto, contain`

##列表
  * list-style 语法：`<'list-style-type'> || <'list-style-position'> || <'list-style-image'>`
    - list-style-type 语法：`<counter-style> | <string> | none`
    - list-style-image `url('starsolid.gif');`
    - list-style-position `inside`、`outside`
  * counter
    - `content: counter(mynum) ": ";`
      `counter-increment: mynum;`
      为相同的选择元素初始化计数器

##盒模型
  * 元素
  * 內边距
  * 边框
  * 外边距
  * dispaly
    - `none`
    - `inline` 该元素生成一个或多个行内元素盒。
    - `block` 该元素生成一个块元素盒。
    - `list-item` 该元素生成一个容纳内容和单独的列表行内元素盒的块状盒。
    - `inline-block` 该元素生成一个块状盒，该块状盒随着周围内容流动，如同它是一个单独的行内盒子（表现更像是一个被替换的元素）
    - `table` 这个元素的作用就像  <table> 元素. 它定义了一个块级盒子.
    - `inline-table` 一个table行内元素盒，内部元素是block的
    - `table-caption` 这个元素的作用的就像<caption> 一样。.
    - `table-cell` 这个元素的作用就像<td> 一样。
    - `table-column` 这个元素的作用就像<col> 一样
    - `table-column-group` 这个元素的作用就像<colgroup> 一样。
    - `table-footer-group` 这个元素的作用就像<tfoot> 一样.
    - `table-head-group` 这个元素的作用就像<thead> 一样
    - `table-row` 这个元素的作用就像<tr> 一样.
    - `table-row-group` 这个元素的作用就像<tr> 一样.
    - `flex`
    - `inline-flex`
    - `grid`
    - `inline-grid`

##布局
  * position： `relative`、`absolute`、`fixed`、`static`
  * float
    - clear属性指定：一个元素是紧挨着前面的浮动元素，还是必须移动到它们的下面（浮动被清除）。
      - 当应用于非浮动块时，它将元素的边框边界移动到所有相关浮动元素外边界的下方。这个行为作用时会导致外边距折叠不起作用。
      - 当应用于浮动元素时，它将元素的外边界移动到所有相关的浮动元素外边界的下方。这会影响后面浮动元素的布局，后面的浮动元素的位置无法高于它之前的元素。
      - 语法： `none | left | right | both | inline-start | inline-end`

##表格

##媒体
  * @media
  * @page
