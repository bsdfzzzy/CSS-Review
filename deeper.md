#CSS进阶

##目录
  * [CSS渐变](#css渐变)
  * [优先级策略](#优先级策略)

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
