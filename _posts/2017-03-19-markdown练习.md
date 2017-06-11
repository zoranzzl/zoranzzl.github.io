---
layout: post
title:  "Markdown 练习"
categories: jekyll update
---


            
那就先从段首缩进说起吧。原因是认真看完 Markdowm 的文档满心激动地想写文章的时候，发现 Markdown 本身不支持段首缩进，只好去查资料。（但是写着写着发现段首缩进不好看就都去掉了）


### 一、段首缩进 
实现 Markdown 的段首缩进目前似乎有三种方法：

*	将输入法切换到全角模式下（一般是按`shift` + `space`）输入两个空格就可以了
*	手动输入空格 `&emsp` `&ensp` `&nbsp`
*	修改 CSS

第一种看起来是最方便的一种，在此就不再多说；第二种的话，亲测两个全角空格 `&emsp` 的长度等于两个汉字的长度（后来查资料说是在不同浏览器中宽度各异）；第三种方法还没学会，以后有机会再更。

### 二、标题 ##

#### 1. 类 Setext 
类 Setext 形式是用底线的形式，利用 `=` （最高阶标题）和 `-`（第二阶标题）
	
	最高阶标题
	=========
	第二阶标题
	---------

效果是这样的：

![head_example](https://raw.githubusercontent.com/chriszhuge/chriszhuge.github.io/master/pictures/head_example.png)

#### 2.类 Atx
在行首插入 1 到 6 个`#`
	
	# 一级标题
	## 二级标题
	### 三级标题
	#### 四级标题
	##### 五级标题
	###### 六级标题

效果是：

![head_example2](https://github.com/chriszhuge/chriszhuge.github.io/blob/master/pictures/head_example2.png?raw=true)

要记得 `#` 和文本中间一定要有空格，虽然没有空格的话在 MarkdownPad 2 中是正常显示的，但是在浏览器中是不解析的。

当然也可以这样写
	
	# 一级标题 #
	## 二级标题 ##

这种似乎看起来更好看一些？但效果都是一样的。

### 三、换行
刚写 Markdown 的时候感觉还挺崩溃，欸我明明敲了回车了啊为什么不换行啊，欸再敲一个为啥就换行了。
  
文档是这样说的
>一个 Markdown 段落是由一个或多个连续的文本行组成，它的前后要有一个以上的空行（空行的定义是显示上看起来像是空的，便会被视为空行。比方说，若某一行只包含空格和制表符，则该行也会被视为空行）。普通段落不该用空格或制表符来缩进。

所以想要换行的话可以敲 `<br/>`,这个效果和自动换行的行间距是一样的。当然也可以敲两个回车，这样中间就会有一个空行。（随手敲回车可能是个好习惯...）

### 四、区块引用

Markdown 标记区块引用是使用类似 email 中用 `>` 的引用方式。

你可以这样写

	>aaaaaaaa
	>
	>bbbbbbbb
	>
	>>cccc
	>
	>>>ddd
	

预览图是：

![block_example](https://github.com/chriszhuge/chriszhuge.github.io/blob/master/pictures/block_example.png?raw=true)

一般引用的时候使用这个，不同数量的 `>` 可以代表多层的引用。Markdown 也允许你偷懒只在整个段落的第一行最前面加上 `>` 不再多言。还是觉得回车什么的确实是很麻烦啊，有的时候写引用的时候常常会忘记。

### 五、代码区块

一个制表符 `Tab` 或四个空格就可以建立代码区块：

		int main(){
			printf("hello world");	
		}

预览图：

![code_example](https://github.com/chriszhuge/chriszhuge.github.io/blob/master/pictures/code_example.png?raw=true)

MarkDownPad 2支持选中一块代码插入制表符，为该块代码建立代码区块：

![insert_code](https://github.com/chriszhuge/chriszhuge.github.io/blob/master/pictures/insert_code.png?raw=true)

但是亲测不好用，因为代码段中本来就存在了大量的制表符，用这个反而会破坏代码结构，降低可读性。

那么当我们有大量代码的时候，难道要一行一行加制表符吗？更好用的方式是：

	```java
	public class Main{
	 	public static void main(String[] args){
        	...
	    	}
	}
	```

将会显示为：

	public class Main{
	 	public static void main(String[] args){
        	...
	    	}
	}

### 六、列表

讲起来不好讲，直接看预览图吧：

![list_example](https://github.com/chriszhuge/chriszhuge.github.io/blob/master/pictures/list_example.png?raw=true)

代码是这样的：

	*	一
	-	二
	+	三

这里 `*` `+` `-`效果都是一样的，也可以用数字 `1.` `2.` 等等，但效果都是一样的。

### 七、链接

[an example](http://example.com/ "Title")

[This link](http://example.net/)


### 八、图片


	





----------



用 Markdown 写中文文档唯一累心的一点就是要不断的大小写转换，`Shift` 键都要被按坏了。QAQ

### 未完待续
