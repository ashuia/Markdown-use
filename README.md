# Markdown-use
## 1、标题
在行首插入 1 到 6 个 # ，对应到标题 1 到 6 阶，井号后加一个空格，例如
>  # 这是 H1

>  ## 这是 H2

>  ###### 这是 H6
## 2、列表
无序列表使用星号、加号或是减号作为列表标记
> *   Red
> *   Green
> *   Blue

等同于：
> +   Red
> +   Green
> +   Blue
也等同于：
>-   Red
>-   Green
>-   Blue
有序列表则使用数字接着一个英文句点：
>1.  Bird
>2.  McHale
>3.  Parish
## 3、引用
先断好行，然后在每行的最前面加上 > 
Markdown 也允许你偷懒只在整个段落的第一行最前面加上 > 
区块引用可以嵌套（例如：引用内的引用），只要根据层次加上不同数量的 > 
引用的区块内也可以使用其他的 Markdown 语法，包括标题、列表、代码区块等。
## 4、分隔线
你可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。
>* * *
>***
>*****
>- - -
## 5、链接
链接为：[]()
Markdown 支持两种形式的链接语法： 行内式和参考式两种形式。
不管是哪一种，链接文字都是用 [方括号] 来标记。
要建立一个行内式的链接，只要在方块括号后面紧接着圆括号并插入网址链接即可，如果你还想要加上链接的 title 文字，只要在网址后面，用双引号把 title 文字包起来即可，例如：
>This is [an example](http://example.com/ "Title") inline link.
>[This link](http://example.net/) has no title attribute.

参考式的链接是在链接文字的括号后面再接上另一个方括号，而在第二个方括号里面要填入用以辨识链接的标记：
>This is [an example][id] reference-style link.

你也可以选择性地在两个方括号中间加上一个空格：
>This is [an example] [id] reference-style link.

接着，在文件的任意处，你可以把这个标记的链接内容定义出来：
>[id]: http://example.com/  "Optional Title Here"

链接内容定义的形式为：
* 方括号（前面可以选择性地加上至多三个空格来缩进），里面输入链接文字
* 接着一个冒号
* 接着一个以上的空格或制表符
* 接着链接的网址
* 选择性地接着 title 内容，可以用单引号、双引号或是括弧包着

下面这三种链接的定义都是相同：
>[foo]: http://example.com/  "Optional Title Here"
>[foo]: http://example.com/  'Optional Title Here'
>[foo]: http://example.com/  (Optional Title Here)
## 6、代码
如果要标记一小段行内代码，你可以用反引号把它包起来

> Use the `printf()` function.
会产生：
> <p>Use the <code>printf()</code> function.</p>

如果要在代码区段内插入反引号，你可以用多个反引号来开启和结束代码区段

## 7、图片
很明显地，要在纯文字应用中设计一个「自然」的语法来插入图片是有一定难度的。
Markdown 使用一种和链接很相似的语法来标记图片，同样也允许两种样式： 行内式和参考式。
行内式的图片语法看起来像是：
>  ![Alt text](/path/to/img.jpg)
>  ![Alt text](/path/to/img.jpg "Optional title")
详细叙述如下：
* 一个惊叹号 !
* 接着一个方括号，里面放上图片的替代文字
* 接着一个普通括号，里面放上图片的网址，最后还可以用引号包住并加上 选择性的 'title' 文字。

 参考式的图片语法则长得像这样：
>  ![Alt text][id]
「id」是图片参考的名称，图片参考的定义方式则和连结参考一样：
> [id]: url/to/image  "Optional title attribute"
到目前为止， Markdown 还没有办法指定图片的宽高，如果你需要的话，你可以使用普通的 <img> 标签。
