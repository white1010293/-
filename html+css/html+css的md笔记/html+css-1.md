#### 1. 什么是HTML、CSS？
  * 是做网站的编程语言。
  * 浏览器把代码解析后的样子就是我们看到的网站。可以通过鼠标右键选择查看网页源代码。

  * 如何去写代码？写到哪里呢？
    * 一个网站是由N个网页组成的。 每一个网页 `.HTML`文件

#### 2. VSCode编辑器
  * `VS code`下载地址：https://code.visualstudio.com/

  * 如何安装插件？  语言包、`open in browser`、`view in browser`、`live server、px to rem`

  * 学习编辑器基本使用
    * 设置： 文件-> 首选项-> 设置 ( 大小、是否换行 `word wrap` )
      |快捷键|功能|
      |---|---|
      |ctrl + s | 保存|
      |ctrl + a |全选|
      |ctrl + x 、ctrl + c 、ctrl + v | 剪切、复制、黏贴|
      |ctrl + z 、ctrl + y | 撤销、前进|
      |shift + end |从头选中一行|
      |shift + home |从尾部选中一行|
      |shift + alt + `↓` |快速复制一行|
      |alt + `↓`或`↑` |快速移动一行|
      |tab |向后缩进|
      |tab + shift |向前缩进|
      | alt + 鼠标左键|多光标|
      |ctrl + d |选择相同元素的下一个|

#### 3. Chrome浏览器？（谷歌浏览器）
  * 下载地址：自行搜索，官网下载
  * Chrome占浏览器市场份额：66.88%

####  4. 深入了解网站开发？

  * UI设计师：设计稿
  * web前端开发工程师（`H5`开发）
    * 设计稿 -> 代码
    * 数据库里的数据 -> 显示到页面
      * `HTML` + `CSS `
        `HTML` : 结构，`CS` ： 样式，`JS`：行为
  * web后端开发工程师

#### 5. web三大核心技术？
  `HTML` + `CSS` + `JavaScript`

#### 6. HTML基本结构和属性？

  * `HTML` : 超文本 标记 语言
    * 超文本 ：文本内容 + 非文本内容 （ 图片、视频、音频等 ）
    * 标记 ：`<`单词`>`
    * 语言 ：编程语言

  * 标记也叫做标签：
      * 单标签  `<header>`
      * 双标签  `<header></header>`

  * 标签是可以上下排列，也可以组合嵌套。

  * `HTML`常见标签属性：http://www.html5star.com/manual/html5label-meaning/

  * 标签的属性：来修饰标签的，设置当前标签的一些功能。
    `<img src="value" title="value">`

#### 7. HTML初始代码？

  * 每个`.html`文件都有的代码叫做初始代码，要符合`html`文件的规范写法。
    `！+ tab`键 ：快速的创建`html`的初始代码
  ```xml
  
  <!DOCTYPE html>  <!-- 文档声明：告诉浏览器这是一个html文件 -->
  <html lang="en">  <!-- lang="en"表示是一个英文网站 lang="zh-cn"表示一个中文网站 -->
  <head>
      <meta charset="UTF-8"> <!-- 元信息：是编写网页中的一些赋值信息 charset="UTF-8"国际编码 -->
      <title>标题写这里</title>  <!-- 设置网页的标题 -->
  </head>
  <body>
  显示网页内容的区域 
  </body>
  </html>
  ```
  * `VsCode`更改每种语言的快速创建方式：设置-用户代码片段-选择语言

#### 8. HTML注释

  写法：`<!-- 注释的内容 -->` 在浏览器中看不到，只能在代码编辑时看到注释的内容

  * 意义：
    1. 把暂时不用的代码注释起来，方便以后使用
    2. 对开发人员进行提示

  * 快速添加与删除注释：
    1. `ctrl + /`
    2. `shift + alt + a`

#### 9. 标题与段落
  * 标题：双标签 `<h1></h1>` ... `<h6></h6>`
    * 在一个网页中，`h1`标题最重要，并且一个`.html`文件中只能出现一次`h1`标签
    * `h5` `h6`标签在网页中不经常使用。

  * 段落：双标签 `<p></p>`

#### 10. 文本修饰标签
  * `<strong></strong>`、`<em></em>`
    * 区别：
      1. 写法和展示效果是有区别的，一个加粗、一个斜体
      2. `strong`的强调性更强，`em`的强调性稍弱
          
  * 下标 ：`<sub></sub>` 文本<sub>sub</sub>
  * 上标 ：`<sup></sup>` 文本<sup>sup</sup>

  * 删除文本 ：`<del></del>` <del>del</del>
  * 插入文本 ：`<ins></ins>` <ins>ins</ins>
      注：一般情况下，删除文本都是和插入文本配合使用的。

#### 11. 图片标签

  * `img` :单标签
    * `src` ：引入图片地址
    * `alt` ：当图片出现问题的时候，可以显示一段友好的提示文字
    * `title` ：提示信息（ 所有标签都具有`title`属性 ）
    * `width`、`height` : 图片的大小 

#### 12. 路径的引入
  * 相对路径（`.`  `..`）：`../`返回上一级目录，可以通过多次`../../../`来返回想要的目录
  绝对路径： 网络路径、本地其他文件 

#### 13. 链接标签

  * `a` ： `<a></a>`
    * `href`属性 ：链接的地址
    * `target`属性 ：可以改变链接打开方式
      * `_self` ：默认，在当前页面打开  
      * `_blank` ：新窗口打开

  * `base` ：单标签 ，作用就是改变链接的默认行为。添加在`<head>` ， `<base target="_blank">`

#### 14. 跳转锚点

  * 跳转锚点是在本页面进行的操作(也可以跳转到其他页面)，可以跳转到本页面指定位置。

  1. `#`号 + `id`属性：`a`跳转到其他标签，给`a`链接`href="#跳转id"`
      ```html
      <a href="#tiaozhuan"></a>
      <p id="tiaozhuan"></p>
      ```
  2. `#`号 + `name`属性：`a`跳转`a`标签，注意`name`属性加给的是`a`标签
      ```html
      <a href="#aa"></a>
      <a name="aa"></a>
      ```

  * 邮箱链接：`<a href = "mailto:2802@qq.com"> </a>`
  * 下载链接：`<a href = "./1.rar"> </a>`

#### 15. 特殊字符
  1. `&` + 字符
  2. 解决冲突  左右尖括号、添加多个空格的实现
      * `&lt;`（左尖括号、小于号）、`&gt;`（右尖括号、大于号）、`&nbsp;`（空格符）

#### 16. 列表标签  （列表标签夹层不能含有其他标签） 

 1. 无序列表 ：`ul` `li` 符合嵌套的规范
 2. 有序列表 ：`oi` `li` 一般用的比较少，可以用无序列表来实现
    * `type`属性可以更改列表样式，一般不用
    * 有序列表扩展：`start`让列表从多少开始计数,`reversed`表示倒序显示,`type`定义前缀样式
      ```html
      <ol start="50" reversed type="v">
        <li>咖啡</li>
        <li>牛奶</li>
        <li value="1">茶</li>
      </ol>
      ```
        * `li` 的`value`属性：定义单个列表的开始序号（强制更改顺序）
         
 3. 定义列表 ：`dl` `dt` `dd` 列表项需要添加标题和对标题进行描述的内容

 * 注 ：列表之间可以互相嵌套，形成多层级的列表。

#### 17. 表格标签

  * `table` ：表格的最外层容器
  * `tr` ：定义表格行
  * `th` ：定义表头
  * `td` ：定义表格单元
  * `caption` ：定义表格标题（显示在表格上方）

    * 注：之间是有嵌套关系的，要符合嵌套规范。

  * 语义化标签 ：`tHead`、`tBody`、`tFoot`
    * `tBody`可以出现多次，但是`tHead`、`tFoot`只能出现一次。
    <br>
  * 表格属性 
    |属性名|格式|说明| 
    |---|---|---|
    |border |`border="1"` |表格边框|
    |align | `align="center"`|表格左右对齐的方式
    |valign |`valign="middle"`|写在`tr`或`td`单元格内容上下对齐方式|
    |cellpadding|`cellpadding="10"`|单元格内的空间，类似`padding`|
    |cellspacing |`cellspacing="10"`|单元格之间的空间，类似`margin`|
    |rowspan |`rowspan="2"`|合并行，添加给`td`|
    |colspan |`colspan="2"`|合并列，添加给`td`|

#### 18. 表单标签
  * `form` : 最外层容器
  * `input`（单标签）标签有一个`type`属性，决定是什么控件。
    * `type`属性：
      |属性名|描述|
      |---|---|
      |`text`|普通的文本输入框| 
      |`password`|密码输入框|
      |`checkbox`|复选框| 
      |`radio`|单选框|
      |`file`|上传文件|
      |`submit`|提交按钮|
      |`reset`|重置按钮|
      |`hidden`|隐藏的`input`，用户看不见，用于存储信息|
      
        * `checkbox`和`radio`通过`name`绑定分组
        * `placeholder`会在首次加载时在表单内显示想要的文本
        * `checked`首次加载时选中，`disabled`不可选中状态

      
  * `textarea` :多行文本框
    * `rows` ：行数 、`cols` : 列数|
  * `select`、`option`：下拉菜单
    * `selected` : 默认选中 `disabled` ：不可选中 `multiple` ：可多选

  * `label` ：标注，不会呈现任何效果。含有`for`属性，常绑定在单选框
    * `for` : `for` 属性可把 `label` 绑定到另外一个元素标签的`id`属性。

  * 关于表单被选中时会有边框的解决方法
    ```css
    input{ outline:none; }
    input:focus{ outline:none; }
    ```
            
#### 19. div和span
  * `div` ： 做一个区域划分的**块**
  * `span` : 对文字进行修饰的，**内联**

  * 注：默认是没有样式的，要用`CSS`添加样式

#### 20. CSS基础语法

  * `选择器{ 属性1 ：值; 属性2 ：值2 }`

    * `widht` : 宽
    * `height` ：高
    * `background-color` : 背景颜色（`css`中的背景颜色，`html`中有`bgcolor`）

  * 长度单位 ：
    1. `px` ：像素
    2. `%` ：百分比

  * `css`注释 ：`/* css注释的内容 */`
    * 快捷键 ；`shift+alt+a`、`ctrl+/`

#### 21. CSS样式的引入方式
  1. 内联样式 
      ```xml
      <p style="内联"></p>
      ```
          

  2. 内部样式 
      ```xml
      <head>
        <style> <!-- 内部样式 --> </style>
      </head>
      ```

  3. 外部样式
      * 引入一个单独的`CSS`文件，`name.css`
      * 通过`link`标签引入外部资源，`rel`属性制定资源跟页面的关系，`href`属性指资源的地址
        ```xml
        <link rel="stylesheet" href="地址">
        ```

      * `@import`方式也可以引入（注：这种方式是有很多问题的，不建议使用）

#### 22. CSS中的颜色表示法
  1. 单词表示法 ：red blue greed yellow ...

  1. 16进制表示法 ： #000000(最小值) #ffffff(最大值)

  2. `rgb`三原色表示法：`rgb(255,255,255)`
       * 取值范围`0~255`

  * 网页提取颜色的谷歌插件下载地址：https://www.baidufe.com/fehelper 

