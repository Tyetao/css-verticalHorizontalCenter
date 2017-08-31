# css-verticalHorizontalCenter
css5种实现垂直水平居中
#### html结构
```html
 <div class="parent">
    <div class="child">
      子元素
    </div>
<div>
```
#### css结构
>1、定位实现
```css
    .parent {
      position: relative;
      width: 200px;
      height: 200px;
      border: 1px solid red;
    }
    .child {
      position: absolute;/*子元素为绝对定位*/
      width: 100px;
      height: 100px;
      top: 0;
      bottom: 0;
      left: 0;
      right: 0;
      margin: auto;/*margin设置为auto*/
      border: 1px solid black;
    }
```
>2、table-cell实现
```css
    .parent {
      width: 200px;
      height: 200px;
      border: 1px solid red;
      display: table-cell;
      vertical-align: middle;/*实现垂直居中*/
    }
    .child {
      width: 100px;
      height: 100px;
      border: 1px solid black;
      margin: 0 auto; /*实现水平居中*/
    }
```

>3、flex实现
```css
    .parent {
      width: 200px;
      height: 200px;
      border: 1px solid red;
      display: flex;
      align-items: center;/*实现垂直居中*/
      justify-content: center;/*实现水平居中*/
    }
    .child {
      width: 100px;
      height: 100px;
      border: 1px solid green;
    }
```
>4 translate+relative定位
```css
  .parent {
      width: 200px;
      height: 200px;
      border: 1px solid red;
    }
    .child {
      width: 100px;
      height: 100px;
      border: 1px solid black;
      position: relative;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);/*偏移自身的宽和高的-50%*/
      /*下面这方法也可以但是要明确自身的高度*/
      /* margin-top: -100px;
      margin-left: -100px; */
    }
```
#### 效果
![image](https://github.com/Tyetao/css-verticalHorizontalCenter/屏幕快照 2017-08-31 10.21.18.png)
