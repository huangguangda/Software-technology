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





















































