# CSS样式引入方式和选择器

@(HTML+CSS知识)


## 1.css样式引入方式（面试题）
1）行内式（直接写在标签里面）
```
<div style="color:#000; backhround:red"></div>

style="属性名：属性值；属性名：属性值"
```
2）引入式
```
<style type="text/css">
标签(h2){
    属性名：属性值；
    属性名：属性值；
   ........
   }
   </style>
```
3）外联式（是项目中最常用的一种办法）
   页面里面可以引用多个样式表
```
  link 按下table 会自动生成下面的代码
  <link rel="stylesheet" href=""/>
```
4）导入式
```
 <style type="text/css">
        @import "css/index.css";

 </style>

```
5）引入式和导入式的区别
  导入式在前 引入式在后（代码有报错提示）

css属性样式  :
  如果给同一个标签同一个属性，就近原则。
  如果给不同标签加属性，所加样式都会起作用。
```
 <style type="text/css">
       导入式
       引入式

 </style>

```
6) 外联式和内嵌式
      顺序可以任意放
       内嵌式 外联式（遵循就近原则，下面的覆盖上面的）
   
      <style type="text/css">
                  外联式
                  内嵌式（显示内嵌式）
 
         </style>

## 2.选择器
### 选择器的样式用法
       选择器{
               属性名：属性值；
               属性名：属性值；
               ......          
             }

>1）.box 类选择器（class选择器）
>2） 标签选择器。例如（h1   p   ul   li  .......）
>3）id选择器 例如：#box
>4） * 通配符选择器（选中也面的所有标签元素）
>5)   后代选择器（后面最好不超过4个）
例如
```
    <style type="textcss">
         .box1 p{
                 样式
              }
           </style>
<div class="box clearfix">
    <div class="box1">
          <p>我是谁</P>
</div>
    <div class="box2">
          <p>谁是我</p>
</div>
    <!--<div class="clear"></div>-->
</div>
```
>6）  分组（并集）选择器( 中间用逗号隔开)
```

    <style type="textcss">
         .box1 p, .box2 p{
                 样式
              }
           </style>
<div class="box clearfix">
    <div class="box1">
          <p>我是谁</P>
</div>
    <div class="box2">
          <p>谁是我</p>
</div>
    <!--<div class="clear"></div>-->
</div>
```
>7）属性选择器

>属性可以自己加 

>例如：
[属性（title）或者属性加属性值（title=“文字”）]
```
     <p    title=“文字”>
       <p  age=“17”>
      <p   name=“title”>

{
  （title）
  （17）
  （文字）                样式 
}
```
>8）伪元素选择器

>：after /：before
```
 <style type="text/css">
        .box:before{
            display: block;
            content: "珠峰培训后面的内容";
        }
        .box:after{
            display: block;
            content: "珠峰培训后面的内容";
        }
    </style>

<div class="box">
    <p>珠峰培训</p>
</div>
```
>9）  相邻兄弟选择器(只对p后面的h2起作用)
```
<styl type="textcss">
       p+h2{
           font-size:12px;   
      }
       
        </style>
<div class="box">
    <p>珠峰培训</p>
    <h2>1122</h2>
</div>
```
>权重                   （值）
类选择器           100
id选择器            10
标签选择器         1
通配符选择器      0
后代选择器      
                     例如：.box p
                                 值是101（前面的类选择器+                                                                                              
                                                   后面的标签选择   
                                                   器）                                             