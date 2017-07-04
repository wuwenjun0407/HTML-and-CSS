# HTML表单标签和CSS样式属性

@(HTML+CSS知识)


## HTML标签
1.input type
```v 
 .regList .regIpt：focus(光标移到input里{文本或密码输入框等}，显示边框颜色)
1）text(文本)例如：
   例如：
   <input type="text"/>  
                                 2）  password   (密码)  
   例如：                                 
   <input type="password"/>  

3） checkbox(复选框) 前面加id
   例如：
   <input id="name" type="checkbox"/><label for="name">我同意</label>
                                   4）radio(单选框)   
    例如：                               
    <input type="radio"/>男
    
    <input type="radio"/>女   
                          
5）button(按钮)
    例如：
    <input type="button" value="登录"/>                              <input type="button" value="登录"/>
                                      6）file(文件) 
    例如：                                
    <input type="file"/>   
                               7）submit(提交)
    例如：                         
    <input type="submit"/>提交
8）reset(重置)    
    <input type="reset"/>

9）select  下拉菜单
       用于填写个人信息，出生日期 城市等
<select name="" id="">
    <option value="">2017</option>
    <option value="">2016</option>
    <option value="">2015</option>
    <option value="">2014</option>
    </select>  
10）textarea  多行文本输入 cols:表示行 
                     rows:表示列
    resize:none  (彻底禁止拖动)                    
<textarea name="" id="" cols="30" rows="10"></textarea>  
```

## CSS样式

1.width     宽度
2.height    高度
   margin 外边距  水平居中（margin：0 auto）
   padding 内边距
 取值|方向|
:---:|:---:|
一个值（margin/padding）：40px）  |上 右 下 左|
两个值|上下  左右|
三个值|上   左右    下
四个值|上  右  下   左(顺时针方向)

3.background  背景（复合属性）
### 背景类

   background-color 背景颜色
   background-image 背景图片
   background-position  背景位置
   background-attachment  背景位置固定
   background-repeat  背景平不平铺
  
  属性值|描述|
  :---: |---:|
  repeat-x|x轴平铺|
  repeat-y|y轴平铺|
  no-repeat|图片不平铺
  repeat|x,y同时平铺
 background： url("css/pic/bd_logo1.png")          
                        no-repeat  100px 100px fixed      
                                                                    
   background: 图片路径地址 图片平不平铺 
                        图片的位置 图片位置固定
   background: {rgba:" 0 0 0 .65 "}(前面三个0是色值  后面.65是透明度  表示65%)
                        
4.border    
### 边框类
边框（border：10px solid red）

边框阴影：
```
              box-shadow: 1px(x轴) 1px    （y轴）0 （阴影）2px(模糊深度，值越大，阴影的会变大)
           #e5e5e5;（阴影颜色）
```              
boder-radius：圆角
```
 边框的类型：
       solid 实线边框
       dashed 虚线边框
       dotted  圆点边框 ```      
```

 属性值|描述|代表意思|
:---:|:---:|:---:|
10px|solid|red|
变宽的宽度|边框的类型|颜色值|


### 文本类

text-align：center ；  水平居中
text-align：left ；       靠左
text-align：right ；     靠右
line-height：#；（“#”如果和高度一样，垂直居中）                             行高
text-indent：文本前面的空格
letter-spacing:  文本间距

### 子元素在父元素中两端对齐
```
让li两端对齐必须加在父级元素ul
.navList{
  
    text-align: justify;(文本两端对齐)
    text-justify:distribute-all-lines;
    （在一行分布）
    -ms-text-justify: distribute-all-
    lines;
    （兼容）
}
.navList:after{
    width: 100%;
    height: 0;
    margin: 0;
    display: inline-block;
    overflow: hidden;
    content: '';
}
.navList li{
    display:inline-block;
}
```

