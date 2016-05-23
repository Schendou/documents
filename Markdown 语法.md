Markdown 语法说明
===

This is H2 title
---

###This is H3 title###

####The H4 title

#####the h5 title

###### the h6 title

#####HTML 内容
要制约的只有一些 HTML 区块元素――比如 &lt;div>、&lt;table>、&lt;pre>、&lt;p> 等标签，必须在前后加上空行与其它内容区隔开，还要求它们的开始标签与结尾标签不能用制表符或空格来缩进。

*e.g*  这是一个表格。

<table>
    <tr>
        <td>*Foo*</td>
        <td>Foo</td>
        <td>Foo</td>
    </tr>
    <tr>
        <td>Foo</td>
        <td>Foo</td>
        <td>Foo</td>
    </tr>
</table>

**注意** 

* 在 HTML 区块标签间的 Markdown 格式语法将不会被处理。比如，你在 HTML 区块内使用 Markdown 样式的强调会没有效果。
* Markdown 语法在 HTML 区段标签间是有效的.
	* e.g <a href="http://wowubuntu.com/markdown/">*Markdown语法说明*</a>

&copy; Tech

*   一列表项包含一个列表区块：
		
		<代码写在这>
		
* 在行首出现数字-句点-空白，要避免这样的状况，你可以在句点前面加上反斜杠。

1986\. What a great season.


#####区块引用 Blockquotes
Markdown 标记区块引用是使用类似 email 中用 > 的引用方式。如果你还熟悉在 email 信件中的引言部分，你就知道怎么在 Markdown 文件中建立一个区块引用，那会看起来像是你自己先断好行，然后在每行的最前面加上 *>* 
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
> 
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.

Markdown 也允许你偷懒只在整个段落的第一行最前面加上 *>*
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
id sem consectetuer libero luctus adipiscing. 

#####分隔线
在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线：
* * *

***

*****

- - -

---------------------------------------
###区段元素
#####链接
Markdown 支持两种形式的链接语法： 行内式和参考式两种形式。

不管是哪一种，链接文字都是用 [方括号] 来标记。

要建立一个行内式的链接，只要在方块括号后面紧接着圆括号并插入网址链接即可，如果你还想要加上链接的 title 文字，只要在网址后面，用双引号把 title 文字包起来即可，e.g：

* This is [an example](http://example.com/ "Title") inline link.

* [This link](http://example.net/) has no title attribute.

* [Markdown语法说明](http://wowubuntu.com/markdown/)

* 如果你是要链接到同样主机的资源，你可以使用相对路径：

	See my [About](/about/) page for details.
	
* [Google][]
[Google]: http://google.com/

* 下面是一个参考式链接的范例：
	* I get 10 times more traffic from [Google] [1] than from
[Yahoo] [2] or [MSN] [3].

  [1]: http://google.com/        "Google"
  [2]: http://search.yahoo.com/  "Yahoo Search"
  [3]: http://search.msn.com/    "MSN Search"
  
* 链接名称的方式
	* I get 10 times more traffic from [Google][] than from
[Yahoo][] or [MSN][].

  [google]: http://google.com/        "Google"
  [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
  [msn]:    http://search.msn.com/    "MSN Search" 

#####强调

* Markdown 使用星号（*）和底线（_）作为标记强调字词的符号，被 * 或 _ 包围的字词会被转成用 <em> 标签包围，用两个 * 或 _ 包起来的话，则会被转成 &lt;strong>，例如：

	* *single asterisks*

	* _single underscores_

	* **double asterisks**

	* __double underscores__

* 强调也可以直接插在文字中间：

	* un*frigging*believable

* 但是如果你的 * 和 _ 两边都有空白的话，它们就只会被当成普通的符号。
	* _ normal_

* 如果要在文字前后直接插入普通的星号或底线，你可以用反斜线：

	* \*this text is surrounded by literal asterisks\*
	
#####代码

* 如果要标记一小段行内代码，你可以用反引号把它包起来（`），例如：

	* Use the `printf()` function.

* 在代码区段内，& 和尖括号都会被自动地转成 HTML 实体，这使得插入 HTML 原始码变得很容易，Markdown 会把下面这段：

	* Please don't use any `<blink>` tags.
* 你也可以这样写：

	* `&#8212;` is the decimal-encoded equivalent of `&mdash;`.
	
#####图片

Markdown 使用一种和链接很相似的语法来标记图片，同样也允许两种样式： 行内式和参考式。

* 行内式
	* 一个惊叹号 !
	* 接着一个方括号，里面放上图片的替代文字
	* 接着一个普通括号，里面放上图片的网址，最后还可以用引号包住并加上 选择性的 'title' 文字。
		* ![Alt text](/path/to/img.jpg)

		* ![Alt text](/path/to/img.jpg "Optional title")
	* 到目前为止， Markdown 还没有办法指定图片的宽高，如果你需要的话，你可以使用普通的 <img> 标签。
		
 		* <img src="/Users/long/Pictures/dragonfly.JPG"  width="480" height="320"/>
 		
 ***
###其它
#####自动链接

* Markdown 支持以比较简短的自动链接形式来处理网址和电子邮件信箱，只要是用尖括号包起来， Markdown 就会自动把它转成链接。一般网址的链接文字就和链接地址一样，e.g:
	* <http://example.com/>

* 邮址的自动链接也很类似，只是 Markdown 会先做一个编码转换的过程，把文字字符转成 16 进位码的 HTML 实体，这样的格式可以糊弄一些不好的邮址收集机器人，e.g：
	* <schendou@163.com>

#####反斜杠

Markdown 可以利用反斜杠来插入一些在语法中有其它意义的符号，例如：如果你想要用星号加在文字旁边的方式来做出强调效果（但不用 <em> 标签），你可以在星号的前面加上反斜杠：

\*literal asterisks\*

- Markdown 支持以下这些符号前面加上反斜杠来帮助插入普通的符号：

		\   反斜线
		`   反引号
		*   星号
		_   底线
		{}  花括号
		[]  方括号
		()  括弧
		#   井字号
		+   加号
		-   减号
		.   英文句点
		!   惊叹号
