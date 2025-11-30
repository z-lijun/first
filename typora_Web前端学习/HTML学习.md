# HTML

HTML全称：Hypertext Markup Language（超文本标记语言）

> 标签：标签通常成对出现，包括开始标签和结束标签（也叫双标签），内容位于这两个标签之间
>
> ```html
> <p>这是一个段落。</p>
> <h1>这是一个标题。</h1>
> <a href="#">这是一个超链接。</a>
> ```
>
> 除了双标签，也存在单标签
>
> ```html
> <input type="text">
> <br>换行标签
> <hr>分割线标签
> ```
>
> 区别：单标签用于没有内容的元素，双标签用于有内容的元素

> #### HTML文件结构
>
> ```html
> <!-- 这里放置文档的元信息 -->
> <!DOCTYPE html>
> <html>
>  <head>
>   <!-- 这里放置文档的元信息 -->
>   <title>文档标题</title>
>   <mata charset="UTF-8">
>   <!--连接外部样式表或脚本文件等 -->
>   <link rel="stylesheet" type="text/css" href="styles.css">
>   <script src="script.js"></script>
>  </head>
>  <body>
>   <!-- 这里放置页面内容 -->
>   <h1>这是一个标题</h1>
>   <p>这是一个段落</p>
>   <a href="https://www.example.com">这是一个链接</a>
>   <!-- 其他内容 -->
>  </body>
> </html>
> ```

>#### `<body>`标签内容
> 
>更改文本样式
> 
>```text
> <p>更改文本样式：<b>字体加粗</b>、<i>斜体</i>、<u>下划线</u>、<s>删除线</s><p>
> 或者<strong>字体加粗</strong>
> ```
> 

> #### 列表
>
> ```html
> <ul>
>     <li>无序列表元素1</li>
>     <li>无序列表元素2</li>
>     <li>无序列表元素3</li>
> </ul>
> 
> <ol>
>     <li>有序列表元素1</li>
>     <li>有序列表元素2</li>
>     <li>有序列表元素3</li>
> </ol>
> 
> <h2>table row</h2>
> <h2>table data</h2>
> <h2>table header</h2>
> #形成表格列表
> <table border="1"> #border形成表格边框，后面数字表示表格边框宽度
>     <tr>#table row
>     	<th>列标签1</th>#table header
>         <th>列标签2</th>
>         <th>列标签3</th>
>     </tr>
>     <tr>
>         <td>元素11</td>#table data
>         <td>元素21</td>
>         <td>元素31</td>
>     </tr>
>     <tr>
>         <td>元素12</td>
>         <td>元素22</td>
>         <td>元素32</td>
>     </tr>
> </table>
> ```

> #### html属性
>
> 属性在html中起到非常重要的作用，它们用于定义元素的行为和外观，以及与其他元素的关系。
>
> 基本语法
>
> ```html
> <开始标签 属性名="属性值">
> ```
>
> 每个HTML元素都可以具有不同的属性
>
> ```html
> <p id="descrbe" class="section">
>     这是一个段落标签
> </p>
> <a href="https://www.baidu.com">这是一个超链接</a>
> <a href="https://www.baidu.com" target="_self">这是第二个超链接</a>
> ```
>
> `<a>`标签中的href属性定义了链接到的目标
> target属性定义链接的打开方式，有四个值：
>
> - #：不跳转
>
> - _self：在当前的窗口或标签页打开
> - _blank：在新的窗口或标签页打开
> - _parent：链接将在父窗口或者父框架中打开
> - _top：在顶层窗口或顶层框架中打开
>
> 属性名称不区分大小写，属性值对大小写敏感
>
> ```html
> <img src="example.jpg" alt="">
> <img SRC="example.jpg" alt="">
> <img src="EXAMPLE.jpg" alt="">
> #前两者相同，第三个不一样
> ```

> #### 适用于大多数HTML元素的属性
>
> | 属性  |                        描述                        |
> | :---: | :------------------------------------------------: |
> | class | 为HTML元素定义一个或多个类名（类名从样式文件引入） |
> |  id   |                  定义元素唯一的id                  |
> | style |                 规定元素的行内样式                 |
>
> 例如
>
> ```html
> <h1 id="title"></h1>
> <div class="nav-bar"></div>
> <h1> class="nav-bar"></h2>
> ```

> #### 图片标签`<img>`
>
> ```html
> <img src="" alt="" width="" height="">
> ```
>
> src属性定义了要显示图像文件的路径或者URL
> alt属性定义图像的替代文本，如果src中的图片无法加载，就会显示alt属性中指定的文本
> width属性设置图片宽度（长）
> height属性设置高度（高）
>
> 例如：
>
> ```html
> <img src="logo.png" alt="">
> <img src="leg.png" alt="该图片无法显示">
> ```

> #### HTML区块-块元素与行内元素
>
> ##### 块元素（block）
>
> 块级元素通常用于组织和布局页面的主要结构和内容，例如段落、标题、列表、表格等。它们用于创建页面的主要部分，将内容分成逻辑块。
>
> - 块级元素通常从新行开始，并占据整行的宽度，因此它们会在页面上呈现为一块独立的内容块
> - 可以包含其他块级元素和行内元素
> - 常见的块级元素包括`<div>`,`<p>`,`h1`到`h6`,`<u1>`,`<ol>`,`<li>`,`<table>`,`<form>`等
>
> ##### 行内元素（inline）
>
> 行内元素通常用于添加文本样式或为文本中的一部分应用。它们可以在文本中插入小的元素，例如超链接、强调文本等。
>
> - 行内元素通常在同一行内呈现，不会独占一行
> - 它们只占据其内容所需的宽度，而不是整行的宽度
> - 行内元素不能包含块级元素，但可以包含其他行内元素
> - 常见的行内元素包括`<span>`,`<a>`,`<strong>`,`<em>`,`<img>`,`<br>`,`<input>`等
>
> ##### 行内块元素（Inline-block）
>
> - 水平方向上排列，但可以设置宽度、高度、内外边距等块级元素的属性
> - 行内块元素可以包含其他行内元素或块级元素

> #### `<div>`标签
>
> 用于创建可以包含其他HTML元素的容器块，通常没有任何语意，仅用于组织内容，经常用于创建页面的布局结构
>
> 代码：
>
> ```html
> <div class=" ">内容</div>
> ```

> #### `<span>`标签
>
> 相当于没有特殊元素的`<a>`标签和`<img>`标签，主要作用是把一小部分文本包装起来，以便于对它们使用样式、CSS行为或JS行为
>
> 代码：
>
> ```html
> <span>内容</span>
> ```

> #### HTML表单
>
> 表单中的`<form>`标签，`<form>`标签是表单的容器，有着非常多的属性，想要创建一个表单，将所有元素包含在`<form>`标签内部就可以了
>
> `<form>`标签中的`<input>`输入属性
>
> ```html
> <input type="text" placeholder="请输入内容">
> <input type="text" value="请输入内容">
> ```
>
> 其中的type属性规定要显示的`<input>`元素的类型，若将text元素改成radio，就变成了一个单选placeholder属性规定了`<input>`所形成的文本框中显示的内容，如：请输入内容
> value属性和placeholder属性差不多，只不过value是将文本直接填充进去，而placeholder是点击时就会消失，只是一个提示
>
> `<label>`标签：仅限于和`<input>`对应使用，和`<span>`差不多
>
> ```html
> <label for="">文本</label>
> ```
>
> for属性是把`<label>`标签绑定到`<input>`元素
> 例如：
>
> ```html
> <label for="username">文本</label>
> <input type="text" id="username" placeholder="请输入用户名">
> ```
>
> `<input>`中若将text元素改成radio，就变成了一个选择，再加上name就变成了单选
>
> ```html
> <input type="radio" name="gender"> 男
> <input type="radio" name="gender"> 女
> <input type="radio" name="gender"> 其他
> #name中的单词必须一致，这样就变成单选
> ```
>
> `<input>`中的type中有一个专门的password元素，可以将密码隐藏起来
> 例如：
>
> ```html
> <input type="password" id="pwd" placeholder="请输入密码">
> ```
>
> type属性中的多选——checkbox
>
> ```html
> <input type="checkbox" name="hobby"> 唱歌
> <input type="checkbox" name="hobby"> 跳舞
> <input type="checkbox" name="hobby"> 烹饪
> ```
>
> type属性中的提交——submit
>
> ```html
> <input type="submit" value="上传">
> ```
>
> 会生成一个提交的按钮，value：按钮的名字，会将`<form>`当中的数据发送出去，发送的地址就是`<form>`标签中的action
> 故action的值就是一个URL，这个URL不是乱填的，需要服务器后台发送API，没有的话就用\#占用
>
> ```html
> <form action="#"></form>
> ```



