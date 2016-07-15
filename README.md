# CSS-Review
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
    - /* style | variant | weight | size/line-height | family */     font: italic small-caps bolder 16px/3 cursive;

##颜色


##内容


##列表


##盒模型


##布局


##表格


##媒体

