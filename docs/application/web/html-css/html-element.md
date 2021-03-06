---
title: 一些元素
category: Web
tag: HTML
author: JQiue
article: false
---

## 标题

标题是通过`<h1>` ~ `<h6>` 定义的，`<h1>` 是最大的标题，`<h6>`是最小的标题

::: demo 标题元素

```html
<h1>一级标题</h1>
<h2>二级标题</h2>
<h3>三级标题</h3>
<h4>四级标题</h4>
<h5>五级标题</h5>
<h6>六级标题</h6>
```

:::

## 段落

段落通过`<p>`定义，被`<p>`包裹的内容会单独占一行

::: demo 段落元素

```html
<p>段落一</p>
<p>段落二</p>
<p>段落三</p>
<p>段落四</p>
```

:::

如果希望在不产生一个段落的情况下换行，可以使用`<br/>`标签，它是自闭和标签

::: demo br

```html
<p>内容一<br/>内容二<br/>内容三</p>
```

:::

::: danger
并不是代码换行浏览器就会解析换行，浏览器会将换行符看作一个空格
:::

## 文本格式化

HTML 提供了一些简单的文本格式化标签，无需写样式调整

::: demo 格式化

```html
<b>加粗</b> <!-- 废弃 -->
<strong>加粗</strong>
<i>斜体</i> <!-- 废弃 -->
<em>斜体</em>
<u>插入</u> <!-- 废弃 -->
<ins>插入</ins>
<s>删除</s> <!-- 废弃 -->
<del>删除</del>
<sub>下标</sub> 和 <sup>上标</sup>
<code>代码</code>
<mark>mark</mark>
```

:::

::: danger 被废弃的标签
因为 HTML 本身只是用来添加[语义](/web/html/4/)的，这些简写的样式标签即将废弃，应使用有语义的标签来替代
:::

## 预格式化文本

通常内容之间的额外的空格回车等都会被压缩，而预格式化文本可以保留这些东西

::: demo 预格式化文本

```html
<pre>
function foo () {
  console.log("Hello, World!");
}
</pre>
```

:::

::: tip
预格式化文本的内容通常以等宽字体显示
:::

## 列表

如果想表示数据的集合就应该使用列表元素，`<li>`是列表中的每一项

### 有序列表

通过`<ol>`定义有序列表，每个`<li>`都会有标明顺序的标识，可以改变`type`属性值来改变标识

::: demo 有序列表

```html
<ol>
  <li>第一项</li>
  <li>第二项</li>
  <li>第三项</li>
</ol>
<ol type="a">
  <li>第一项</li>
  <li>第二项</li>
  <li>第三项</li>
</ol>
<ol type="i">
  <li>第一项</li>
  <li>第二项</li>
  <li>第三项</li>
</ol>
```

:::

### 无序列表

无序列表通过`ul`创建，列表项没有像顺序一样的标识，通过改变`type`属性改变标识样式

::: demo 无序列表

```html
<ul>
  <li>第一项</li>
  <li>第二项</li>
  <li>第三项</li>
</ul>
<ul type="circle">
  <li>第一项</li>
  <li>第二项</li>
  <li>第三项</li>
</ul>
<ul type="square">
  <li>第一项</li>
  <li>第二项</li>
  <li>第三项</li>
</ul>
```

:::

### 自定义列表

自定义列表和其他列表不同的是，它是一个键值对形式的列表，通过`<dl>`（定义整个列表）、`<dt>`（定义标题）、`dd`（定义描述）这一套标签来定义

::: warning
`<dt>`和`<dd>`不能相互嵌套，`<dt>`不一定位于`<dl>`子元素的第一位，`<dt>`不一定只有一个
:::

::: demo 自定义列表

```html
<dl>
  <dt>标题一</dt>
  <dd>描述一</dd>
  <dd>描述二</dd>
  <dt>标题二</dt>
  <dd>描述一</dd>
  <dd>描述二</dd>
</dl>
```

:::

::: danger 对于所有的列表
任何列表元素都必须遵循合理的嵌套关系，即父元素只能容纳具体的列表项标签，不能容纳其他元素或内容
:::

## 表格

表格是一套标签组成的，`<table>`定义表格容器，`<tr>`定义行，`<tb>`定义单元格

::: demo 表格

```html
<table>
  <tr>
    <td>第一行第一个单元格</td>
    <td>第一行第二个单元格</td>
  </tr>
  <tr>
    <td>第二行第一个单元格</td>
    <td>第二行第二个单元格</td>
  </tr>
</table>
```

:::

::: tip
HTML 表格默认没有边框和斑马纹，这是 markdown 转换成对应的 HTML 标签时增加的
:::

上面只是基本的表格结构，`<caption>`用来定义表格的标题，放在表格之内

::: demo 带表头的表格

```html
<table> 
  <caption>标题</caption>
  <tr>
    <td>第一行第一个单元格</td>
    <td>第一行第二个单元格</td>
  </tr>
  <tr>
    <td>第二行第一个单元格</td>
    <td>第二行第二个单元格</td>
  </tr>
</table>
```

:::

### 语义化表格

`<thead>`,`<tbody>`,`<tfoot>`这三个标签实现了对表格的语义化布局，这样表格的结构更加清晰

::: demo 语义化表格

```html
<table> 
  <caption>标题</caption>
  <thead>
    <tr>
      <th>列一</th>
      <th>列二</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>第一行第一个单元格</td>
      <td>第一行第二个单元格</td>
    </tr>
    <tr>
      <td>第二行第一个单元格</td>
      <td>第二行第二个单元格</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>汇总一</td>
      <td>汇总二</td>
    </tr>
  </tfoot>
</table>
```

:::

::: tip
`<thead>`中没有使用`<td>`，而是使用`<th>`，这也是语义化的一部分，`<th>` 是一个特殊的`<td>`单元格，唯一的区别就是`<th>`中的字体会默认加粗
:::

综上所述，表格基本有如下几个标签构成：

1. table 标签定义外部框架
2. tr 标签定义行
3. th 标签定义表头单元格
4. td 标签定义单元格
5. caption 标签定义标题
6. thead 标签定义表头
7. tbody 标签定义主体部分
8. tfoot 标签定义页脚

### 表格的属性

表格中的元素自带一些属性，用于设置表格的样式

+ rowspan：设置`<td>`跨越的行数
+ colspan：设置`<td>`跨越的列数
+ cellspacing：设置`<td>`之间的间隙
+ cellpadding：设置`<td>`和内容之间的边距
+ border：设置表格的边框，默认值为 0，`border="1"`表示边框宽度是 1px
+ align：设置内容的对齐方式
+ bgcolor：设置表格的背景颜色

## 表单

表单用来收集用户的数据，提供了浏览者和网页交互的功能，`<form>`定义一个表单域，而其他与之关联表单元素则是给用户提供输入内容的，其中`<input>`是最重要的表单元素

::: demo 表单元素

```html
<form>
文本框：<input type="text"><br> 
密码框：<input type="password"><br> 
单选框：<input type="radio" name="sex"><input type="radio" name="sex"><br> 
多选框：<input type="checkbox"><input type="checkbox"><br>
普通按钮：<input type="button" value="点击"><br>
提交按钮：<input type="submit" value="提交"><br>
范围：<input type="range"><br>
重置：<input type="reset" name="reset"><br>
时间：<input type="time"><br>
日期：<input type="month"><br>
日期：<input type="date"><br>
文件：<input type="file"><br>
</form>
```

:::

改变`<input>`的`type`属性值就可以转换为不同的表单元素，无论以何种形式展现，它的功能是输入数据

### 其他表单元素

+ `<textarea>`提供了输入多行文本的能力
+ `<select>`和`<option>`提供了下拉列表
+ `<label>`提供了内容绑定元素的能力，默认情况下点击内容是不会聚焦到元素的，只要将`for`属性和表单元素的`id`值关联起来就可以实现绑定，也可以将表单元素放入`<label>`中实现，这样无需编写属性
+ `<datalist>`定义一个数据列表，描述`<input>`可能输入的值，将`id`值赋值给`<input>`的`list`属性即可实现绑定
::: demo 其他表单元素

```html
<textarea></textarea><br/>
<select>
  <option>选项一</option>
  <option>选项二</option>
  <option>选项三</option>
</select><br/>
<label for="account">账号：</label>
<input type="text" id="account"><br/>
<label>密码：<input type="password"></label><br/>
<input type="text" list="fruits"><br/>
<datalist id="fruits">
  <option value="车厘子">
  <option value="牛油果">
  <option value="红毛丹">
</datalist>
```

:::

### form 的属性

+ name：给表单命名，提供 JavaScript 获取`<form>`元素的手段
+ action：规定数据提交的目标页面
+ method：规定数据提交的方式，默认发送 GET 请求，
+ target：规定在何处打开`action`属性规定的 url

### input 的属性

对于`<input>`来说，不同的`type`对应的属性也不同

+ 当`type="text"`时，接收文本内容

1. name：给后台提供数据标识
2. value：规定文本域的属性值，也就是用户可见的内容
3. maxlength：规定文本域可以输入的最大字符数
4. placeholder：提供一些提示，描述所期待的值
5. pattern：规定用于验证文本域内容的正则表达式
6. form：规定一个输入域所属的一个或多个表单
7. autofocus：页面加载时，域自动获得焦点
8. autocomplete：规定文本域具有自动完成功能
9. readonly：设置文本域为只读
10. list：指定一个数据列表

+ 当`type="radio"`时，将所有的单选框 name 属性值设置成一样的就成为了一组，这样同一组单选框之间是互斥的，只能有一个单选框处于被选中状态

1. value：规定单选框的 value 属性值，它会被发送到服务器
2. checked：规定单选单选框处于选中状态
3. required：规定对应单选框是必选
4. form：规定单选框所属的一个或多个表单
5. autofocus：规定在页面加载时，对应单选框自动地获得焦点
6. disabled：规定单选框不可用

+ 当`type="checkbox"`时，复选框则可以选中任意多项

1. value：规定复选框的 value 属性值，它会被发送到服务器
2. checked：规定复选框处于选中状态
3. required：规定指定的复选框必须被选中
4. form：规定复选框所属的一个或多个表单
5. autofocus：规定在页面加载时，指定复选框自动地获得焦点
6. disabled：规定复选框不可用

### textarea 的属性

1. name：给后台提供数据标识
2. rows：规定多行文本框的行数
3. cols：规定多行文本框的列数
4. disabled：规定多行文本域是否可用
5. form：规定多行文本域所属的一个或多个表单
6. maxlength：规定文本域可以输入的最大字符数
7. placeholder（HTML5）：提供一种提示，描述所期待的值
8. readonly：设置文本域为只读
9. required：规定文本域内容是必填的
10. autofocus：规定文本域在页面加载后自动获取焦点
11. wrap：规定当在表单中提交时，文本区域中的文本如何换行

::: tip
不能使用`value`属性规定它的初始值
:::

### select 的属性

1. multiple：规定下拉列表可以选择多项，默认只能选择其中一项
2. size：规定下拉列表展开之后可见列表项的数目
3. selected：设置一个`<option>`项为默认选中状态

## 超链接

超链接是网页的核心内容之一，通过超链接可以实现站内页面或者站际页面之间的跳转，没有超链接的网站的可用性必然具有很大的局限性，超链接占据了网页中的大部分内容，在 HTML 中通过`<a>`标签来创建一个超链接，`href`属性指定要跳转的链接，链接类型不一定是网页链接，可以是 RSS 源、图像、文件等

::: demo 文本链接

```html
<a href="/web/html/1/">点击回到第一篇文章</a>
```

:::

a 标签的内容不一定是文本，也可以是图片，也可以是其他的一些内容

::: demo 图片链接

```html
<a href="/application/web/html/1/" target="_blank"><img src="/bgImage.jpg"></a>
```

:::

因为`<a>`标签有默认的 CSS 样式，导致当鼠标指针放在被`<a>`包裹内容上就会变成一个小手

主要的属性：

1. href：规定链接的跳转地址
2. download：规定下载文件的名称
3. target：规定跳转的页面在何处打开

::: tip target取值

+ _blank：在新窗口中打开
+ _self：默认值，在当前窗口打开
+ _parent：在包含当前子窗口的父窗口或者框架集中打开
+ _top：在整个窗口中打开
:::

### 锚点

使用`<a>`标签不仅能跳转指定页面，也可以跳转到页面中的指定位置，锚点也可以用于不同页面的位置

使用步骤：

1. 设置锚点链接
2. 设置锚点位置

+ 通过`id`来实现

```html
<a href="#标题">点击回到标题</a>
<div id="anchor">锚点位置</div>
```

::: demo 锚点

```html
<a href="#标题">定位到标题位置</a>
```

:::

+ 通过`name`，只能用于`<a>`标签

```html
<a href="#anchor">锚点链接</a>
<a name="anchor">锚点位置</a>
```

+ 通过 JavaScript 实现

### base

`<base>`标签中的`target`属性用于控制页面上所有的超链接跳转方式，必须写在`<head>`标签内，如果`<a>`标签有自己的`target`属性，则优先自己的`target`

### 假链接

假链接指的是点击后不会跳转的链接，通常用于开发中还未完成的页面中，当项目完成时则会替换为真链接，给`href`属性赋值`#`或者`javascrpt:`即可实现假链接

::: tip
点击`#`假链接会自动回到页面顶部，`javascript:`则不会
:::

## 图片

通过`<img>`标签就能在文档中插入一张图片，只需要告诉`src`属性的图片链接

::: demo img

```html
<img src="/bgImage.jpg">
```

:::

支持 JPEG、PNG、GIF、WebP、SVG 格式

## 多媒体

声音和视频都可以在 HTML 中播放，HTML5 新增了定义声音和视频的标签

### audio

`<audio>`是一个 HTML5 元素，通过`src`指定资源路径

::: demo audio

```html
<audio controls src="http://s138.ananas.chaoxing.com/audio/a0/e8/52/f814b5355ffd42e059187d3ce16cba1e/audio.mp3?at_=1612934735878&ak_=a25ecb672f06e77a5036d511788ea77e&ad_=579c22a2cf3594c71a75b17fab204e15">浏览器不支持</audio>
```

:::

它有一些自己的属性：

1. autoplay：会在音频就绪后马上播放
2. controls：会向用户显示播放控件（默认隐藏）
3. loop：会一直循环播放
4. muted：静音

### video

`<video>`是一个 HTML5 元素，通过`src`指定资源路径

::: demo video

```html
<video controls src="http://s138.ananas.chaoxing.com/video/c9/51/17/4a626b15b5abfa147da4af8084054c26/sd.mp4?at_=1612352532045&ak_=b3da89ddae922efb89270e7300931769&ad_=e36a6b4b68892a4f3b361772b5d8925c" width="222px">浏览器不支持</video>
```

:::

它有自己的属性：

1. autoplay：会在视频就绪后马上播放
2. controls：向用户显示播放控件（默认隐藏）
3. loop：会一直循环播放
4. muted：静音
5. width：设置播放器的宽度
6. height：设置播放器的高度
7. poster：设置视频在播放前显示图像

## div

在以前的 Web 开发中，页面逻辑并不复杂，用户的要求也不是很高，因此`<table>`标签被大量地运用到页面布局上，而`<table>`本质上就是一个展示数据的元素，用来做布局元素导致页面逻辑不够清晰，所以`<div>`标签是用来解耦这种行为的，这样页面更加清晰，代码组织更加合理，利于前端开发的分工合作。于是产生了“div + css”这种布局页面的模方式，`<div>`是一种容器级的标签，可以容纳任何内容，本身没有任何功能和样式

## span

`<span>`是一个文本级的容器标签，没有任何特殊功能以及样式，目的就是为包裹的文本来添加一些样式

## 进度

`progress`用于显示进度，支持三个属性：max、value 和 form，max 指定总进度，value 指定当前进度

::: demo 进度

```html
<progress max="100" value="30"></progress>
```

:::
