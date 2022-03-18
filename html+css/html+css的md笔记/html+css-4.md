#### 1. HTML与XHTML的区别

  * `DOCTYPE`文档及编码
  * 元素大小写  （ `XHTML`不允许元素标签大写 ）
  * 属性布尔值  （ `XHTML`属性的值必须要完整 ）
  * 属性引号    （ `XHTML`属性的值必须要加引号 ）
  * 图片的alt属性（ `XHTML` img 中必须加alt属性 ）
  * 单标签的写法 （ `XHTML`单标签后必须要加/ `<br/>` ）
  * 双标签闭合

#### 2. strong和b标签、em和i标签

  * 表现形态都是 文本加粗 和 文本斜体，区别在于，`strong`和`em`是具备语义化的,而b和i不具备语义化
  
  * 注意：`strong`、`b`、`em`、`i`、`span` 都属于内联

#### 3. 引用标签
  |标签类型|描述|元素类型|
  |---|---|---|
  |`blockquote` | 引用大段段落解释|  块元素，带有上下左右外边距
  |`q` | 引用小段的短语解释 |        内联元素，会自动添加双引号
  |`abbr` | 缩写或首字母缩略词|   内联元素，默认带有下划点线，删除`title`属性后，点线消失 
  |`address` | 引用文档地址信息|  块元素，默认斜体 `font-style: italic;` 
  |`cite` | 引用著作的标题|       内联元素，默认斜体 `font-style: italic; `

#### 4. iframe嵌套页面 标签

  * `iframe`元素会创建包含另外一个文档的内联框架（即行内框架）
    * 可以引用其他`html`到当前`html`中显示。

  * 主要是利用`iframe`属性进行样式的调节。
      |属性|描述|
      |---|---| 
      |`frameborder`|规定是否显示框架周围边框 ，`0`表示不显示，`1`表示显示
      |`width`| 定义`iframe`的宽度
      |`height`| 定义`iframe`的高度
      |`scrolling` |规定是否在`iframe`中显示滚动条 ，`scrolling="no"`表示不显示滚动条
      |`src` |   规定在`iframe`中引入`URL`
      |`srcdoc`| 规定在`iframe`中显示的页面内容

  * 应用场景：
    * 数据传输
    * 共享代码： 如：W3school网站的演示示例，改变`iframe`的`src`来进行区域内容切换
    * 局部刷新
    * 第三方介入

#### 5. br与wbr标签

  * `br`表示换行操作，而`wbr`表示软换行操作。  `<br/>`  `<wbr/>`
  
  * `wbr`软换行，添加在较长单词中间，告诉浏览器换行时机
    * 如果单词太长，或者您担心浏览器会在错误的位置换行，那么可以使用`wbr`元素来添加 Word Break Opportunity ( 单词换行时机 )

#### 6. pre元 与 code

  * 针对网页中的程序代码的显示效果。(显示的都是等宽字体)

    * `pre`不支持回车，`code`支持回车。

#### 7. map 与 area

  * 给特殊图形添加链接，`area`能添加热区的形状：矩形、圆形、多边形。

  ```xml
  <img src="" alt="" usemap="#star">
  <map name="star">
    <area shape=""  coords="" href="" alt="">
  </map>
  ```

  * `shape`指定形状 : `rect` 矩形 、`circle` 圆 、 `poly` 多边形
  * `coords`制定坐标 : 
    * 矩形：`coords="x1 y1 x2 y2"`  矩形左上、右下角坐标
    * 圆形: `coords="x1 y1 r"`       圆心坐标与半径
    * 多边形：`coords="x1 y1 x2 y2 x3 y3..."` 每个拐点的坐标，首尾坐标会相连
  * `href`跳转`URL`地址

#### 8. embed 与 object

  * `embed`和`object`都能够嵌入一些多媒体，如flash动画、插件等。基本使用没有太多区别，主要是为了兼容不同的浏览器。
    * `object`要配合`param`使用
    * 关于`object`扩展
      ```xml
      <object data="" type="">
        <!-- 设置文件路径，name值要写对 -->
        <param name="movie" value=".Flash/flash5377.swf">  

        <!-- 设置透明度，name值要写对 -->
        <param name="wmode" value="transparent">           
      </object>
      ```

#### 9. audio 与 video

  * `audio`控制音频，`video`控制视频，可通过`controls`属性来显示控件。
    |属性名|描述|
    |---|---| 
    |`controls` | 显示控件
    |`autoplay` | 自动播放
    |`hidden`   | 隐藏
    |`loop`     | 循环
    |`muted`    | 默认静音
    |`preload`  | 如果出现该属性，则音频在页面加载时进行加载，并预备播放。<br>如果使用 `"autoplay"`，则忽略该属性。
    |`poster` | 规定视频下载时显示的图像，或者在用户点击播放按钮前显示的图像。如果未设置该属性，则使用视频的第一帧来代替。

  * 关于浏览器格式不支持问题
    * `<source>`标签添加在 `audio`、`video` 内部 ，`src`链接添加在`source`内，可以设置多个格式在多个`source` 单标签，放入`src`地址
      ```xml
      <video>
        <source src="" type="video/mp4">
        <source src="" type="video/ogg">
        <source src="" type="video/avi">
      </video>
      ```
        * 按从上到下的顺序引入, 第一个能播放 后面的就不需要, 
          * 不同的浏览器 支持不同的格式, 总共就这个三种格式 `mp4\ogg\avi`

  * 关于等比缩放的扩展：如果不想让子元素等比缩放，给子元素添加 `min-width="100%"`
      <div style="page-break-after:always; "></div> 

#### 10. 文字注解

  * `ruby` 、 `rt` 这样一个组合要结合使用
    ```xml
    <p> 这是一个段 <ruby>落 <rt> luo </rt></ruby> </p> 
    <!-- 给文字上方添加注音 -->
    ```

  * `bdo` 可以改变文字排列方向
    ```xml
    <bdo dir="rtl">这是一个段落</bdo> <!-- 从右向左排列 -->
    ```

  * `CSS`样式中如何改变文字排列方向
    ```css
    span{ direction : rtl; unicode-bidi: bidi-override;}
    ```
    * `unicode-bidi` 属性与 `direction` 属性一起使用，来设置或返回文本是否被重写。
      * `bidi-override`属性 创建一个附加的嵌入层面。重新排序取决于 `direction` 属性。

#### 11. link标签的扩展

  * 添加外部样式
    ```xml
    <link rel="stylesheet" type="text/css" href="./样式地址">
    ``` 
    
  * 添加网址的小图标
    ```xml
    <link rel="icon" type="/image/x-icom" href="./图标地址">
    ``` 
  * `DNS`预解析（加快网站访问速度）
    ```xml
    <link rel="dns-prefetch" href="解析网址">
    ``` 

#### 12. meta标签扩展学习

  * `meta`添加一些辅助信息
  * 网站描述
    ```xml
    <meta name="description" content= "大连美团网精选大连美食餐厅,酒店预订,电影票">
    ```
  * 添加搜索关键字
    ```xml
    <meta name="keywords" content="大连美食，大连酒店,大连团购" > 
    ```
  * 选择浏览器内核
    ```xml
    <meta name="renderer" content= "webkit" > 
    ```
  * IE 解决部分兼容问题
    ```xml
    <meta http-equiv= "X-UA-Compatible" content="ie=edge" >  
    ```
  * 重定向：网页三秒后跳转地址
    ```xml
    <meta http-equiv="refresh" content= "3" url="跳转的地址">   
    ```
  * 指定网页在缓存中的过期时间，一旦网页过期，必须到服务器上重新传输。
    ```xml
    <meta http-equiv=" expires" content= "Wed, 20 Jun 2019 22:33:00 GMT">
    ```

#### 13. HTML5新语义化标签
  |H5标签|描述|
  |---|---|
  |`header` | 页眉 
  |`footer` | 页脚
  |`main`   | 主体 
  |`hgroup` | 标题组合          
  |`nav`    | 导航
  |`article` | 独立的内容
  |`aside`   | 辅助信息的内容
  |`section` | 区域
  |`figure`  | 描述图像或视频
  |`figcaption` | 描述图像或视频的标题部分
  |`details`/`summary` | 文档细节/文档标题

  * 注：`header`、`footer`、`main`在一个网页中只能出现一次
  
  * `datalist` : 选项列表  (用在文本输入框，可以结合`js`，提示用户近期输入的内容)
    ```xml
    <input type="text" list="tishi">
    <datalist id="tishi">
      <option value="abbr"></option>
      <option value="asssd"></option>
    </datalist>
    ```
  * `progress`/`meter`  : 定义进度条/定义度量范围
    * `meter`标签属性: `min` `max` `value` `low` `high`

  * `time`   :   定义日期或时间
    * `我在 <time datetime="2010-02-14">情人节</time> 有个约会。`
  * `mark`   :   带有记号的文本

#### 14. 表格的扩展学习

  * 隐藏空单元 : `empty-cells:hide;`
  * 添加单线   : `border-collapse:collapse;`
    * `border-collapse:collapse;`让表格显示单线边框，两个相邻的单元格只会有一个边框线
  * 单元格斜线 : `border`/`rotate`   (设置超大边框和文字定位)

  * 列分组 : `colgroup`/`col`  

#### 15. 表单扩展学习

  * 美化表单控件：  1. `label` + `:checked`； 2. `position` + `opacity`

  * 新的`input`控件
    |input新增的type属性值|描述| 
    |---|---|
    |`email`  | 电子邮箱地址输入框
    |`url`    | 网址输入框
    |`number` | 数值输入框
    |`range`  | 滚动条
    |`date`/`month`/`week` | 日期控件，`date`具备年月日，`month`具备年月，`week`具备年和周
    |`search` | 搜索框
    |`color`  | 颜色控件
    |`tel`    | 电话号码输入框 ，在移动端会默认调起数字键盘
    |`time`   | 时间控件

  * 新的表单属性:
    |属性名|说明| 
    |---|---|
    |`autocomplete` | 自动完成    (提示之前输入的信息 默认：`on`开启  /`off `关闭)
    |`autofocus` | 获取焦点       ( 加载时光标在控件上)
    |`required`  | 不能为空
    |`method`   | 数据传输方式<br>`GET`，安全性低，适合用在查询；`POST`，安全性高
    |`enctype`  | 数据传输类型<br>字符串 ：  `enctype="application/x-www-form-urlencoded"`  <br>二进制数据流 ：可提交文件 `enctype="multipart/form-data"`
    |`name`/`value` | 数据的键值对
    |`pattern`   | 使用在需要验证的`from`控件中，正则表达式验证是否符合规则
      * `pattern`属性要在有`form`表单时, 并且点击该`form`表单的提交按钮后才会验证。

  * 扩展标签 ：
    * `fieldset`   :  表单内元组分组(将内部标签包裹)
      * `legend`     :  为`fieldset`元素定义标题
    * `optgroup`   :  定义选项组

#### 16. BFC规范
  * 触发`BFC`规范的元素，可以形成一个独立的容器，不受到外界的影响，从而解决布局问题。

  * **BFC**（Block Formatting Context）叫做“块级格式化上下文"
    1. 内部的盒子会在垂直方向，一个个地放置；
    2. 盒子垂直方向的距离由`margin`决定， **属于同一个BFC的两个相邻Box的上下`margin`会发生重叠**；
    3. 每个元素的左边，与包含的盒子的左边相接触，即使存在浮动也是如此；
    4. **`BFC`的区域不会与`float`重叠**；
    5. `BFC`就是页面上的一个隔离的**独立容器**，容器里面的子元素不会影响到外面的元素，反之也如此；
    6. *计算`BFC`的高度时，浮动元素也参与计算*。
    <br> 
    * 触发BFC 规范
      1. 根元素(`html`)；
      2. `float`的属性不为`none`；
      3. `position`为`absolute`或`fixed`；
      4. `display`为`inline-block`，`table-cell`(表格单元格)，`table-caption`(表格标题)，`flex`,`grid`；
      5. `overflow`不为`visible`
      
  * BFC特性及应用
    * 解决`margin`叠加问题
    * 解决`margin`传递问题
    * 解决浮动问题
    * 解决`float`覆盖问题

