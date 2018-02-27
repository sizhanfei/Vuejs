从index.html开始
========

## 知识点

* html5的基础知识
* vue.js导入
* Vue对象的创建

## index.html

从第一个index.html开始吧！

### vue.js引用

~~~html
<script src="https://unpkg.com/vue/dist/vue.js"></script>
~~~

### html代码块

~~~html
<div id="myApp">
  {{ message }}
</div>
~~~

### javascript脚本部分

~~~javascript
var myApp = new Vue({
  el: '#myApp',
  data: {
    message: 'Hello Vue.js World!'
  }
});
~~~

## 完整代码
~~~
<!DOCTYPE html>
<html lang="zh">

<head>
    <title></title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <script src="https://unpkg.com/vue/dist/vue.js"></script>
</head>

<body>
    <div id="myApp"> {{ message }} </div>
    <script>
        var myApp = new Vue({
            el: '#myApp'
            , data: {
                message: 'Hello World! from szftime'
            }
        });
    </script>
</body>

</html>
~~~
