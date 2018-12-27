css.md

通过使用 CSS 我们可以大大提升网页开发的工作效率！

在我们的 CSS 教程中，您会学到如何使用 CSS 同时控制多重网页的样式和布局。

CSS 简介
你需要具备的知识
在继续学习之前，你需要对下面的知识有基本的了解：

HTML / XHTML


## 什么是 CSS?
CSS 指层叠样式表 (Cascading Style Sheets)
样式定义如何显示 HTML 元素
样式通常存储在样式表中
把样式添加到 HTML 4.0 中，是为了解决内容与表现分离的问题
外部样式表可以极大提高工作效率
外部样式表通常存储在 CSS 文件中
多个样式定义可层叠为一

## CSS 实例
CSS 规则由两个主要的部分构成：选择器，以及一条或多条声明:

## CSS 实例
CSS声明总是以分号(;)结束，声明组以大括号({})括起来:

```
p {color:red;text-align:center;}
```

CSS 注释
注释是用来解释你的代码，并且可以随意编辑它，浏览器会忽略它。

CSS注释以 "/*" 开始, 以 "*/" 结束, 实例如下:

/*这是个注释*/
```
p
{
text-align:center;
/*这是另一个注释*/
color:black;
font-family:arial;
}
```

CSS Id 和 Class

id 和 class 选择器
如果你要在HTML元素中设置CSS样式，你需要在元素中设置"id" 和 "class"选择器。

id 选择器
id 选择器可以为标有特定 id 的 HTML 元素指定特定的样式。

HTML元素以id属性来设置id选择器,CSS 中 id 选择器以 "#" 来定义。

以下的样式规则应用于元素属性 id="para1":

实例
#para1
{
    text-align:center;
    color:red;
}

```
@Controller
@EnableAutoConfiguration
public class SampleController {
 @RequestMapping("/")
 @ResponseBody
 String home() {
   return "Hello World!";
 }
}
```

在以下实例中, 所有的 p 元素使用 class="center" 让该元素的文本居中:

```
p.center {text-align:center;}
```

## CSS 创建

#### 如何插入样式表

插入样式表的方法有三种:

- 外部样式表(External style sheet)
- 内部样式表(Internal style sheet)
- 内联样式(Inline style)

#### 外部样式表

当样式需要应用于很多页面时，外部样式表将是理想的选择。在使用外部样式表的情况下，你可以通过改变一个文件来改变整个站点的外观。每个页面使用 <link> 标签链接到样式表。 <link> 标签在（文档的）头部：

```
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```

#### 内部样式表

当单个文档需要特殊的样式时，就应该使用内部样式表。你可以使用 <style> 标签在文档头部定义内部样式表，就像这样:

```
<head>
<style>
hr {color:sienna;}
p {margin-left:20px;}
body {background-image:url("images/back40.gif");}
</style>
</head>
```

#### 内联样式
由于要将表现和内容混杂在一起，内联样式会损失掉样式表的许多优势。请慎用这种方法，例如当样式仅需要在一个元素上应用一次时。

要使用内联样式，你需要在相关的标签内使用样式（style）属性。Style 属性可以包含任何 CSS 属性。本例展示如何改变段落的颜色和左外边距：
```
<p style="color:sienna;margin-left:20px">这是一个段落。</p>
```

#### 多重样式
如果某些属性在不同的样式表中被同样的选择器定义，那么属性值将从更具体的样式表中被继承过来。 

例如，外部样式表拥有针对 h3 选择器的三个属性：
```
h3
{
    color:red;
    text-align:left;
    font-size:8pt;
}
```
而内部样式表拥有针对 h3 选择器的两个属性：
```
h3
{
    text-align:right;
    font-size:20pt;
}
```
假如拥有内部样式表的这个页面同时与外部样式表链接，那么 h3 得到的样式是：
```
color:red;
text-align:right;
font-size:20pt;	
```
即颜色属性将被继承于外部样式表，而文字排列（text-alignment）和字体尺寸（font-size）会被内部样式表中的规则取代。


#### 多重样式优先级
样式表允许以多种方式规定样式信息。样式可以规定在单个的 HTML 元素中，在 HTML 页的头元素中，或在一个外部的 CSS 文件中。甚至可以在同一个 HTML 文档内部引用多个外部样式表。

一般情况下，优先级如下：

内联样式）Inline style > （内部样式）Internal style sheet >（外部样式）External style sheet > 浏览器默认样式
```
<head>
    <!-- 外部样式 style.css -->
    <link rel="stylesheet" type="text/css" href="style.css"/>
    <!-- 设置：h3{color:blue;} -->
    <style type="text/css">
      /* 内部样式 */
      h3{color:green;}
    </style>
</head>
<body>
    <h3>测试！</h3>
</body>
```
注意：如果外部样式放在内部样式的后面，则外部样式将覆盖内部样式。


多重样式优先级深入概念
优先级是浏览器是通过判断哪些属性值与元素最相关以决定并应用到该元素上的。优先级仅由选择器组成的匹配规则决定的。

优先级就是分配给指定的CSS声明的一个权重，它由匹配的选择器中的每一种选择器类型的数值决定。

优先级顺序
下列是一份优先级逐级增加的选择器列表：
```
通用选择器（*）
元素(类型)选择器
类选择器
属性选择器
伪类
ID 选择器
内联样式
!important 规则例外
当 !important 规则被应用在一个样式声明中时,该样式声明会覆盖CSS中任何其他的声明, 无论它处在声明列表中的哪里. 尽管如此, !important规则还是与优先级毫无关系.使用 !important 不是一个好习惯，因为它改变了你样式表本来的级联规则，从而使其难以调试。
```
一些经验法则：

Always 要优化考虑使用样式规则的优先级来解决问题而不是 !important
Only 只在需要覆盖全站或外部 css（例如引用的 ExtJs 或者 YUI ）的特定页面中使用 !important
Never 永远不要在全站范围的 css 上使用 !important
Never 永远不要在你的插件中使用 !important
权重计算:


解释：
```
 1. 内联样式表的权值最高 1000；
 2. ID 选择器的权值为 100
 3. Class 类选择器的权值为 10
 4. HTML 标签选择器的权值为 1
利用选择器的权值进行计算比较，em 显示蓝色，示例如下：https://c.runoob.com/codedemo/3048
```
CSS 优先级法则：
 A 选择器都有一个权值，权值越大越优先；
 B 当权值相等时，后出现的样式表设置要优于先出现的样式表设置；
 C 创作者的规则高于浏览者：即网页编写者设置的CSS 样式的优先权高于浏览器所设置的样式；
 D 继承的CSS 样式不如后来指定的CSS 样式；
 E 在同一组属性设置中标有“!important”规则的优先级最大；示例如下：https://c.runoob.com/codedemo/3049 
结果：在Firefox 下显示为蓝色；在IE 6 下显示为红色；










































