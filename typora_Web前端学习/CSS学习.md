# CSS

> CSS全名：Cascading Style Sheets，中文名：层叠样式表
> 用于定义网页样式和布局的样式表语言
> 通过CSS，可以指定页面中各个元素的颜色、字体、大小、间距、边框、背景等样式、从而实现更精确的页面设计

#### CSS语法

> CSS通常由选择器、属性和属性值组成，多个规则可以组合在一起，以便同时应用多个样式
>
> ```
> 选择器{
> 	属性1：属性值1；
> 	属性2：属性值2；
> }
> ```
>
> - 选择器的声明中可以写无数条属性
> - 声明的每一行属性，都需要以英文分号结尾
> - 声明中的所有属性和值都是以键值对这种形式出现的
>
> 实例：
>
> ```css
> /*这是一个p标签选择器*/
> p{
> 	color:blue;
> 	font-size:16px;
> }
> ```
>
> vscode中注释是Ctrl+/
>
> 意思是把p标签中的字体颜色改成蓝色，font-size是字体大小，改成16像素，整个页面中的p标签都会进行这一操作
>
> 内部样式表：把CSS放在HTML的头部`<head>`标签中
>
> 实例：#`<style>`标签就是CSS样式
>
> ```css
> <head>
>     <meta charset="UTF-8">
>     <meta name="viewport" content="width=device-width, initial-scale=1.0">
>     <title>CSS 导入方式</title>
> 
>     <style>
>         p {
>             color:blue;
>         	font-size:16px;
>         }
>     </style>
> </head>
> <body>
>     <p>这是应用了CSS样式的文本</p>
> </body>
> ```

> #### CSS三种导入方式
>
> 1. 内联样式（Inline Styles）：将CSS直接放在HTML元素的标签中
> 2. 内部样式表（Internal Stylesheet）：将CSS放在HTML文档中的`<head>`标签中
> 3. 外部样式表（External Stylesheet）：将CSS单独放在一个CSS文件中，在`<head>`标签中用另一个标签将CSS链接到HTML文档中，这种方式允许在多个页面上重复使用相同的样式
>
> 三种导入方式的优先级：内联样式>内部样式表>外部样式表

> 内联样式
>
> 实例：
>
> ```html
> <h1 style="color: red ;">这是一个一级标签,使用内联样式</h1>
> ```

> 内部样式表
>
> 实例：
>
> ```html
> <head>
>     <meta charset="UTF-8">
>     <meta name="viewport" content="width=device-width, initial-scale=1.0">
>     <title>CSS 导入方式</title>
>     <style>#内部样式
>         h2{
>             color:green;
>         }
>     </style>
> </head>
> <body>
>     <h2>这是一个二级标签，应用内部样式</h2>
> </body>
> ```

> 外部样式表
>
> 实例：
>
> ```html
> <head>
>     <meta charset="UTF-8">
>     <meta name="viewport" content="width=device-width, initial-scale=1.0">
>     <title>CSS 导入方式</title>
>     <link rel="stylesheet" href="./css/style.css">#嵌入在head中的CSS链接
> </head>
> <body>
>     <h3>这是一个三级标题，应用外部样式</h3>
> </body>
> ```
>
> `<link>`中的href属性是外部CSS文件的路径
>
> CSS文件：
>
> ```css
> h3{
>     color:violet;
> }
> ```

> #### 选择器
>
> 选择器是CSS中的关键部分，它允许你针对特定元素或一组元素定义样式
>
> - 元素选择器
> - 类选择器
> - ID选择器
> - 通用选择器
> - 子元素选择器
> - 后代选择器（包含选择器）
> - 并集选择器（兄弟选择器）
> - 伪类选择器

> 类选择器：
>
> ```html
> <head>
>     <meta charset="UTF-8">
>     <meta name="viewport" content="width=device-width, initial-scale=1.0">
>     <title>Document</title>
>     <style>
>         /*类选择器*/
>     	.content{
>         background-color: aqua;/*背景颜色*/
>         }
>         /*ID选择器*/
>    		#content{
>             font-size:larger;/*换字体大小*/
>         }
>         /*通用选择器*/
>         *{
>             font-family:'kaiti';/*字体换成楷体*/
>         }
>     </style>
> </head>
> <body>
>     <h1>不同类型的CSS选择器</h1>
>     <h3 class="content">这是一个类选择器示例</h3>
>     <h3 id="content">这是一个ID选择器示例</h3>
> </body>
> ```
>
> 创建标签，代码：
>
> ```text
> h3.content 带类的
> h3#id 带ID的 如：h3#content
> ```
>
> 通用选择器就是\*号后面接属性，代表对全体元素进行处理

> 子元素选择器就是嵌套在其他标签里的元素进行处理，示例：
>
> ```html
> <head>
>     <meta charset="UTF-8">
>     <meta name="viewport" content="width=device-width, initial-scale=1.0">
>     <title>Document</title>
>     <style>
>     /*子元素选择器*/
>     .father > .son{
>         color:black;
>     }
>     </style>
> </head>
> <body>
>     <div class="father">
>         <P class="SON">这是一个子元素选择器示例</P>
>     </div>
> </body>
> ```
>
> 后代选择器可以包含子元素选择器，因ID>类>标签名
>
> ```html
>    <head>
>     <meta charset="UTF-8">
>     <meta name="viewport" content="width=device-width, initial-scale=1.0">
>     <title>Document</title>
>     <style>
>     /*子元素选择器*/
>     .father > .son{
>         color:black;
>     }
>     /*后代选择器*/
>     .father p{
>         color:red;
>     }
>     </style>
> </head>
> <body>
>     <div class="father">
>         <P class="SON">这是一个子元素选择器示例</P>
>         <div >
>             <p class="grandson">这是一个后代选择器示例</p>
>         </div>
>     </div>
> </body>
> 
> ```

> 兄弟选择器会选择同一级别下的，紧跟在选中元素之后的第一个标签
>
> 示例：
>
> ```html
> <head>
>     <meta charset="UTF-8">
>     <meta name="viewport" content="width=device-width, initial-scale=1.0">
>     <title>Document</title>
>     <style>
>     /*并集/兄弟选择器*/
>     h3 + p {
>         color: white;
>     }
>     </style>
> </head>
> <body>
>     <p>这是一个普通的p标签</p>
>     <h3>这是一个相邻兄弟选择器示例</h3>
>     <p>这是另一个p标签</p>
> </body>
> ```
>
> 选择器改变了后面这个p的元素

> 伪类选择器
>
> 以冒号开开头，通常给用户交互文档结构或者其他条件下的元素应用样式
> 比如鼠标停留在词条上，发生颜色变化，这就可以用伪类选择器实现
>
> ```html
> <head>
>     <meta charset="UTF-8">
>     <meta name="viewport" content="width=device-width, initial-scale=1.0">
>     <title>Document</title>
>     <style>
>     /*伪类选择器*/
>     #element:hover{
>         background-color: brown;
>     }
>     </style>
> </head>
> <body>
>     <h3 id="element">这是一个伪类选择器示例</h3>
> </body>
> ```
>
> 伪类选择器的hover属性：鼠标悬停特效
> 选中第一个子元素：first-child
> 选中第n个子元素：nth-child()
> 链接的状态：active

> 伪元素选择器，创建一个虚拟元素，并且样式化，而不是选择实际存在的元素
> 通常以双冒号开头如：
>
> ::after——选中元素之前
> ::before——选中元素之后
> 插入虚拟的内容

> #### CSS 常用属性
>
> font是一个复合属性，可以用这一个属性来定义粗细、大小、字体等
> 示例：
>
> ```html
> <h1 style="font: bolder 50px 'KaiTi';">这是一个font复合属性的示例</h1>
> ```
>
> display属性可以将块级元素、行内元素和行内块元素相互转换
>
> 代码：
>
> ```html
> /*类选择器*/
> <head>
>     <style>
> .div-inline{
>         display: inline;/*块级元素转换成行内元素*/
>         background-color: aquamarine;
>     }
>     </style>
> </head>
> <div class="div-inline">这是一个转换成行内元素的div标签1</div>
> /*直接用内联样式也可以*/
> <div style="display：inline; background-color:aquamarine">
>     这是一个转换成行内元素的div标签2
> </div>
> ```
>
> 块级元素和行内块元素都是可以调整宽高的，（用width、height属性调整）
> 但是行内元素不行，它的宽高是由它所包含的内容所决定的
>
> display属性可以转换很多元素，需要自己慢慢了解

> #### CSS盒子模型
>
> 是CSS中一种常用于布局的基本概念，描述了文档中的每个元素都可以被看成是一个矩形的盒子，控制盒子模型可以精确的控制元素在页面中的位置和大小
>
> ![盒子模型](../3d9d5bbdcd28e536017cc77b9fa85920.png)

> 盒子模型相关属性
>
> |      属性名       |                             说明                             |
> | :---------------: | :----------------------------------------------------------: |
> |  内容（Content）  |             盒子包含的实际内容，比如文本、照片等             |
> | 内边距（Padding） | 围绕在内容的内部，是内容与边框之间的空间。可以使用`padding`属性来设置 |
> |  边框（Border）   | 围绕在内边距的外部，是盒子的边界。可以使用`border`属性来设置 |
> | 外边距（Margin）  | 围绕在边框的外部，是盒子与其他元素之间的空间。可以用`margin`属性来设置 |

> border、padding这些属性都是复合属性，可以设置很多属性
>
> border：边框大小  边框线条类型  边框颜色
> 代码：
>
> ```html
> <style>
>         .demo{
>             background-color: aqua;
>             display:inline-block;
>             border: 20px solid black;/*盒子边框属性*/
>         }
> 		.border-demo{
>             background-color: beige;
>             width: 50px;
>             height: 50px;
>             border-style: solid;
>             border-width: 10px;/*盒子边框的长度，单其实每一个属性都是复合属性，而且是按照上右下左的逆时针顺序进行的*/
>             border-left: 10px solid brown;/*单单设置左边框，也是复合属性*/
>             border-left-color: red;
> 
>         }
> </style>
> ```
>
> 同理padding和border一样，有着-left、-top、-bottom、-right等属性（浏览器边框与盒子边框的距离）
>
> 

