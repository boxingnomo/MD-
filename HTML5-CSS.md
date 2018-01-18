# 探索：HTML5/CSS

---

- HTML&CSS
- HTML5&CSS3

  ---

## HTML与CSS基础

 **HTML基础部分：** 

基础；超文本标记语言（英语： **HyperText Markup Language** ，简称：HTML）是一种用于创建网页的标准标记语言。可以使用 HTML 来建立自己的 WEB 站点。

HTML 运行在浏览器上，由浏览器来解析。

基本结构；

    <!DOCTYPE html>
    <html>
    <head>
    <meta charset="utf-8">
    <title>菜鸟教程(runoob.com)</title>
    </head>
    <body>
    <h1>我的第一个标题</h1>
    <p>我的第一个段落。</p>
    </body>
    </html>

- 解决 **中文乱码问题** ；

  对于中文网页需要使用 <meta charset="utf-8">

- 关于HTML **元素** ：
  1. 标记尽量使用 **小写** 
  1. 标记都要 **成对出现** 
- 关于HTML元素的 **属性** ：
  1. 属性一般描述于 **开始标签** 
  1. 属性总是以 **名称/值对** 的形式出现，比如：name="value"。
  1. 元素的必备属性：
    - class属性 为元素定义一个或多个classname (元素与classname之间是 **”多对多“** 的关系
    - id属性 为元素定义唯一的idname(元素与 **id** name之间是 **”一对一的关系“** 的关系)
    - style属性 规定元素的行内样式（inline style）
    - title属性；描述了元素的额外信息 (作为工具条使用)

---

 **CSS基础部分** ：

基础：CSS 指层叠样式表 (英文； **Cascading Style Sheets** ，简称；CSS)。与HTML结合使用，解决内容和表现分离的问题。

外部样式表通常存储在 CSS 文件中；多个样式定义可层叠为一

语法：CSS 规则由两个主要的部分构成：

 **<选择器，一条或多条声明** >

![](https://static.notion-static.com/3042b7eaa67e4a81af9a5cd6233aaa32/selector.gif)

 **选择器** 通常是您需要改变样式的 HTML 元素。

 **声明** 由一个属性和一个值组成。声明语句以用分号结束。

属性（property）是您希望设置的样式属性（style attribute）。

每个属性有一个值。属性和值被冒号分开。

 **注释** ：/**/

## **块级元素block element与行内元素inline element**

1. 关于行内元素和块状元素的说明

  根据CSS规范的规定，每一个网页元素都有一个display属性，用于确定该元素的类型。每一个元素都有默认的display属性值；比如div元素，它的默认display属性值为“block”，成为“块级”元素(block-level)；而span元素的默认display属性值为“inline”，称为“行内”元素。我们可以通过修改CSS中选择器的display属性来自定义修改元素的块级与行内属性。

  块级元素，就会自动占据一定矩形空间，可以通过设置高度、宽度、内外边距等属性，来调整的这个矩形的样子；像“span”“a”这样的行内元素，则没有自己的独立空间，它是依附于其他块级元素存在的，因此，对行内元素设置高度、宽度、内外边距等属性，都是无效的。

1. 行内、块状元素区别：

 (1)块级元素会独占一行，其宽度自动填满其父元素宽度。块级元素会换行往下排。

行内元素不会独占一行，相邻的行内元素会排列在同一行里，知道一行排不下，才会换行，其宽度随元素的内容而变化

 (2) 一般情况下，块级元素可以设置 width, height属性，行内元素设置width,  height无效

(注意：块级元素即使设置了宽度，仍然是独占一行的)

 (3)块级元素可以设置margin 和 padding.  行内元素的水平方向的padding-left,padding-right 都产生边距效果，但是竖直方向的padding-top,padding-bottom都不会产生边距效果。（水平方向有效，竖直方向无效）

---

## HTML语法部分：（包括有用却未掌握部分）

1. 文本格式化：
  - <sub> 	定义下标字
  - <sup> 	定义上标字
  - <del> 	定义删除字
  - <ins> 	定义更正字
  - <pre> 	定义预格式文本 对缩进 空格可以识别
  - <blockquote> 	定义引用缩进
  - <q> 	引号标记
1. 图片链接
  - <a href="url"><img src=""></a>
1.  <head> 中的内嵌元素：<title>, <base>,<link>,<style>, <meta>, , <script>, <noscript>.
  - **<title>** 标签定义了 **文档的标题** 。

    用途：定义在浏览器工具栏的标题；当网页添加到收藏夹时；示在收藏夹中的标题显示在搜索引擎结果页面的标题。

  - **<base>** 标签描述了基本的链接地址/链接目标，该标签作为HTML文档中所有的链接标签的 **默认链接** 。<base href="url">
  - **<link>** 标签定义了文档与外部资源之间的关系。常用于 **链接到样式表** :
  - **<style>** 标签定义了HTML文档的样式文件引用地址.可以直接添加样式来 **渲染 HTML 文档**
  - **<meta>** 标签提供了元数据.元数据也不显示在页面上，但会被浏览器解析。

        为搜索引擎定义关键词
        <meta name="keywords" content="HTML, CSS, XML, XHTML, JavaScript">
        为网页定义描述内容:
        <meta name="description" content="免费 Web & 编程 教程">
        定义网页作者:
        <meta name="author" content="Runoob">
        每30秒中刷新当前页面:
        <meta http-equiv="refresh" content="30">

  - **<script>** 与<noscript>标记，Script用于加载JavaScript脚本。noscript 元素用来定义在脚本未被执行时的替代内容（文本）

        <script language="JavaScript 1.2" type="text/JavaScript">脚本片段</script>

        <script language="JavaScript 1.2" type="text/JavaScript" src=".js">不存在脚本片段</script>

    无法识别 <script> 标签的浏览器会把标签的内容显示到页面上。为了避免浏览器这样做，您应当在注释标签中隐藏脚本。<!— ... //—>

    老式的（无法识别 <script> 标签的）浏览器会忽略注释，这样就不会把标签的内容写到页面上。

    而新式的浏览器则懂得执行这些脚本，即使它们被包围在注释标签中！

        <script>
         **<!—** function displayMsg(){alert("Hello World!")}
        // **—>
        ** </script>