---
title: JavaScript
category: 编程语言
tag: JavaScript
author: JQiue
---

膜拜一下作者`”Brendan Eich“`

<div align="center"><img src="https://gitee.com/jqiue/img_upload/raw/master/images/13073857_FIRG.jpg"></div>

## 为什么要学习JavaScript

仅仅只是HTML和CSS写出来的网页是没有灵魂的，简直就是白痴，无法和用户交互行为，JavaScript就是用来解决交互问题的

为了发挥 JavaScript 的全部潜力，了解它的本质、历史及局限性是十分重要的

JavaScript是一门动态弱类型语言

## 实现

JavaScript是由ECMAScript，DOM，BOM组成的

ECMAScript描述了该语言的语法和基本对象

DOM 描述了处理网页内容的方法和接口；

BOM 描述了与浏览器进行交互的方法和接口。

### ECMAScript、DOM 和 BOM

尽管 ECMAScript 是一个重要的标准，但它并不是 JavaScript 唯一的部分，当然，也不是唯一被标准化的部分。实际上，一个完整的 JavaScript 实现是由以下 3 个不同部分组成的：

![](https://www.w3school.com.cn/i/ct_js_JavaScript_ECMAScript_DOM_BOM.gif)

由于JavaScript设计的初衷是为了操作DOM，因此它必须依赖于浏览器运行

### ECMAScript

ECMAScript 并不与任何具体浏览器相绑定，实际上，它也没有提到用于任何用户输入输出的方法（这点与 C 这类语言不同，它需要依赖外部的库来完成这类任务）。那么什么才是 ECMAScript 呢？ECMA-262 标准（第 2 段）的描述如下：

“ECMAScript 可以为不同种类的宿主环境提供核心的脚本编程能力，因此核心的脚本语言是与任何特定的宿主环境分开进行规定的... ...”
Web 浏览器对于 ECMAScript 来说是一个宿主环境，但它并不是唯一的宿主环境。事实上，还有不计其数的其他各种环境（例如 Nombas 的 ScriptEase，以及 Macromedia 同时用在 Flash 和 Director MX 中的 ActionScript）可以容纳 ECMAScript 实现。那么 ECMAScript 在浏览器之外规定了些什么呢？

简单地说，ECMAScript 描述了以下内容：

+ 语法
+ 类型
+ 语句
+ 关键字
+ 保留字
+ 运算符
+ 对象

ECMAScript 仅仅是一个描述，定义了脚本语言的所有属性、方法和对象。其他语言可以实现 ECMAScript 来作为功能的基准，JavaScript 就是这样：

![](https://www.w3school.com.cn/i/ct_js_ECMAScript_JavaScript_ActionScript_ScriptEase.gif)

每个浏览器都有它自己的 ECMAScript 接口的实现，然后这个实现又被扩展，包含了 DOM 和 BOM（在以下几节中再探讨）。当然还有其他实现并扩展了 ECMAScript 的语言，例如 Windows 脚本宿主（Windows Scripting Host, WSH）、Macromedia 在 Flash 和 Director MX 中的 ActionScript，以及 Nombas ScriptEase。

## 基本结构

```javascript
<script type="text/javascript">
  //code...
</script>
```

## 使用方式

1. 直接在HTML标签中使用

```html
<button onclick="aleat('点我干嘛')">别点我!</button>
```

2. 在页面的任意位置使用script标签插入js

```html
<script type="text/javascript">
  //javascript code...
</script>
```

3. 引入外部js文件

```html
<script src= "index.js" type="text/javascript"></script>
```

::: warning
1. JS代码可以放在页面的任意位置使用，但是放置的位置不同，将影响JS执行的顺序
2. 引入外部JS的script标签中，不能再包含任何的JS代码
:::