# css引用

#### 1.三种样式引入规则

1.  内联样式

    行内样式直接写在标签的style属性上

    ```javascript
      <!-- 内联(行内)样式：<标签 style="属性1:属性值1;属性2:属性值2;属性3:属性值3;...">内容</标签> -->
        <p style="font-size: 20px;color: hotpink;">我是内联(行内)样式</p>

    ```
2.  内部样式表

    样式放在head或body标签的style标签中

    ```javascript
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>CSS三种引入方式</title>
    <style>
             /* 内部样式：
           选择器 {
                属性1: 属性值1;
                属性2: 属性值2;
                ...
            } */
            div {
                font-size: 30px;
                color: aqua;
            }
    </style>
    </head>
    <body>
        <div>我是内部样式</div>
    </body>
    </html>

    ```
3.  外部样式表

    单独的样式文件以.css为后缀名，通过\<link/>引入

    ```javascript
    <!DOCTYPE html>
    <html lang="en">

    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>CSS三种引入方式</title>
          <!-- 外部样式：<link rel="stylesheet" href="css文件的路径"> -->
          <!-- 外部样式要单独创建一个CSS文件然后通过link的href填写正确的CSS文件的路径，
          否则外部样式没有效果 -->
        <link rel="stylesheet" href="../CSS/myCss.css">
    </head>

    <body>
        <section>我是外部样式</section>
    </body>

    </html>

    ```

#### 2. 样式引入的优先级

一般情况下，优先级如下：

内联样式>内部样式=外部样式>浏览器默认样式
