#CSS进阶

##目录
  * [CSS渐变](#css渐变)
  * [优先级策略](#优先级策略)
  * [外边距塌陷](#外边距塌陷)
  * [块格式化上下文](#块格式化上下文)
##CSS渐变
  * 线性渐变 `linear-gradient`
  * 径向渐变 `radial-gradient`

##优先级策略
  假设优先级最高分9999，那么带有!important的元素优先级最高，style有1000分，id选择器有100分，类选择器10分，元素选择器1分，在计算时子元素优先级分数会加上父元素的一起算，举例如下：
  css代码为：
	
	body{
		color: write;	
	}
	#box{
		color: blue;	
	}
  	.box{
		color: red;	
	}
	.boxs{
		color: black !important;	
	}
	p{
		color: green;
	}
  html代码为：
  	
	<!DOCTYPE html>
	<html>
	<head></head>
	<body>
		<div id="box"></div>
		<div class="box">
			<p></p>
			<div class="boxs" id="box"></div>
		</div>
		<p></p>
	</body>
	<html>
  如上结果，id为box没有class的权重为101,class为box没有id的权重为11,在div里的p权重为12,在div里的div权重最高因为有!important，忽略id的作用，最外面的p标签权重为2

##外边距塌陷
####毗邻兄弟元素
  * 毗邻的兄弟元素的外边距会塌陷（当靠后的元素 清除浮动 时除外）。
####父元素与第一个/最后一个子元素
  * 如果块元素的 margin-top 与它的第一个子元素的margin-top 之间没有 border、padding、inline content、 clearance 来分隔，或者块元素的 margin-bottom 与它的最后一个子元素的margin-bottom 之间没有 border、padding、inline content、height、min-height、 max-height 分隔，那么外边距会合并(塌陷)。子元素多余的外边距会被父元素的外边距截断。
####空块元素
  * 如果块元素的 margin-top 与 margin-bottom 之间没有 border、padding、inline content、height、min-height 来分隔，那么它的上下外边距将会合并。
####浮动 及 绝对定位 元素外边距不会合并。

##块格式化上下文
块格式化上下文是用于决定块盒子的布局及浮动相互影响的一个区域
下列情况将创建一个块格式化上下文：
* 根元素或其它包含它的元素
* 浮动 (元素的 float 不为 none)
* 绝对定位元素 (元素的 position 为 absolute 或 fixed)
* 行内块 inline-blocks (元素的 display: inline-block)
* 表格单元格 (元素的 display: table-cell，HTML表格单元格默认属性)
* 表格标题 (元素的 display: table-caption, HTML表格标题默认属性)
* overflow 的值不为 visible的元素
* 弹性盒子 flex boxes (元素的 display: flex 或 inline-flex)
