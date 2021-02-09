# HTML

## 初入HTML

```HTML
<html>
    <head><!--子标签1-->
        <title>这是标签</title>//网页标题
    </head>
  <body>/网页主体，所有可见内容。
      这是网页所有内容。
    </body>
</html><!--根标签-->

<!-- 
HTML的注释码
-->

<img><!-- 单个标签-->
<ing /> <!--自结束标签-->
```

## 标签的属性

```HTML
<html>
    <head>
        <title>标签的属性</title>
    </head>
    <body>
        
    <!--
        属性，在标签中（开始标签或自结束标签）还可以设置属性
            属性是一个名值对（x=y）
          属性是用来设置标签中的内容如何显示
            属性和标签名或其他属性应该使用空格隔开
            属性不能瞎写，根据文档中的规定编写
            有些属性有属性值，有些没有.如果有属性值，属性应该使用引号引起来 
      -->
        <h1>这是我的<font color="red" size='3'>第一个网页</font></h1>
    </body>
</html>
```

## 文档声明

```html
<!doctype html>  <!-- 声明-->
<html>
    <head>
        <title></title>    
    </head>
    <body>
        <!--
        迭代
            网页的版本
                HTML4
                HTML5
            文档声明（doctype）
                  -文档声明用来告诉浏览器当前的网页版本
                  -HTML5的文档声明
                    <!doctype html>
			-->
    </body>
</html>
```



## 进制&字符编码

```html
<!doctype html>  <!-- 声明-->
<html>
    <head>
        <!--可以通过meta标签设置网页的字符集，避免乱码问题-->
        <meta charset="utf-8"> <!--告诉浏览器是 utf-8编码编写-->
        <title></title>
    </head>
    <body>
        <!--
		进制：
              十进制(日常使用)：
                 -特点：满10进1；
                 -计数：0 1 2 3 4 5 6 7 8 9 10 11
			    -单位数字：10个（0~9）
              二进制(计算机底层的进制)：
				-特点：满2进1；
				-计数：0 1 10 11 100 101 110 111
				-单位数字：2个（0~1）
				-扩展：
					-所有数据在计算机底层都会以二进制的形式保存
					
			八进制(很少用):
				-特点：满8进1；
				-计数：0 1 2 3 4 5 6 7 10 11 12...17 20
				-单位数字：8个（0~7）
			十六进制(一般显示一个二进制的数字是，都会转换为十六进制)：
				-特点：满16进1；
				-计数 0 1 ..9 a(11) b c d e f .... 1a 1b 1c 1d 1e 1f ...
				-单位数字：16个（0~9）
		字符编码：
			-编码
				-将字符转化为二进制的过程为编码
			-解码
				-将二进制转化为字符的过程为解码
			-字符集(charser)
				-编码和解码所采用的的规则成为字符集
			-常见的字符集
				ASCII
				ISO88591
				GB2312
				GBK
				UTF-8(万国码)
	-->
    </body>
</html>
```

## 文档的使用

- zeal 文档

```html
<!doctype html>  <!-- 文档声明-->
<!--html的根标签（元素）-->
<html>
    <!--head 是网页的头部，head中的内容不会在网页中直接出现，
		主要用来帮助浏览器或搜索引擎来解析网页-->
    <head>
        <!--meta标签用来设置网页的元数据-->
         <meta charset="utf-8"> <!--告诉浏览器是 utf-8编码编写--> 
        <!--title中的内容会显示在浏览器的标题栏，搜索引擎会主要根据title的
			的内容来判断网页的主要内容-->
        <title>网页的标题</title>
    </head>
    <body>
        
    </body>

</html>
```

## 实体

-    如果我们需要在网页中书写一些特殊的符号，则需要使用html中的实体（转义字符）

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>实体</title>
</head>
<body>
    <!--
        在网页中编写多个空格默认情况会被浏览器解析为一个空格
        在HTML中有些时候，我们不能直接书写一些特殊符号，例如
        多个练习的空格、字母两侧的大于和小于号<>
    -->
    <p>今天&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;天气真不错</p>
    <p>
        <!--
            如果我们需要在网页中书写一些特殊的符号，则需要使用html
            中的实体（转义字符）
            &实体的名字：
                &nbsp;空格
                &gt;大于号
                &lt;小于号
                &copy;版权符号©
        -->
        a&nbsp;
    </p>
</body>
</html>
```

## meta标签

- meta主要用于设置网页中的一些元数据，元数据是给计算机看的；
- 写在< head >里。

```html
<!DOCTYPE html>
<html lang="zh"><!--语言为中文-->
<head>
    <meta charset="UTF-8">
    <!--
        meta主要用于设置网页中的一些元数据，元数据是给计算机看的；
        charset 指定网页的字符集
        name 指定的是数据的名词
        content 指定的数据的内容
    -->


    <meta name="keyworlds" content="HTML5,前端，CSS">
    <!--                            关键字，关键字，关键字
        keyworlds 搜索关键字 
        content 关键字，关键字间用逗号隔开
    -->


    <meta name="description" content="描述">
    <!--
        description 用于指定网站的描述
    -->


    <meta http-equiv="refresh" content="3;url=https://www.baidu.com">
    <!--
         <meta http-equiv="refresh" content="3;url=https://www.baidu.com">
         将页面重定向到另一个网站。
    -->

    
        <title>Document</title>
    <!--
        title 标签的内容会作为搜索结果的超链接上的文字显示
    -->

</head>
<body>
    
</body>
</html>
```



## 语义化标签

- 块元素：1.在页面中独占一行的元素。（block element）

  ​			  2. 在网页中一般通过块元素来对页面进行布局

- 行内元素：1. 不会独占一行的元素

  				2.  行内元素主要用来包裹文字
     				3.  一般情况下会在块元素中放行内元素，而不会在行内元素中放块元

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <!--
        在网页中HTML专门用来负责网页结构
        所以在使用html标签时，应该关注的是标签的语义，而不是它的样式。
        h1在网页中的重要性仅次于title标签，一般下一个页面只会有一个h1
        一般只用到h1~h3

        在页面中独占一行的元素称为块元素（block element）
    -->
    <h1>一级标题</h1>
    <h2>二级标题</h2>
    <h3>三级标题</h3>
    <h4>四级标题</h4>
    <h5>五级标题</h5>
    <h6>六级标题</h6>



    <!--
         <hgroup>
        <h1>回乡偶书其二</h1>
        <h2>其一</h2>
        </hgroup>
        hgroup 标签用来为标题分组，可以将一组相关的标题放到group里。
    -->
    <hgroup>
        <h1>回乡偶书其二</h1>
        <h2>其一</h2>
    </hgroup>
    



    <!--
        p标签表示页面中的一个段落
        p标签也是一个块元素
    -->
    <p>在p标签中的内容就会显示一个段落</p>

    <!--
        em--表示斜体
        strong--加粗
        b--加粗
        q--引号
        br--换行

        在页面中不会独占一行的元素称为行内元素。eg.em是行内元素。
                                               p是块元素。
    -->
    <p>今天天气<em>真</em>不<strong>错</strong>！</p>
    <p>今天天气<br>真不<b>错</b>！</p>
</body>
</html>
```

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">

    <title>Document</title>
</head>
<body>
    <!--
        块元素
            -在网页中一般通过块元素来对页面进行布局
        行内元素（inline element）
            -行内元素主要用来包裹文字
            -一般情况下会在块元素中放行内元素，而不会在行内元素中放块元素
            -p元素中不能放任何块元素
        
        浏览器在解析网页时。会自动对网页中不符合规范的内容进行修正
            比如：
                标签卸载了根元素的外部
                p元素中嵌套了块元素
                根元素中出现一除head和body以外的子元素
        -->
        <p>haha
            <h1>我就要写在p元素里面</h1>
        </p>
</body>
</html>
```

- header 表示网页的头部
- main 表示网页的主体部分（一个页面中只会有一个main）
- footer 表示网页的底部 
- aside 表示和主体相关的其他内容（侧边栏）
- article 表示一个独立的文章
- section 表示一个独立的区块，上边的标签都不能表示时使用section
- div 没有语义，就用来表示一个区块，目前来讲div还是我们主要的布局元素
- span 行内元素，没有任何语义，一般用于网页中选中文字

```html
 <!--
        header 表示网页的头部
        main 表示网页的主体部分（一个页面中只会有一个main）
        footer 表示网页的底部
        nav 表示网页中的导航
        aside 表示和主体相关的其他内容（侧边栏）
        article 表示一个独立的文章
        section 表示一个独立的区块，上边的标签都不能表示时使用section
        div 没有语义，就用来表示一个区块，目前来讲div还是我们主要的布局元素
        span 行内元素，没有任何语义，一般用于网页中选中文字
    -->
    <header></header>
    <main></main>
    <footer></footer>
    <nav></nav>
    <aside></aside>
    <article></article>
    <section></section>
    <div></div>
    <span></span>
```

## 列表

1. 有序列表
   - 使用ol标签来创建有序列表---使用ol表示列表项
2. 无序列表
   - 使用ul标签来创建无序列表---使用li表示列表项
3. 定义列表
   - 使用dl标签来创建一个定义列表
     使用dt来表示定义的内容
     使用dd来对内容进行解释说明
4. 列表之间可以互相嵌套

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <!--
        列表（list）
        HTML中列表一共有三种
            1、有序列表
            2、无序列表
            3、定义列表
        
        有序列表，使用ol标签来创建有序列表
            使用ol表示列表项
        无序列表，使用ul标签来创建无序列表
            使用li表示列表项
        定义列表，使用dl标签来创建一个定义列表
            使用dt来表示定义的内容
            使用dd来对内容进行解释说明

        列表之间可以互相嵌套
    -->
    <ol>行为</ol>
    <ol>表现</ol>
    <ol>行为</ol>

    <li>结构</li>
    <li>表现</li>
    <li>行为</li>
<dl>
    <dt>结构</dt>
    <dd>结构表示网页的内容，结构用来规定网页中哪里是标题，那里是段落</dd>

</dl>

    <!--列表之间可以互相嵌套-->
<ul>
    <li>
        aa
        <ul>
            <li>aa-1</li>
        </ul>
    </li>
</ul>

</body>
</html>
```

## 超链接

- 使用a标签来定义超链接

  ​			属性：

  ​				href 指定跳转的目标路径

- 超链接--行内元素，在a标签中可以嵌套除它自身外的任何元素

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <!--
        alt+shift+方向键 快速复制
        超链接
            使用a标签来定义超链接
                属性：
                    href 指定跳转的目标路径
                        -值可以是一个外部网站的地址

        超链接也是一个行内元素，在a标签中可以嵌套除它自身外的任何元素

    -->
    <a href="https://www.baidu.com">超链接</a>
    <br><br><!--br*n  就是创建几个br标签-->
    <a href="08.列表.html">超链接2</a> 
</body>
</html>
```

### 相对路径

- 相对路径会使用 . or .. 开头

  ​			./

  ​			../

  ./可以省略，如果不写./也不写../ 则相当于写了./

- ./ 表示当前文件所在目录

- ../ 表示当前文件所在目录的上一级目录

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <!--
        当我们需要跳转到一个服务器内部的页面时，一般会使用相对路径
            相对路径都会使用.or..开头
                ./
                ../
            ./可以省略，如果不写./也不写../则相当于写了./

            ./ 表示当前文件所在目录
            ../ 表示当前文件所在目录的上一级目录
    -->
    <a href="./08.列表.html">超链接1</a> <!--找不到，不在同意路径-->
    <a href="../08.列表.html">超链接2</a> <!--../ 表示当前文件所在目录的上一级-->
    <br><br>
    <a href="./inner/index.html">超链接3</a> 
</body>
</html>
```

