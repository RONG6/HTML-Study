# CSS

- 网页分为三个部分

  ​    结构（HTML）

  ​    表现（CSS）

  ​    行为（JavaScript）

- CSS

  ​    -层叠样式表

  ​    -网页实际是一个多层的结构，通过CSS可以分别为网页的每层设置样式

  ​      而最终只能看到网页上最上边一层

  ​    -总之，CSS用来设置网页中元素的样式
  
## 外部样式表
- 外部样式表
       -可以将CSS样式编写到外部的CSS文件中
           通过link标签引入外部的CSS文件
       -外部样式表需要link标签来引入（必须在head中引用）
            意味着只要想使用这些样式的网页都可以对其引用
             使杨舍可以在不同的页面中进行复用
       -将样式编写到外部的CSS文件中，可以使用到浏览器的缓存机制
           从而加快网页的加载速度，提高用户体验

  ```html
<link rel="stylesheet" href="路径">
  ```

## CSS基本语法

- 在style标签中写CSS

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
    /*这里写CSS语句*/
    </style>
</head>
<body>
    
</body>
</html>
```

- CSS基本语法：

  ​      选择器 声明块

  ​      

  ​      选择器，通过选择器可以选中页面中的指定元素

  

  ​      声明块，通过声明块来指定元素设置的样式

  ​            声明块有一个一个的声明组成

  ​            声明是一个名值对结构

  ​            一个样式名对应一个样式值，名和值之间以 : 连接，以 ; 结尾

  ```css
  p{
               color: green;
               font-size: 40px;
    }
  ```

  

## 常用选择器

### 元素选择器

- 作用：根据标签名选中指定元素

```css
 p{
            color: red;
   }
h1{
    color: green;
}
```



### ID选择器

- 作用：根据id的属性值选中一个元素
- 语法：#id属性值{}

```html
<style>
    #p1{
        color: red;
    }
</style>
<body>
    <p id="p1">我是P标签</p>
</body>
```

### 类选择器

- 作用：根据元素的class值选中一组元素
- 语法：.class属性值

```html
<style>
    .blue{
        font-size: 30px;
}
    .abc{
        color: red;
    }
</style>
<body>
    <p class="blue">乡音难改鬓毛衰</p>
    <p class="blue">儿童相见不相识</p>
    <p class="blue abc">笑问客从何处来</p>
    <!-- 可以使用多个class 名之间用空格隔开 任意一个名都可以进行控制 -->
</body>
```



### 通配选择器

- 作用：选中页面中所有的元素
- 语法：*

```html
<style>
    *{color: red;}
</style>
<body>
   <h1>我是标题！</h1>
    <p id="p1">少小离家老大回</p>
    <p class="blue">乡音难改鬓毛衰</p>
    <p class="blue">儿童相见不相识</p>
    <p class="blue abc">笑问客从何处来</p>
    <!-- 可以使用多个class 名之间用空格隔开 任意一个名都可以进行控制 -->
    <p>秋水共长天一色</p>
    <p>落霞与孤鹜齐飞</p>
</body>
```

### .....

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        /*
        将所有的段落设置为红色（字体颜色）

        元素选择器
            作用：根据标签名选中指定元素

        */

      /*  p{
            color: red;
        }
        h1{
            color: rgb(green, green, red);
        }*/

        /* 
        将第一句变成红色
        id选择器：
            作用：根据id的属性值选中一个元素
            语法：#id属性值{}
        */
        /*
        #p1{
            color: red;
        }*/

        /* 
            讲第二句和第三局变成蓝色
            class标签，和id类似，不同的是class可以重复使用

            类选择器
                作用：根据元素的class属性值选中一组元素
                语法：.class属性值{}

        */
        .blue{
            color: blue;  
        }
        /* 
            通配选择器
                作用:选用页面中的所有元素
                语法:*
        */
        *{
            color: red;
        }
        
    </style>
</head>
<body>
    <h1>我是标题！</h1>
    <p id="p1">少小离家老大回</p>
    <p class="blue">乡音难改鬓毛衰</p>
    <p class="blue">儿童相见不相识</p>
    <p class="blue abc">笑问客从何处来</p>
    <!-- 可以使用多个class 名之间用空格隔开 任意一个名都可以进行控制 -->
    <p>秋水共长天一色</p>
    <p>落霞与孤鹜齐飞</p>
</body>
</html>
```

## 复合选择器

### 交集选择器

- 作用：选中同时符合多个条件的元素
- 语法：选择器1选择器2选择器n{}
- 注意点：交集选择器中如果有元素选择器，必须使用元素选择器开头

```html
<style>
    div.red{color: red;}/*将 我市div 设置为红色*/
</style>
<body>
    <h1>我说我是h1</h1>
    <div class="red">我是div</div>
    <p class="red">我说p元素</p>
    <p id="a">我是a p标签</p>
    <span>我是span</span>
</body>
```



### 并集选择器

- 作用：同事选中多个选择器对应的元素
- 语法：选择器1,选择器2,选择器n{}

```html
<style>
    h1,span{color: green;}
    #a,.red{color: yellow;}
</style>
<body>
    <h1>我说我是h1</h1>
    <div class="red">我是div</div>
    <p class="red">我说p元素</p>
    <p id="a">我是a p标签</p>
    <span>我是span</span>
</body>
```



## 关系选择器

### 关系

- 父元素

  ​	-直接包含子元素的元素叫父元素

- 子元素

  ​	-直接被父元素包含的元素叫子元素

- 祖先元素

  ​	-直接或间接包含后代元素的元素叫祖先元素

  ​    -一个元素的父元素也是它的祖先元素

- 后代元素

  ​	-直接或间接被祖先元素包含的元素叫后代元素

  ​    -子元素也是后代元素

- 兄弟元素

  ​	-拥有相同元素的元素是兄弟元素

### 子元素选择器

- 作用：选中指定父元素的子元素
- 语法：父元素>子元素

```html
div.a>span{color: red;}
```

### 后代元素选择器

- 作用：选中指元素内指定后代元素
- 语法：祖先 后台

```html
div span{color: blue;}
或者
div>p>span{color: blue;}
```

### 兄弟选择器(☆只针对后面的元素)

- 选择下一个兄弟(只选择下一个兄弟)

  ​	-语法：前一个+后一个

```html
p + span{color: black;}
```

- 选择后面所有的兄弟

  ​	-语法：前一个~后一个

```html
p ~ span{color: black:}
```

```html
<style>
    div.a>span{color: red;}/*子元素选择器*/
    div span{color: blue;}/*后代元素选择器 或者 div>p>span{color: blue;}*/
    p + span{color: black;}/*兄弟选择器（1）*/
    p ~ span{color: yellow;}/*兄弟选择器（2）*/
</style>
<body>
    <div class="a">
        我是一个div
        <p>我是div的p元素
            <span>&nbsp;&nbsp; 我是p元素中的span</span>
        </p>
        <span>我是div中的span元素</span>
    </div>
    <span>我是div的外部元素</span>
    
</body>
```



## 属性选择器

- [属性名]选择含有指定属性的元素
- [属性名=属性值]选择含有指定属性和属性值得元
- [属性名^=属性值] 选择属性值以指定值开头的元素
- [属性名$=属性值]选择属性值以指定值结尾的元素
- [属性名*=属性值]选择属性值中含有某值得元素的元素

```html
<style>
    /* 
        [属性名]选择含有指定属性的元素
        [属性名=属性值]选择含有指定属性和属性值得元素
        [属性名^=属性值] 选择属性值以指定值开头的元素
        [属性名$=属性值]选择属性值以指定值结尾的元素
        [属性名*=属性值]选择属性值中含有某值得元素的元素
    */
	p[title]{ color: red;}
	p[title=p2]{color: blue;}
	p[title^=p]{color: green;}
	p[title$=a]{color: pink;} 
	p[title*=a]{color: yellow;}
</style>
<body>
    <p title="提示文字">少小离家老大回</p>
    <p title="p2a">乡音难改鬓毛衰</p>
    <p title="p3a">儿童相见不相识</p>
    <p title="p4a">笑问客从何处来</p>
    <p title="a5">秋水共长天一色</p>
    <p title="a6">落霞与孤鹜齐飞</p>
</body>
```

## 伪类选择器

- 伪类选择器（特殊的类）

  ​	-描述一个元素的特殊状态

  ​		比如：第一个元素、被点击的元素、鼠标移入的元素....

- 伪类一般情况下都是 : 开头

  ​      ：first-child 第一个子元素 

  ​      ：last-child 最后一个子元素

  ​      ：nth-child() 选中第n个子元素

  ​        -特殊值：

  ​            n 全部

  ​            2n或even 选中偶数类的元素

  ​            2n+1或odd 表示奇数位的元素

- 以上伪类都是根据所有的子元素进行排序



  - :first-of-type

  ​      :last-of-type

  ​      :nth-of-type()

  ​        -这几个伪类的宏能和上述的类似，不同点是他们在同类型元素中进行排序

  

- ：not()否定伪类

  ​       -将符合条件的元素从选择器中去除

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <style>
        /* 讲第一个li设置为红色 */
        ul>li:first-child{color: red;}
        ul>li:nth-child(3){color: red;}
        ul>li:not(3){color: brown;}
       
    </style>
</head>
<body>
<ul>
    <span>我是一个span</span>
    <li>第0个</li>
    <li>第一个</li>
    <li>第二个</li>
    <li>第三个</li>
    <li>第四个</li>
    <li>第五个</li>
</ul>
</body>
</html>
```

## 超链接(a标签)的伪类

### 超链接独有

- :link 用来表示没有访问过的链接（正常的链接）

  ```css
  a:link{color: red;}
  ```

- :visited 用来表示访问过的链接

  ​	-由于隐私的原因，所以visited这个伪类只能修改链接的颜色，其他都不能修改

  ```css
  a:visited
  {
               color: orange;
               /* font-size: 50px;   不能设置，隐私原因 */
  }
  ```

  ### 所有标签共有

- :hover 用来表示鼠标移入的状态

    ```css
    a:hover{color: orange; font-size: 10px;}
    ```

- :active 用来表示鼠标点击的状态 (正在点击的状态）)

    ```css
               a:active{color: yellow;}
    ```

    

