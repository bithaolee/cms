一、栅格
	1.固定栅格：（940px宽）
		1.1 栅格数小于12，一行的栅格总数超过12列，则多余的自动挤到下一行
			<div class="row">
				<div class="span4">4个栅格</div>
				<div class="span8">8个栅格</div>
			</div>
		1.2 嵌套栅格,子栅格数之和必须等于父栅格数
			<div class="row">
				<div class="span4">4个栅格
					<div class="row">
						<div class="span1">1个栅格</div>
						<div class="span3">3个栅格</div>
					</div>
				</div>
				<div class="span8">8个栅格</div>
			</div>
		1.3 栅格偏移
			<div class="row">
				<div class="span4 class="offset2">4个栅格,并向有偏移2个栅格宽</div>
				<div class="span8">8个栅格</div>
			</div>

	2.流动栅格（class="row-fluid"宽度自适应，按比例来切分成12个栅格，基本的操作与上面的固定栅格一样，在处理嵌套栅格时，子栅格数之和一定等于12）
		嵌套栅格：
			<div class="row-fluid">
				<div class="span4">4个栅格
					<div class="row-fluid">
						<div class="span3">1个栅格</div>
						<div class="span9">3个栅格</div>
					</div>
				</div>
				<div class="span8">8个栅格</div>
			</div>

	3.容器(class="container" or class="container-fluid")
		3.1 940px的居中的容器
			<div class="container">
				<div class="row">
					<div class="span4">4个栅格</div>
					<div class="span8">8个栅格</div>
				</div>
			</div>
		3.2 自适应宽度的容器
			<div class="container-fluid">
				<div class="row-fluid">
				    <div class="span2">
				      <!--Sidebar content-->
				    </div>
				    <div class="span10">
				      <!--Body content-->
				    </div>
			  	</div>
			</div>


二、Bootstrap的基本样式
	1. 排版
		1.1 <h1></h1> -- ... --> <h6></h6>

		1.2 Bootstrap定义的全局 font-size 是 14px，line-height 是 20px。这些样式应用到了 <body> 和所有的段落上。另外，对 <p> (段落)还定义了1/2行高(默认为10px)的底部外边距(margin)属性。

		1.3 
			1.3.1 
				<p class="lead">通过添加 .lead 让段落突出显示 </p>
				<p class="text-left">文本左对齐</p>
				<p class="text-center">文本居中</p>
				<p class="text-right">文本右对齐</p>

				//强调类
				<p class="muted">灰色文本</p>
				<p class="text-warning">黄色警告文本</p>
				<p class="text-error">红色错误文本</p>
				<p class="text-info">蓝色信息文本</p>
				<p class="text-success">绿色成功文本</p>

		1.4 
			<small>缩小</small>
			<strong>加粗</strong>
			<em>斜体</em>

			<abbr title="attribute">缩略语</abbr> 
				当鼠标悬停在缩写和缩写词上时就会显示完整内容，Bootstrap实现了对HTML <abbr>元素的增强样式。缩略语元素带有title属性，外观表现为带有较浅的虚线框，鼠标移至上面时会变成带有“问号”的指针。

		1.5 地址
			<address>
			  <strong>Twitter, Inc.</strong><br>
			  795 Folsom Ave, Suite 600<br>
			  San Francisco, CA 94107<br>
			  <abbr title="Phone">P:</abbr> (123) 456-7890
			</address>
			 
			<address>
			  <strong>Full Name</strong><br>
			  <a href="mailto:#">first.last@example.com</a>
			</address>

		1.6 引用
			<blockquote>我是引用</blockquote>
			<blockquote><p>我是引用</p></blockquote>
			使用.pull-right类，可以让引用展现出向右侧移动、对齐的效果。
				<blockquote class="pull-right"><p>我是引用</p></blockquote>

			添加<small>标签来注明引用来源。来源名称可以放在<cite> 标签里面。
				<blockquote>
				  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
				  <small>Someone famous <cite title="Source Title">Source Title</cite></small>
				</blockquote>


		1.7 列表
			1.7.1 有序列表和无序列表保持html本来的语法
			1.7.2 无样式的列表(移除了默认的list-style，并左侧填充列表(只对直接子节点项有效)。)
				<ul class="unstyle">
					<li>...</li>
				</ul>
			1.7.3 使用inline-block让列表项水平排列一行，同时每项都有少量的内补（padding）。
				<ul class="inline">
				  <li>...</li>
				</ul>

			1.7.4 对一个列表（条目）进行关联描述。****
				<dl>
				  <dt>...</dt>
				  <dd>...</dd>
				</dl>

				水平描述:使<dl>中的每个条目和其描述一对一水平显示。
				<dl class="dl-horizontal">
				  <dt>...</dt>
				  <dd>...</dd>
				</dl>


	2. 代码
		//TODO

	3. 表格
		<table class="table">
		  …
		</table>

	4. 表单
		......

	5. 按钮
		任何赋予.btn类的页面元素都会显示按钮样式。不过，通常是用于更好的表现<a> 和 <button> 页面元素。
			按钮	class=""			描述
			默认	btn					带渐变的标准灰色按钮
			主要	btn btn-primary		提供额外的视觉感, 可在一系列的按钮中指出主要操作
			信息	btn btn-info		默认样式的替代样式
			成功	btn btn-success		表示成功或积极的动作
			警告	btn btn-warning		提醒应该谨慎采取这个动作
			危险	btn btn-danger		表示这个动作危险或存在危险
			反向	btn btn-inverse		备用的暗灰色按钮，不依赖于语义和用途
			链接	btn btn-link		简化一个按钮, 使它看起来像一个链接，同时保持按钮的行为

		想使用更大或更小的按钮吗？添加.btn-large、.btn-small 或 .btn-mini即可改变按钮大小。
		通过添加.btn-block类，可使按钮变为块级元素，同时会填充整个父级元素。（例如显示一个很长条形的按钮）
		给<a>元素添加.disabled类。



















