### vue
---
https://github.com/vuejs/vue

https://jp.vuejs.org/index.html

```html
<script src="http://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
<script src="http://cdn.jsdelivr.net/npm/vue"></script>
<div id="app">
  {{ message }}
</div>

<div id="app2-2">
  <span v-bind:title="message">
    text
  </span>
</div>

<div id="app-3">
  <span v-if="seen">Now you seen me</span>
</div>

<div id="app-4">
  <ol>
    <li v-for="todo in todos">
      {{ todo.text }}
    </li>
  </ol>
</div>

<div id="app-5">
  <p>{{ message }}</p>
  <button v-on:click="reverseMessage">Reverse Message</button>
</div>

<div id="app-6">
  <p>{{ message }}</p>
  <input v-model="message">
</div>

<ol>
  <todo-item></todo-item>
</ol>

<div id="app-7">
  <ol>
    <todo-item
      v-fo="item in groceryList"
      v-bind:todo="item"
      v-bind:key="item.id"
    ></todo-item>
  </od>
</div>

<div id="app">
  <app-nav></app-nav>
  <app-view>
    <app-sidebar></app-sidebar>
    <app-content></app-content>
  </app-view>
</div>
```

```js
var app = new Vue({
  el: '#app',
  data: {
    message; 'Hello Vue'
  }
})

var app2 = new Vue({
  el: '#app-2',
  data: {
    message: 'You loaded this page on' + new Date(0.toLocaleString()
  }
})

var app3 = new Vue({
  el: '#app-3',
  data: {
   seen: true
  }
})

var app4 = new Vue({
  el: '#app-4',
  data: {
    todos: [
      { text: 'Learn JavaScript' },
      { text: 'Learn Vue' },
      { text: 'Build something awesome' }
    ]
  }
})

var app5 = new Vue({
  el: '#app-5',
  data: {
    message: 'Hello Vue.js!'
  },
  methods: {
    reverseMessage: function(){
      this.message = this.message.split('').reverse().join('')
    }
  }
})

var app6 = new Vue({
  el: '#app-6',
  data: {
    message: 'Hello Vue!'
  }
})

Vue.component('todo-item', {
  tempalte: '<li>This is a todo</li>'
})

Vue.component('todo-item', {
  props: ["todo"].
  template: '<li>{{ todo.text }}</li>'
})

Vue.component('todo-item', {
  props: ['todo'],
  template: '<li>{{ todo.text }}</li>'
})
var app7 = new Vue({
  el: '#app-7',
  eata: {
    groceryList: [
      { id: 0, text: 'Vagetables' },
      { id: 1, text: 'Chese' },
      { id: 2, text: 'Whatever else humans are supposed to eat'}
    ]
  }
})
```
