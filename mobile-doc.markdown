# Mobile Web开发

标签（空格分隔）： mobile

---

### 基本模板
```html
    <!DOCTYPE html>
    <html lang="zh-cn">
      <head>
        <meta charset="utf-8" />
        <meta http-equiv="X-UA-Compatible" content="IE=edge" />
        <meta name="viewport" content="width=device-width, initial-scale=1" />
        <!--IOS中Safari允许全屏浏览-->
        <meta content="yes" name="apple-mobile-web-app-capable" />
        <!--IOS中Safari顶端状态条样式-->
        <meta content="black" name="apple-mobile-web-app-status-bar-style" />
        <title>mobile web developer</title>
        <link href="css/demo.css" rel="stylesheet" />
      </head>
      <body>
        <h1>你好，世界！</h1>
      </body>
    </html>
```

### 基础概念

 1. `1`css pixels = `2`device pixels
 2. DPI(每英寸所拥有的像素`device pixels`数目)的计算方法：
    ![dpi_image](http://img.educity.cn/img_15/273/2014030418/611180242.jpg)
 3.  密度决定比例
    ![dpi_image](http://img.educity.cn/img_15/273/2014030418/612180242.jpg)
 4. 通过前面三点，就可以决定我们的页面制作需要参考多大的尺寸了
 5. viewport的使用
    target-densitydpi=device-dpi的设置使得`1`css pixels = `1`device pixels

### 3S原则

    Simple、Small、Speedy。
    功能简易，设计优雅，图片、代码小而简洁、优化性能以达到页面性能最优的效果。

### 调试工具

    谷歌浏览器 --> F12打开控制台 --> 底部状态栏Emulation标签

### 响应式开发

 1. 媒体查询media
 2. 流式布局
 3. 图片自适应

### 性能优化

 1. 减少DOM层级嵌套（用尽可能少的标签实现页面效果）
 2. 减少http请求数
 3. 使用css3代替图片
 4. 减少Reflow和Repaint
 5. 优化图片（图片格式的选择、css sprites、大小压缩等）

### 资料收集

 1. -webkit-box-flex布局方案
 
```html
    <div class="box">
      <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
      </ul>
    </div>
```
```css
    .box{width: 600px; height: 400px; margin: 10px auto; font-size: 0;}
    .box ul{display: -webkit-box; background: #000;}
    .box li{height: 100px; line-height: 100px; text-align: center; font-size: 16px; -webkit-box-flex: 1;}
    .box li:first-child{background: #f00;}
    .box li:nth-child(2){background: #ff0; margin-left: 10px;}
    .box li:first-child{background: #c96;}
```
效果如下图：
![file-list](http://sc.chinaz.com/upload/2013/04/10/2013041009140619.png)
 2. 禁止手机横屏时字号调整
 
```css
    .box{-webkit-text-size-adjust: 100%;}
```

 3.字体单位
建议使用`rem`设置字号，该单位根据`root`为基准 

[1]： http://wenku.baidu.com/link?url=kU00-0hZO8X1-RaURxOlZqb5t5ire98HSY4Ymh-nq5dd79xTRGxQ5hMLpGrFrZQWZV--Gph7vqKl8ayeng8C9yo-R5DAdstcXVVwiQjArva&pn=1


