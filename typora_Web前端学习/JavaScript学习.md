# JavaScript

> #### 什么是JavaScript
>
> JavaScript和Java没有任何关系
> JavaScript简称js
>
> JavaScript是一种轻量级、解释型、面向对象的脚本语言。它主要被设计用于在网页上实现动态效果，增加用户与网页的交互性。
>
> 作为一种客户端脚本语言，JavaScript可以直接嵌入HTML，并在浏览器中执行。
>
> 与HTML和CSS不同，JavaScript使得网页不再是静态的，而是可以根据用户的操作动态变化的。

> #### JavaScript的作用
>
> JavaScript在前端开发中扮演着重要的角色，其应用领域包括但不限于：
>
> - 客户端脚本：用于在用户浏览器中执行，实现动态效果和用户交互
> - 网页开发：与HTML和CS协同工作，使得网页具有更强的交互性和动态性
> - 后端开发：使用Node.js，JavaScript也可以在服务器端运行，实现服务器端应用的开发

> #### JS导入方式
>
> CSS代码是放在style标签内，JS代码是放在script标签内，script标签可以放在head标签和body标签中
>
> 第一种是在html中写script标签，第二种是外部引用，将JS代码单独保存在外部文件中，通过script标签的src属性引入
>
> 第一种内联样式的导入代码：
>
> ```html
> <!DOCTYPE html>
> <html lang="en">
> <head>
>     <meta charset="UTF-8">
>     <meta name="viewport" content="width=device-width, initial-scale=1.0">
>     <title>JS 导入方式</title>
>     <script>
>         console.log('hello,head标签的内联样式');
>     </script>
> </head>
> <body>
>     <h1>JavaScript 的导入方式</h1>
>     <script>
>         console.log('hello,body标签的内联样式');
>     </script>
> </body>
> </html>
> ```
>
> 在浏览器中按F12，用console.log属性，打开console控制台，就可以看到script的导入

> 第二种外联样式的导入代码：
>
> ```html
> <!DOCTYPE html>
> <html lang="en">
> <head>
>     <meta charset="UTF-8">
>     <meta name="viewport" content="width=device-width, initial-scale=1.0">
>     <title>JS 导入方式</title>
>     <!-- 用script的src属性导入JS，使用的是相对路径，./是引用在当前文件夹下的文件 -->
>     <script src="./js/myscript.js"></script>
> </head>
> <body>
> </body>
> </html>
> ```
>
> ```js
> <!-- JS文件夹中的myscript.js文件-->
> console.log('hello,外联样式');
> ```
>
> js文件中输入log可以直接生成`console.log`标签

> alert属性可以生成页面显示弹窗
>
> ```
>     <script>;
>         alert("你好，内联样式代码");
>     </script>
> ```

> #### JS 基本语法
>
> var，全称variable，变量的意思，具有函数作用域
>
> let  赋值属性，具有块级作用域，更安全更灵活
>
> const 声明常量
>
> 一般就是使用let和const，而避免使用var
>
> ```
> <script>
> var x;
> let y = 5;
> const PI = 3.14;
> </script>
> ```
>
> 示例：
>
> ```html
> <!DOCTYPE html>
> <html lang="en">
> <head>
>     <meta charset="UTF-8">
>     <meta name="viewport" content="width=device-width, initial-scale=1.0">
>     <title>JavaScript 基本语法</title>
> </head>
> <body>
>     <script>
>         var x;
>         let y = 5;
>         const PI = 3.14;
>         console.log(x, y, PI);
>         let name = '如花';
>         console.log(name);
>         let empty_value = null;
>         console.log(empty_value);
>     </script>
> </body>
> </html>
> ```
>
> x显示出的undefined，和空值null
>
> 区别：null表示已经赋值了，就是空，而undefined表示还没计算出来，或者函数没有返回值时，返回的也是undefined

> #### 条件语句
>
> 条件语句是编程中常用的结构，用于基于不同的条件执行不同的代码块。
>
> `if`语句：用于执行一个代码块，当指定的条件为真（true）时执行。语法如下：
>
> ```js
> if(condition){
> 	// 如果条件为真，执行这里的代码
> }
> ```
>
> `else`语句：用于在上一个if和所有的else if都为假时执行的代码块。语法如下：
>
> ```js
> if (condition){
> 	// 如果条件为真，执行这里的代码
> }else{
> 	// 如果条件为假，执行这里的代码
> }
> ```
>
> `else if`语句：用于在上一个if语句条件为假时，检查另一个条件。可以有多个else if语法。语法如下：
>
> ```js
> if (condition1){
>     // 如果条件1为真，执行这里的代码
> }else if (condition2){
>     // 如果条件2为真，执行这里的代码
> } else{
>     // 如果以上条件都为假，执行这里的代码
> }
> ```
>
> if和else都只有一个，而else if 可以有多个
>
> 示例：
>
> ```js
> <!DOCTYPE html>
> <html lang="en">
> <head>
>     <meta charset="UTF-8">
>     <meta name="viewport" content="width=device-width, initial-scale=1.0">
>     <title>JavaScript 基本语法</title>
> </head>
> <body>
>     <script>
>     //判断年龄if else语句
>         let age = 9;
>          if (age > 18) {
>             console.log('你已经成年了');
>          }else{
>             console.log('未成年');
>          }
> 	//判断时间if elseif语句，注意alert里面要用英文引号
>          let time = 12;
>          if (time < 12) {
>             alert('上午好');            
>          } else if (time < 18) {
>             alert('下午好');
>          }else{
>             alert('晚上好');
>          }
>     </script>
> </body>
> </html>
> ```

> #### 循环语句
>
> 循环语句用于重复执行一段代码，直到指定的条件不再满足为止
>
> `for`循环：是一种常见的循环结构，用于按照指定的条件重复执行代码块
>
> ```js
> for (初始化表达式；循环条件；迭代器){
> 	// 循环体，执行这里的代码
> }
> ```
>
> 示例：
>
> ```html
> <!DOCTYPE html>
> <html lang="en">
> <head>
>     <meta charset="UTF-8">
>     <meta name="viewport" content="width=device-width, initial-scale=1.0">
>     <title>JavaScript 基本语法</title>
> </head>
> <body>
>     <!--For 循环并打印出i的值-->
>     <script>
>         console.log("For 循环");
>         for (let i = 0; i < 10; i++) {
>             console.log(i);
>         }
>     </script>
> </body>
> </html>
> ```
>
> html注释是<!--注释-->，js的注释//
>
> `while`循环会在指定条件为真时执行代码块
>
> 代码：
>
> ```
> while(循环条件){
> 	// 循环体，执行这里的代码
> }
> ```
>
> 一般有限循环使用for循环，无限循环使用while循环
>
> 示例：
>
> ```js
> <!DOCTYPE html>
> <html lang="en">
> <head>
>     <meta charset="UTF-8">
>     <meta name="viewport" content="width=device-width, initial-scale=1.0">
>     <title>JavaScript 基本语法</title>
> </head>
> <body>
>     <script>
>         //while 循环，实现打印1到10
>         console.log("while 循环");
>         let count = 1;
>         while (count < 10) {
>     console.log(count);
>     count++;//将count加一，防止产生无限循环
> }
>     </script>
> </body>
> </html>
> ```

> #### break与continue
>
> 循环关键字
>
> - `break` 用于跳出循环，结束循环的执行
> - `continue` 用于跳出当前循环中的剩余代码，继续下一次循环
>
> 示例：
>
> ```js
> <!DOCTYPE html>
> <html lang="en">
> <head>
>     <meta charset="UTF-8">
>     <meta name="viewport" content="width=device-width, initial-scale=1.0">
>     <title>JavaScript 基本语法</title>
> </head>
> <body>
>     <script>
>         //测试函数关键字
>         for(var i = 0; i < 7;i++){
>             if(i==2){
>                 continue;
>             }
>             if(i==4){
>                 break;
>             }
>             console.log(i);
>             //只会打印0，1，3，因为2被跳过了，而4和后面的被中断了
>         }
>     </script>
> </body>
> </html>
> ```

> #### 函数
>
> JavaScript函数
>
> `函数`是一段可重复使用的代码块，它接受输入（参数）、执行特定任务，并返回输出。
>
> ```js
> function function_name(参数1,参数2,参数3,...){//参数可以不写，表示不传参
> 	// 函数体，执行这里的代码
> 	return 返回值;// 可选，返回值
> }
> ```
>
> 示例：
>
> ```js
> <!DOCTYPE html>
> <html lang="en">
> <head>
>     <meta charset="UTF-8">
>     <meta name="viewport" content="width=device-width, initial-scale=1.0">
>     <title>Document</title>
> </head>
> <body>
>     <script>
>         //定义函数
>         function hello() {
>             console.log('hello,world!');
>         }
>         hello();//调用函数
>         //定义有返回值的函数
>         function hello_with_return(){
>             return 'hello,world! - 返回值';
>         }
>         let a = hello_with_return();//接收返回值
>         console.log(a);//打印出返回值
>         console.log(hello_with_return());//也可直接打印出返回值
>         
>         //定义一个有参数的函数
>         function hello_with_friends(name){
>             console.log('hello,' + name);
>         }
>         //调用函数，给予函数参数
>         hello_with_friends('李华')
>     </script>
> </body>
> </html>
> ```
>
> > ##### 作用域
> >
> > 作用域分为局部作用域和全局作用域
> > 在函数内部声明的变量具有局部作用域，在函数外面声明的变量具有全局作用域

> #### 事件
>
> 事件是文档或浏览器窗口中发生的特定瞬间，例如用户的点击、键盘的按下、页面的加载等。常见的事件如下
>
> |    事件     |       描述       |
> | :---------: | :--------------: |
> |   onClick   |     点击事件     |
> | onMouseOver |     鼠标经过     |
> | onMouseOut  |     鼠标移出     |
> |  onChange   | 文本内容改变事件 |
> |  onSelect   |    文本框选中    |
> |   onFocus   |     光标聚集     |
> |   onBlur    |     移开光标     |
>
> > #### 事件绑定
> >
> > JavaScript绑定事件的方法有三种：
> >
> > - `HTML`属性
> > - `DOM`属性
> > - `addEventListener`方法
>
> > 示例：
> >
> > ```js
> > <!DOCTYPE html>
> > <html lang="en">
> > <head>
> >     <meta charset="UTF-8">
> >     <meta name="viewport" content="width=device-width, initial-scale=1.0">
> >     <title>事件处理</title>
> > </head>
> > <body>
> >     <!--按钮属性-->
> >     <button onclick="click_event()">这是一个点击事件按钮</button>
> >     <!-- 文本输入框，属性跟着聚焦和失焦事件 -->
> >     <input type="text" onfocus="focus_event()" onblur="blur_event()">
> >     <script>
> >         // 点击事件
> >         function click_event(){
> >             alert('点击事件触发了');
> >         }
> >         // 聚焦事件
> >         function focus_event(){
> >             console.log('获取焦点');
> >         }
> >         // 失去焦点事件
> >         function blur_event(){
> >             console.log('失去焦点');
> >         }
> >     </script>
> > </body>
> > </html>
> > ```

> #### DOM
>
> 在Web开发中，DOM通常与JavaScript一起使用
>
> 当网页被加载时，浏览器会创建页面的文档对象，也就是DOM（Document Object Model）。
> 每个HTML或XML文档都可以被视为一个文档树，文档树是整个文档的层次结构表示。
> 文档节点是整个文档树的根节点。
> DOM为这个文档树提供了一个编程接口，开发者可以使用JavaScript来操作这个树状结构。
>
> ![](C:\Users\赵立军\Desktop\jds.png)
>
> 示例代码：
>
> ```
> 
> ```
>
> 

