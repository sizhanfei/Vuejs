计算属性
========

## 知识点

* computed

### computed

处理元数据，便于进行二次利用。（比如：消费税自动计算功能）
~~~html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>Vue 测试实例 - szftime</title>
<script src="https://cdn.bootcss.com/vue/2.2.2/vue.min.js"></script>
</head>
<body>
<div id="app">
  <p>原始字符串: {{ message }}</p>
  <p>计算后反转字符串: {{ reversedMessage }}</p>
</div>

<script>
var vm = new Vue({
  el: '#app',
  data: {
    message: 'Runoob!'
  },
  computed: {
    // 计算属性的 getter
    reversedMessage: function () {
      // `this` 指向 vm 实例
      return this.message.split('').reverse().join('')
    }
  }
})
</script>
</body>
</html>
~~~
实例中声明了一个计算属性 reversedMessage 。

提供的函数将用作属性 vm.reversedMessage 的 getter 。

vm.reversedMessage 依赖于 vm.message，在 vm.message 发生改变时，vm.reversedMessage 也会更新。

~~~html
<div id="myApp">
    今年3月3日发卖的任天堂新一代主机Switch的价格是：{{price}}円，含税价格为：{{priceInTax}}円，折合人民币为：{{priceChinaRMB}}元。
</div>
<script>
    var myApp = new Vue({
        el: '#myApp',
        data: {
            price: 29980
        },
        computed: {
            priceInTax: function(){
                return this.price * 1.08;
            },
            priceChinaRMB: function(){
                return Math.round(this.priceInTax / 16.75);
            },
        },
    });
</script>
~~~
