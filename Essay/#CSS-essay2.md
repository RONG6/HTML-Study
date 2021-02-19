CSS

## 文档流
- 网页是一个多层的结构
- 这些层中最底下的一层成为文档流，文档流是网页的基础所创建的元素默认都是在文档流中进行排列

- 对于我们来说，元素主要有两个状态
    在文档流中
    不在文档流中（脱离文档流）

- 元素在文档流中有什么特点
	-块元素

​          块元素会在页面中独占一行

​          默认宽度是父元素的全部

​          默认高度是被内容撑开（子元素）

​        -行内元素

​          行内元素不会独占页面一行，只占自身大小
​          行内元素在页面中自左向右水平排列，若果一行之中不能容纳下所有的行内元素，则元素会换到第二行继续自左向右排列
​	       行内元素的默认宽度和高度都是被内容撑开

```html
<body>
    <div class="div1">我是div1</div>
     <div class="div2">我是div2</div>
     <span>我是span1</span>
     <span>我是span2</span>
</body>
```

## 盒模型
- CSS将页面中的所有元素都设置为了一个矩形的盒子
- 将元素设置为矩形以后，对页面的布局就变成了摆放到不同的位置（网页的布局）
- 每一个盒子都由以下几个部分组成：
	内容区（content）
        内边距（padding）
        边框（border）
        外边距（margin）
 ```css
/*内容区，元素中的所有的子元素和文本内容都在内容区排列
      内容区的大小有width和heigth两个属性来设置
         width 设置内容区的宽度
         height 设置内容区的高度
*/
	width:200px;
	height: 200px;
	background-color: #bfa;
 ```
- 边框，属于盒子的边缘，边框里边属于盒子内部，
- ★边框的大小会影响整个盒子的大小
- 设置边框，至少需要三个样式
      边框的宽度：border-width
          的颜色：border-color
          的样式：border-style （虚线还是实线）

### 边框

- 边框的宽度：border-width
	 
	```css
	border-width: 10px;/*不写默认为3px*/
	/* 
	            border-width 可以用来指定四个方向的边框的宽度
	                值的情况
	                    四个值：上右下左 
	                    三个值：上 左右 下
	                    两个值：上下 左右
	                    一个值：上下左右
	            除了border-width还有一组 border-xxx-width
	                xxx可以是 top rigth bottom left单独用来指定某一个边的宽度
	                */
	            border-width: 10px 20px 30px 40px;
	```
	
- 边框的颜色：border-color

   ​	规则和border-width一样

- 边框的样式：border-style

   ​        solid表示实线

   ​        dotted 点状虚线

   ​        dashed 虚线

   ​        double 双线 

   ​        none 表示没有任何值

   ```css
   border-style: solid;
   ```

- ★border的简写属性，可以同时设置边框所有的相关样式

   ```css
   border: 10px solid red;
   /*若不想要右边*/
   border-rigth: none;/*none 表示不设置任何值*/
   ```

### 内边距

- 内容区和边框间的距离是内边距

- 一共有四个方向的内边距

  -padding-top/rigth/bottom/left

- 内边距的设置会影响盒子的大小

- 背景颜色会延伸到内边距上

-  一个盒子的可见框的大小,由内容区 内边距和 边框共同决定,所以在计算盒子大小时,需要将这三个区域加到一起计算

- padding 用法和border一样

- 简写属性，规则同上

  ```css
  padding: 10px 20px 30px 49px;
  ```

- ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <meta http-equiv="X-UA-Compatible" content="IE=edge">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Document</title>
      <style>
          .box1{
              width: 200px;
              height: 200px;
              background-color: #bfa;
              border: 3px orange solid;
  
              /* 
                  内边距（padding）
                      -内容区和边框间的距离是内边距
                      -一共有四个方向的内边距
                          padding-top
                          padding-rigth/bottom/left
                      -内边距的设置会影响盒子的大小
                      -背景颜色会延伸到内边距上
                  一个盒子的可见框的大小,由内容区 内边距和 边框共同决定,
                      所以在计算盒子大小时,需要将这三个区域加到一起计算
              */
              /* padding-top: 100px;
              padding-left: 100px;
              padding-bottom: 100px;
              padding-right: 100; */
  
              /* padding 内边距的简写属性，规则和border一样 */
              padding：10px 20px 30px 40px;
  
          }
          .inner{
              width: 100%;
              height: 100%;
              background-color: yellow;/*内容区*/
          }
      </style>
  </head>
  <body>
      <div class="box1">
          <div class="inner"></div>
      </div>
  </body>
  </html>
  ```

- 

