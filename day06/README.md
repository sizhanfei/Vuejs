过滤器
========

## 知识点

* filters

### filters

格式化变量内容的输出。（日期格式化，字母大小写，数字再计算等等）<br>
filterBy过滤器 : 过滤器的值必须是一个数组，filterBy + 过滤条件。过滤条件是：'string || function'+ in 'optionKeyName'
~~~html
<div id="myApp">
    <p>{{message}}</p>
    <p>{{message | toupper }}</p>
    <hr>
    <p>现在的vue.js学习进度是{{num}}({{num | topercentage}})。</p>
</div>
<script>
    var myApp = new Vue({
        el: '#myApp',
        data: {
            message: 'hello vue.js world.',
            num: 0.3
        },
        filters: {
            toupper: function(value){
                return value.toUpperCase();
            },
            topercentage: function(value){
                return value * 100 + '%';
            },
        },
    });
</script>
~~~
