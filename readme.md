# deepcss

## 基础回顾

### 1.层叠，优先级和继承

- 层叠

	- 层叠三步骤之一：
1.样式表的来源

		- 用户代理样式

			- 就是默认样式

		- !important声明

			- 优先级顺序：
(1) 作者的！important
(2) 作者
(3) 用户代理

	- 层叠三步骤之二：
2.选择器优先级

		- 选择器优先级

			- 总的来说：
ID > 类 > 标签
			- 子主题 2

		- 准确描述

			- 如果选择器的ID数量更多，则它会胜出
			-  如果ID数量一致，那么拥有最多类的选择器胜出
			- 如果以上两次比较都一致，那么拥有最多标签名的选择器胜出
			- 如果以上都都都一致， 
那么按照源码的顺序由近及远来
			- 重要的补充

				- 伪类选择器（如：hover）
和属性选择器（如[type="input"]）
与一个类选择器的优先级相同
				- 通用选择器（＊）和组合器（>、+、~）对优先级没有影响

		- 优先级标记

			- 一个常用的表示优先级的方式是用数值形式来标记
			- 例如1个ID, 2个class, 3个标签，那么优先级就为 :  1,2,3 

		- 关于优先级的思考

	- 层叠三步骤之三：
3.源码顺序

		- 由近及远
链接样式和源码顺序

			- 后声明的比先声明的更优先

		- 层叠值

			- 在层叠中胜出的那个声明，
就是一个层叠值
			- 作为层叠结果，应用到一个元素上的特定属性的值

	- 两条经验法则

		- 在选择器中不要使用ID
		- 不要使用     !important

- 继承

	- 如果一个元素的某个属性没有层叠值，
则可能会继承某个祖先元素的值
	- 但不是所有的层叠值都能被继承
	- 能被继承的层叠值

		- 主要是文本

			- color、font、font-family、font-size、font-weight、font-variant、font-style、line-height、letter-spacing、text-align、text-indent、text-transform、white-space以及word-spacing

		- 列表属性也能被继承

			- list-style、list-style-type、list-style-position以及list-style-image

		- 表格的边框属性也能继承
注意这里不是div

			- border-collapse和border-spacing

- 特殊值

	- inherit关键字

		- 用继承代替一个层叠值
		- 使用inherit关键字强制继承一个通常不会被继承的属性，比如边框和内边距

	- initial关键字

		- 有时，你需要撤销作用于某个元素的样式。这可以用initial关键字来实现。
		- 每一个CSS属性都有初始（默认）值。如果将initial值赋给某个属性，那么就会有效地将其重置为默认值
		- 小心auto值

			- auto，其实就是浏览器默认层叠值
			- auto 对于某些元素来说，不合法

- 简写属性
简写属性是用于同时给多个属性赋值的属性。

	- 常见

		- font

			- 简写的顺序：
font-style、font-weight、font-size、font-height、font-family

		- background

			- 简写的顺序
border-width、border-style以及border-color

		- border

			-  border是border-width、border-style以及border-color的简写属性

		- border-width

			- border-width是上、右、下、左四个边框宽度的简写属性

	- 简写属性带来的问题

		- 简写属性会默默覆盖其他样式：
被简写的属性如果被省略了，缺省属性则会隐式的被定义为 浏览器默认值

	- 理解简写值的顺序

		- 1．上、右、下、左
		- 2．水平、垂直
如果只写了2个属性键值

- 总结

### 2.相对单位

### 3.box model

## 布局

### 4.float

### 5.flex

### 6.网格

### 8.响应式

### 7.定位和层叠上下文

## 工程化

### 9.模块化

### 10.模式库

## 动效和过渡

### 14.过渡

### 15.变换

### 16.动画

## 高级话题/设计感

### 11.背景，阴影和混合

### 12.对比，颜色和间距

### 13.排版

*XMind - Trial Version*