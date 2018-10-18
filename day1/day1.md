# 前端入门——day1（简介及推荐书籍和网站）

![html5-css-javascript-logos](https://user-images.githubusercontent.com/22407219/47126388-eacf3c00-d2ba-11e8-980a-7f44e8804c22.png)

## 写给谁
这篇文章写给想要入门前端或者刚入门前端的小白~
如果是已经工作好几年的小伙伴们可以直接跳过这一系列文章啦。

## 为啥写这篇文章
终于决定给自己挖这个坑了，之前一直没打算写这样的系列文章。回想起自己的前端历程，走了不少弯路，希望这个系列的文章可以帮小白们少走弯路，快速入门。

## 不同的地方
- 不会一天一更，因为白天要上班，晚上回去还要忙着准备一些其他的事情，会尽量做到两到三天一更，大家见谅啦~
- 不会有很多很复杂的概念，我会用自己的语言表达出来，尽量精简，容易理解。
- 会结合自己实际开发中用到的一切，讲自己踩过的坑，要注意的点，尽量做到把我会的都教给大家。
- 不讲太旧的东西，像IE6兼容的问题之类的，需求已经很少很少了。
- 会推荐合适的书，合适的网站给大家学习

## 开始咯
### 什么是前端，前端要做什么
嘿嘿嘿，简单来说，你正在浏览的这个网页，上面的按钮，文字，图片之类的，都是前端工程师展现给你看的。这样的页面又叫H5页面，通常来说，前端负责页面的展示和页面逻辑，后端负责提供数据，比如数据库的增删改查等等。

### 前端要学哪些东西
说实话，很多，目前实际开发中，一个前端要学以下东西（甚至更多）：
- 基础： HTML + CSS + Javascript
- 框架： Vue或者React或者Angular （一般学一个即可，建议可学Vue, 后面的文章也只会讲Vue）
- 打包工具： webpack或者gulp或者grunt （主流是Webpack）
- npm: 包管理（会用就行，不必深究）
- git: 版本控制工具（多人协作开发时）

是不是有点慌，哈哈哈不着急，一个一个来。

事实上当你学会了`基础`，那么就可以进行网页开发了，而且也能在很短的时间内学会框架，而一旦掌握了基础和框架，那么正式开发中所需要的技能就基本上都具备了，`其他的东西都是一些工具。`

所以，`基础最重要。`今天就讲讲基础，该怎么学，有哪些好的学习资源以及要看哪些书。

### 准备工作
下载并安装[Vscode][2]，Vscode是一款超赞的IDE，所谓IDE就是用来写代码的工具，提供代码高亮补全之类的功能，反正就是前端开发必备啦！

### 关于HTML，Javascript，CSS的关系
这三个代表三种不同的语言，也对应着三种不同的文件，分别以`.html, .js, .css`结尾。这三种文件组合起来就形成了我们所看到的网页。`相辅相成，负责不同的功能。`
拿盖房子来类比：
- HTML就是搭建好的毛坯房，搭好了架子，样子丑丑的，里边也住不了人，因为里边啥也没有，电器啥的都没有。
- CSS就是搞装修，把网页整的漂漂亮亮的。
- Javascript就是控制房子里的逻辑，比如说打开门，打开空调，打开电视机等等等等。

所以:

- HTML负责网页的基本架构，你想要在页面上有个按钮，就需要在HTML文件里写一个`<button>点我</button> `标签
- css负责网页的美化，比如设置按钮的背景色，`background-color: red;`
- Javascrip负责控制点击按钮发生的事情，比如点击时出现一个警告窗。

### 把三种文件连接起来

- 新建一个文件夹，用vscode打开这个文件夹，然后在该文件夹下分别新建`day1.html, day1.css, day1.js`三个文件。
- 在`day1.html`里输入一个感叹号`!`然后按下`tab`键（注意该感叹号是英文的感叹号，而不是中文的），会自动生成下面的HTML代码。
```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="X-UA-Compatible" content="ie=edge">
	<title>Document</title>
</head>
<body>
	
</body>
</html>
```
- 然后在`<body></body>`之间添加一个button标签`<button class="my-button">点我</button>`,这样就可以显示出一个按钮。
- 在title的下面添加`<link rel="stylesheet" href="./day1.css">`,这样就引入了CSS文件。
- 在`</body>`的上面一行添加`<script src="./day1.js"></script>`,这样就引入了Js文件。得到的最终代码如下：
```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="X-UA-Compatible" content="ie=edge">
	<title>Document</title>
	<link rel="stylesheet" href="./day1.css">
</head>
<body>
	<button class="my-button">点我</button>
	<script src="./day1.js"></script>
</body>
</html>
```
 
这样我们便把这三种不同的文件连接起来了，虽然目前CSS和JS里什么都没有，后面再具体往里边加东西。现在你可以用浏览器打开`day1.html`看下样子了

`ps: script标签和link标签里的./代表当前目录下，如果想表示上一层目录则要用../`

### HTML
HTML入门真的花不了多少时间，要明白以下几点就好了。
- HTML是一门标签语言，即由一个个标签组成，通常是一对组成一个元素，比如`<button>点我</button>`，注意后面的button前有个斜杠，代表是闭合。
- 也有不需要闭合的标签，比如`<link rel="stylesheet" href="./day1.css">`
- 标签是可以嵌套的，比如link标签就是嵌套在head标签里的。
- 你如果想增加页面的内容，那就在`body`标签里新增标签，head里内嵌的标签是不会显示在页面上的，因此我们通常只需要在body标签里写东西。

推荐入门网站:

[HTML-如果你英文还可以，能翻墙，点这里][3]

[HTML-如果你喜欢看中文，点这里][4]

学习方法很简单，照着教程，一个一个敲，然后看效果,大概一天能看完。

推荐书籍：
不推荐，这么简单的东西看看文档就可以搞定了。

### CSS
先在day1.css中写下以下代码:
```
.my-button {
    background-color: #add8e6;
}
```
然后在浏览器中打开`day1.html`，会发现我们按钮背景色变成了浅蓝色。解释一下：
- 在HTML的button上添加的class叫`类`，类的名字叫`my-button`
- css中的`.my-button`中的`“.”`表示类选择器，意思是选中类名为my-button的元素。
- `#add8e6`是16进制表示颜色的方法，也可以使用rgb的表示法，还可以使用一些内置的颜色，比如red。

推荐入门网站：

[CSS-英文教程][5]

[CSS-中文教程][6]

一些需要着重注意的点：
- 要搞懂盒子模型,即下面这张图：
![default](https://user-images.githubusercontent.com/22407219/47126485-6204d000-d2bb-11e8-9b2f-1bb1ad6cf6b4.PNG)

- 要搞懂选择器有很多种，但是最常用的是类选择器和id选择器，还有`nth-child`选择器很实用，你可以都了解一下。
- 要搞懂display属性，尤其注意`inline`, `inline-block`, `block`之间的区别
- 要搞懂定位的影响，即`position`属性，搞懂相对于谁定位。
- 初期少用浮动（`float`），因为很多人用错地方，也不懂怎么清除浮动。
- 教程里的的内容，可以先跳过一些，看完`CSS Tutorial`和`CSS Advanced`就可以了，节约时间，剩下的有空再看。另外弹性布局(flex)也可以先跳过，虽然非常非常好用！！！后面单独拿一章讲。


在过教程看到相关内容时，要带着上面这些问题去看。

### Javascript
打开`day1.js`,添加以下代码:
```
document.querySelector('.my-button').addEventListener('click', function () {
  alert('Hello, World!!')
})
```

解释一下：
- `document.querySelector('.my-button')`表示找到HTML中，类名为my-button的元素
- `addEventListener`表示给这个元素添加事件监听器，事件名为`click`，即点击事件。当这个元素被点击时，调用后面的匿名函数，弹出警示窗。

相对于HTML，CSS来说，Javascript才更像一门真正的语言，就像C语言那样。
对前端来说，核心中的核心是Javascript，因为它控制整个页面的逻辑，从而与用户进行交互。

推荐网站：

[Javascript-英文教程][7]

[Javascipt-中文教程][8]

推荐书籍：
1. [《JavaScript DOM编程艺术 （第2版）》][9] 这本书很薄，很容易读完，入门书最佳。
2. [《JavaScript高级程序设计（第3版）》][10] 传说中的红宝书，比较厚，耐心阅读。

`ps: 推荐新人《Javascript权威指南》这本书的人通通乱棍打死，这本书绝对绝对不适合作为入门书籍，以上两本书就足够入门到较合格的前端开发了`

`ps: 请先跳过闭包！！难度较大，而且初级开发中用到的地方很少，需要的时候再去深入。适当的退步是为了更快的前进`

### 最后

安利一个在线编程学习网站，也是英文的，很适合入门。[Codecademy][11]
总结下学习方法：
- 对于基础的东西，去我推荐的网站，一个一个看，一个一个敲，`不需要强记`，留个印象，后面会越用越熟练。
- 不同的阶段看不同的书，入门前端只需要过完我推荐的网站，同时看推荐的两本书 ，就够了，越专注入门越快。
- 进步最快的方式永远是跟着敲，不要满足于看了。
- 遇到问题先谷歌，实在不懂了可以来提问，有时间会帮大家解答。


  [2]: https://code.visualstudio.com/
  [3]: https://www.w3schools.com/html/default.asp
  [4]: http://www.runoob.com/html/html-tutorial.html
  [5]: https://www.w3schools.com/css/default.asp
  [6]: http://www.runoob.com/css/css-tutorial.html
  [7]: https://www.w3schools.com/js/js_arithmetic.asp
  [8]: http://www.runoob.com/js/js-tutorial.html
  [9]: https://book.douban.com/subject/6038371/
  [10]: https://book.douban.com/subject/10546125/
  [11]: https://www.codecademy.com/catalog/language/javascript
