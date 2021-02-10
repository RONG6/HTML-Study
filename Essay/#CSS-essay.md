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

### 源码

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

