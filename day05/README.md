组件
========

## 知识点

* component

### component

定义页面的局部区域块，完成单独的页面**小**功能。
每个页面中几个独立的板块，或者是互相调用的板块组合在一起。

~~~html
<div id="myApp">
  <ol>
    <game-item v-for="item in games" v-bind:game="item"></game-item>
  </ol>
</div>
<script>
/* 组件定义：game-item */
Vue.component('game-item', {
  props: ['game'],
  template: '<li>{{ game.title }}</li>'
});
/* Vue对象实例化 */
var myApp = new Vue({
  el: '#myApp',
  data: {
    games: [
      { title: '斗地主' },
      { title: '打麻雀' },
      { title: 'UNO' }
    ]
  }
});
</script>
~~~
