# 100 Days Of Code - Log


![Thursday](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/Vuetify%20day%2079.png)

### Day 79: October 11, Thursday

**Today 's Progress**: Created a Form in Vuetify for Vue.JS

**Thoughts**: I had oral surgery today! I did not want to code but after 78 days of straight coding I had to try Vuetify seems pretty cool.

### Resources used:
  * [Vuetify](https://vuetifyjs.com/en/getting-started/quick-start)
  * [Vue.js.org](https://vuejs.org/)

```Html
<!DOCTYPE html>
<html>
<head>
  <link href="https://fonts.googleapis.com/css?family=Roboto:100,300,400,500,700,900|Material+Icons" rel="stylesheet">
  <link href="https://cdn.jsdelivr.net/npm/vuetify/dist/vuetify.min.css" rel="stylesheet">
  <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no, minimal-ui">
</head>
<body>
  <div id="app">
  <v-container grid-list-md text-xs-center>
    <v-app id="inspire">
      <v-form ref="form" v-model="valid" lazy-validation>
        <v-text-field
          v-model="name"
          :rules="nameRules"
          :counter="10"
          label="Name"
          required
        ></v-text-field>
        <v-text-field
          v-model="email"
          :rules="emailRules"
          label="E-mail"
          required
        ></v-text-field>
        <v-select
          v-model="select"
          :items="items"
          :rules="[v => !!v || 'Item is required']"
          label="Item"
          required
        ></v-select>
        <v-checkbox
          v-model="checkbox"
          :rules="[v => !!v || 'You must agree to continue!']"
          label="Do you agree?"
          required
        ></v-checkbox>

        <v-btn
          :disabled="!valid"
          @click="submit"
        >
          submit
        </v-btn>
        <v-btn @click="clear">clear</v-btn>
      </v-form>
    </v-app>
    </v-container>
  </div>

  <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/vuetify/dist/vuetify.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/babel-polyfill/dist/polyfill.min.js"></script>
  <script>
  new Vue({
  el: '#app',
  data: () => ({
    valid: true,
    name: '',
    nameRules: [
      v => !!v || 'Name is required',
      v => (v && v.length <= 25) || 'Name must be less than 25 characters'
    ],
    email: '',
    emailRules: [
      v => !!v || 'E-mail is required',
      v => /.+@.+/.test(v) || 'E-mail must be valid'
    ],
    select: null,
    items: [
      'Could not access Page',
      'User experiance Good',
      'User experiance Bad',
      'User experiance Ugly'
    ],
    checkbox: false
  }),

  methods: {
    submit () {
      if (this.$refs.form.validate()) {
        // Native form submission is not yet supported
        axios.post('/api/submit', {
          name: this.name,
          email: this.email,
          select: this.select,
          checkbox: this.checkbox
        })
      }
    },
    clear () {
      this.$refs.form.reset()
    }
  }
})
  </script>
</body>
</html>
```
A little light coding in incredible pain!.


**Link(s) to work**

1. Working on learning vuetifyjs application in local environment.

Code is at local not yet in github.



![Wednesday](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/Vuetify%20day78.png)

## Day 78: October 10, Wednesday

**Today 's Progress**: Doing a little exploration into Vuetify for Vue.JS

**Thoughts**: I watched this [Three Vue.js Vuetify Tips (Grid System, Buttons, Alerts)](https://www.youtube.com/watch?v=FpnvRNkQTY4) and started looking at Vuetify.

### Resources used:
  * [Vuetify](https://vuetifyjs.com/en/getting-started/quick-start)
  * [Vue.js.org](https://vuejs.org/)

```Html
<!DOCTYPE html>
<html>
<head>
  <link href='https://fonts.googleapis.com/css?family=Roboto:300,400,500,700|Material+Icons' rel="stylesheet">
  <link href="https://cdn.jsdelivr.net/npm/vuetify/dist/vuetify.min.css" rel="stylesheet">
  <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no, minimal-ui">
</head>
<body>
  <div id="app">
    <v-app>
      <v-content>
        <v-container><h1>{{hello}}</h1></v-container>
      </v-content>
    </v-app>
  </div>

  <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/vuetify/dist/vuetify.js"></script>
  <script>
    new Vue({
        el: '#app',
        data(){
            return {
                hello:"Hello World!"
            }
        }
    })
  </script>
</body>
</html>
```
A little light coding.


**Link(s) to work**

1. Working on learning vuetifyjs application in local environment.

Code is at local not yet in github.



![Tuesday](http://obrienspubsbrandon.com/wp-content/uploads/2018/07/Taco-Tuesday.jpg)

## Day 77: October 09, Tuesday

**Today 's Progress**: Next steps are deploying my local app now that its working in a local dev environment. I need to find a way to deploy it.

**Thoughts**: I read some on using CA certifications and Testing VUE apps. I will have to learn how to deploy my app.

### Resources used:
  * [Github repo for todoApp](https://github.com/Johnny2136/my-todo-app)
  * [Vue.js.org](https://vuejs.org/)
  * [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html)

It works... learning deployment.


**Link(s) to work**

1. Working on my TODO application in local environment.

Code is at [https://github.com/Johnny2136/my-todo-app](https://github.com/Johnny2136/my-todo-app).

![Monday](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/Debugging7.png)

### Day 76: October 08, Monday

**Today 's Progress**: Great progress on my VUE.js todo app its working!!!!!! [Vue.js Todo App - Basics - Part 1](https://www.youtube.com/watch?v=A5S23KS_-bU)and [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html) working in a local dev environment. Upgraded to VUE 3.0, Working at last!!!!!

**Thoughts**: I added my first todo list here[VueApp](https://jsfiddle.net/johnny2136/br7qzL1t/2/) to a local Git file and use Vue-CLI 3.0 after going though more videos I am finally starting to get it, cautiously optimistic. Debugging continues.

### Resources used:
  * [Github repo for todoApp](https://github.com/Johnny2136/my-todo-app)
  * [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)
  * [Vue.js.org](https://vuejs.org/)
  * [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html)

It works... more refactoring and debugging tomorrow. PROGRESS!!!!

```html
{{/* eslint-disable */}}
<template>
 <div>
    <input type="text" class="todo-input" placeholder="What needs to be done" v-model="newTodo" @keyup.enter="addTodo">
    <transition-group name="fade" enter-active-class="animated fadeInUp" leave-active-class="animated fadeOutDown">
    <div v-for="(todo, index) in todosFiltered" :key="todo.id" class="todo-item">
      <div class="todo-item-left">
        <input type="checkbox" v-model="todo.completed">
        <div v-if="!todo.editing" @dblclick="editTodo(todo)" class="todo-item-label" :class="{ completed : todo.completed }">{{ todo.title }}</div>
        <input v-else class="todo-item-edit" type="text" v-model="todo.title" @blur="doneEdit(todo)" @keyup.enter="doneEdit(todo)" @keyup.esc="cancelEdit(todo)" v-focus>
      </div>
      <div class="remove-item" @click="removeTodo(index)">
        &times;
      </div>
    </div>
    </transition-group>

    <div class="extra-container">
      <div><label><input type="checkbox" :checked="!anyRemaining" @change="checkAllTodos"> Check All</label></div>
      <div>{{ remaining }} items left</div>
    </div>

    <div class="extra-container">
      <div>
        <button :class="{ active: filter == 'all' }" @click="filter = 'all'">All</button>
        <button :class="{ active: filter == 'active' }" @click="filter = 'active'">Active</button>
        <button :class="{ active: filter == 'completed' }" @click="filter = 'completed'">Completed</button>
      </div>

      <div>
        <transition name="fade">
        <button v-if="showClearCompletedButton" @click="clearCompleted">Clear Completed</button>
        </transition>
      </div>

    </div>
  </div>
</template>
<script>
/* eslint-disable */
export default {
  name: 'todo-list',
  data () {
    return {
      newTodo: '',
      idForTodo: 3,
      beforeEditCache: '',
      filter: 'all',
      todos: [
        {
          'id': 1,
          'title': 'Finish Vue Screencast',
          'completed': false,
          'editing': false,
        },
        {
          'id': 2,
          'title': 'Take over world',
          'completed': false,
          'editing': false,
        },
      ]
    }
  },
  computed: {
    remaining() {
      return this.todos.filter(todo => !todo.completed).length
    },
    anyRemaining() {
      return this.remaining != 0
    },
    todosFiltered() {
      if (this.filter == 'all') {
        return this.todos
      } else if (this.filter == 'active') {
        return this.todos.filter(todo => !todo.completed)
      } else if (this.filter == 'completed') {
        return this.todos.filter(todo => todo.completed)
      }
      return this.todos
    },
    showClearCompletedButton() {
      return this.todos.filter(todo => todo.completed).length > 0
    }
  },
  directives: {
    focus: {
      inserted: function (el) {
        el.focus()
      }
    }
  },
  methods: {
    addTodo() {
      if (this.newTodo.trim().length == 0) {
        return
      }
      this.todos.push({
        id: this.idForTodo,
        title: this.newTodo,
        completed: false,
        editing: false,
      })
      this.newTodo = ''
      this.idForTodo++
    },
    editTodo(todo) {
      this.beforeEditCache = todo.title
      todo.editing = true
    },
    doneEdit(todo) {
      if (todo.title.trim() == '') {
        todo.title = this.beforeEditCache
      }
      todo.editing = false
    },
    cancelEdit(todo) {
      todo.title = this.beforeEditCache
      todo.editing = false
    },
    removeTodo(index) {
      this.todos.splice(index, 1)
    },
    checkAllTodos() {
      this.todos.forEach((todo) => todo.completed = event.target.checked)
    },
    clearCompleted() {
      this.todos = this.todos.filter(todo => !todo.completed)
    }
  }
}
</script>
<style lang="scss">
@import url("https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.5.2/animate.min.css");
  .todo-input {
    font-family: "Comic Sans MS", cursive, sans-serif;
    width: 100%;
    padding: 10px 18px;
    font-size: 18px;
    margin-bottom: 16px;
    &:focus {
      outline: 0;
    }
  }
  .todo-item {
    font-family: "Comic Sans MS", cursive, sans-serif;
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    animation-duration: 0.3s;
  }
  .remove-item {
    cursor: pointer;
    margin-left: 14px;
    &:hover {
      color: black;
    }
  }
  .todo-item-left { // later
    display: flex;
    align-items: center;
  }
  .todo-item-label {
    padding: 10px;
    border: 1px solid white;
    margin-left: 12px;
  }
  .todo-item-edit {
    font-size: 24px;
    color: #2c3e50;
    margin-left: 12px;
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc; //override defaults
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    &:focus {
      outline: none;
    }
  }
  .completed {
    text-decoration: line-through;
    color: grey;
  }
  .extra-container {
    font-family: "Comic Sans MS", cursive, sans-serif;
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-size: 16px;
    border-top: 1px solid lightgrey;
    padding-top: 14px;
    margin-bottom: 14px;
  }
  button {
    font-family: "Comic Sans MS", cursive, sans-serif;
    padding: 5px 35px;
    font-size: 14px;
    background-color: white;
    appearance: none;
    &:hover {
      background: lightblue;
    }
    &:focus {
      outline: none;
    }
  }
  .active {
    background: lightblue;
  }
  // CSS Transitions
  .fade-enter-active, .fade-leave-active {
    transition: opacity .2s;
  }
  .fade-enter, .fade-leave-to {
    opacity: 0;
  }
</style>
```

**Link(s) to work**

1. Working on my TODO application in local environment.

Code is at [https://github.com/Johnny2136/my-todo-app](https://github.com/Johnny2136/my-todo-app).

![Sunday](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/Debugging6.png)

### Day 75: October 07, Sunday

**Today 's Progress**: Making headway on my Vue todo app slow progress but progress none the less [Vue.js Todo App - Basics - Part 1](https://www.youtube.com/watch?v=A5S23KS_-bU)and [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html) ported into a local dev environment. Upgraded to VUE 3.0, Working somewhat...

**Thoughts**: I am tiring to add my first todo list here[VueApp](https://jsfiddle.net/johnny2136/br7qzL1t/2/) to a local Git file and use Vue-CLI 3.0 after going though more videos I am still struggling but starting to get it, cautiously optimistic. Debugging continues.

### Resources used:
  * [Github repo for todoApp](https://github.com/Johnny2136/my-todo-app)
  * [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)
  * [Vue.js.org](https://vuejs.org/)
  * [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html)

It compiles renders and shows tasks... more refactoring and debugging tomorrow. PROGRESS!!!!

```html
<template>
<div>
    <h2> My Vue.JS ToDo List:</h2>
     <input type="text" class="todo-input" placeholder="Add what needs to be done here!" v-model="newTodo" @keyup.enter="addTodo">     
      <div v-for="todo in todos" :key="todo.id" class="todo-item">
        {{todo.title}}
      </div>
</div>
</template>
<script>
/* eslint-disable */
export default {
  name: 'todo-list',
  data () {
    return {
        newTodo: '',
        idForTodo: 3,
        beforeEditCache: '',
        filter: 'all',
        todos: [
        {
          'id': 1,
          'title': 'Finish Vue ToDo Project',
          'completed': false,
          'editing': false,
        },
        {
          'id': 2,
          'title': 'Grok Vue-CLI',
          'completed': false,
          'editing': false,
        },
      ]
    }
  },
  methods: {
    addTodo() {
      //alert('adding todo')
      if (this.newTodo.trim().length == 0) {
        return
      }
      this.todos.push({
        id: this.idForTodo,
        title: this.newTodo,
        completed: false,
        editing: false,
      })
      this.newTodo = ''
      this.idForTodo++
    },
  },
 }

</script>
<style lang="scss">
@import url("https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.5.2/animate.min.css");
  .todo-input {
    width: 100%;
    padding: 10px 18px;
    font-size: 18px;
    margin-bottom: 16px;
    &:focus {
      outline: 0;
    }
  }
  .todo-item {
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    animation-duration: 0.3s;
  }
  .remove-item {
    cursor: pointer;
    margin-left: 14px;
    &:hover {
      color: black;
    }
  }
  .todo-item-left { // later
    display: flex;
    align-items: center;
  }
  .todo-item-label {
    padding: 10px;
    border: 1px solid white;
    margin-left: 12px;
  }
  .todo-item-edit {
    font-size: 24px;
    color: #2c3e50;
    margin-left: 12px;
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc; //override defaults
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    &:focus {
      outline: none;
    }
  }
  .completed {
    text-decoration: line-through;
    color: grey;
  }
  .extra-container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-size: 16px;
    border-top: 1px solid lightgrey;
    padding-top: 14px;
    margin-bottom: 14px;
  }
  button {
    font-size: 14px;
    background-color: white;
    appearance: none;
    &:hover {
      background: lightgreen;
    }
    &:focus {
      outline: none;
    }
  }
  .active {
    background: lightgreen;
  }
  // CSS Transitions
  .fade-enter-active, .fade-leave-active {
    transition: opacity .2s;
  }
  .fade-enter, .fade-leave-to {
    opacity: 0;
  }
</style>
```

**Link(s) to work**

1. Working on my TODO application in local environment.

Code is at [https://github.com/Johnny2136/my-todo-app](https://github.com/Johnny2136/my-todo-app).


![Saturday](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/Debugging5.png)

### Day 74: October 06, Saturday

**Today 's Progress**: STILL Debugging (the CLI is hard. I can understand just putting script tags for vue in a html page and then codeing from there, but the CLI is a whole other beast.) [Vue.js Todo App - Basics - Part 1](https://www.youtube.com/watch?v=A5S23KS_-bU)and [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html) ported into a local dev environment. Upgraded to VUE 3.0, still not working...

**Thoughts**: I am tiring to add my first todo list here[VueApp](https://jsfiddle.net/johnny2136/br7qzL1t/2/) to a local Git file and use Vue-CLI after going though more videos I am still struggleing to GROK this!!! Debugging continues.

### Resources used:
  * [Github repo for todoApp](https://github.com/Johnny2136/my-todo-app)
  * [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)
  * [Vue.js.org](https://vuejs.org/)
  * [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html)

It compiles and renders... Without the list so more refactoring and debugging tomorrow.

```html
template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
    </p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

```

**Link(s) to work**

1. Working on my TODO application in local environment.

Code is at [https://github.com/Johnny2136/my-todo-app](https://github.com/Johnny2136/my-todo-app).

![friday](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/Debugging4.png)
### Day 73: October 05, Friday

**Today 's Progress**: STILL Debugging (back to compiling with errors!!!!) [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)and [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html) ported into a local dev environment. Upgraded to VUE 3.0, still not working...

**Thoughts**: I am tiring to add features and update my first todo list here[VueApp](https://jsfiddle.net/johnny2136/br7qzL1t/2/) after going though the videos I came up with this[VueJS_ToDoList](https://jsfiddle.net/johnny2136/g72evm4L/) the next steps being getting this in my local dev environment Need further Debugging.

### Resources used:
  * [Github repo for todoApp](https://github.com/Johnny2136/my-todo-app)
  * [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)
  * [Vue.js.org](https://vuejs.org/)
  * [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html)

It compiles but still doesn't render... continued debugging tomorrow.

```html
<li v-for="todo in todos">
     <label>
       <input type="checkbox"
         v-on:change="toggle(todo)"
         v-bind:checked="todo.done">

       <del v-if="todo.done">
         {{ todo.text }}
       </del>
       <span v-else>
         {{ todo.text }}
       </span>
     </label>
   </li>
 </div>
```
The error I get in the browser is:
![error](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/Error4forDebugging4.png)

**Link(s) to work**

1. Working on my TODO application in local environment.

Code is at [https://github.com/Johnny2136/my-todo-app](https://github.com/Johnny2136/my-todo-app).



![thursday](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/Debugging3.png)

### Day 72: October 04, Thursday

**Today 's Progress**: STILL Debugging (But getting closer!!!! At least it compiles without errors!!!!) [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)and [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html) ported into a local dev environment. Upgraded to VUE 3.0, still not working...

**Thoughts**: I am tiring to add features and update my first todo list here[VueApp](https://jsfiddle.net/johnny2136/br7qzL1t/2/) after going though the videos I came up with this[VueJS_ToDoList](https://jsfiddle.net/johnny2136/g72evm4L/) the next steps being getting this in my local dev environment Need further Debugging.

### Resources used:
  * [Github repo for todoApp](https://github.com/Johnny2136/my-todo-app)
  * [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)
  * [Vue.js.org](https://vuejs.org/)
  * [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html)

It compiles but still doesn't render... continued debugging tomorrow.

```bash
johnn@DESKTOP-Johnny5 MINGW64 /d/johnny/GitHub/my-todo-app (feature)
$ npm run serve

> my-todo-app@0.1.0 serve D:\johnny\GitHub\my-todo-app
> vue-cli-service serve

 INFO  Starting development server...
 98% after emitting CopyPlugin

 DONE  Compiled successfully in 2725ms  9:10:56 PM  9:1 PM:10:56 PM
  App running at:
  - Local:   http://localhost:8081/
  - Network: http://192.168.56.1:8081/

  Note that the development build is not optimized.
  To create a production build, run npm run build.
```
The error I get in the browser is:
Uncaught ReferenceError: todoApp is not defined
    at eval (webpack-internal:///./node_modules/cache-loader/dist/cjs.js?!./node_modules/babel-loader/lib/index.js!./node_modules/cache-loader/dist/cjs.js?!./node_modules/vue-loader/lib/index.js?!./src/components/HelloWorld.vue?vue&type=script&lang=js&:82)
    at Module../node_modules/cache-loader/dist/cjs.js?!./node_modules/babel-loader/lib/index.js!./node_modules/cache-loader/dist/cjs.js?!./node_modules/vue-loader/lib/index.js?!./src/components/HelloWorld.vue?vue&type=script&lang=js& (app.js:829)
    at __webpack_require__ (app.js:725)
    at fn (app.js:102)
    at eval (webpack-internal:///./src/components/HelloWorld.vue?vue&type=script&lang=js&:2)
    at Module../src/components/HelloWorld.vue?vue&type=script&lang=js& (app.js:2046)
    at __webpack_require__ (app.js:725)
    at fn (app.js:102)
    at eval (webpack-internal:///./src/components/HelloWorld.vue:3)
    at Module../src/components/HelloWorld.vue (app.js:2034)
webpack-internal:///./node_modules/vue/dist/vue.runtime.esm.js:8009 You are running Vue in development mode.
Make sure to turn on production mode when deploying for production.
See more tips at https://vuejs.org/guide/deployment.html

**Link(s) to work**

1. Working on my TODO application in local environment.

Code is at [https://github.com/Johnny2136/my-todo-app](https://github.com/Johnny2136/my-todo-app).



![Wednesday](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/ToDoDebug%20day%202.png)

### Day 71: October 03, Wednesday

**Today 's Progress**: STILL Debugging [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)and [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html) ported into a local dev environment. Upgraded to VUE 3.0, still not working...

**Thoughts**: I am tiring to add features and update my first todo list here[VueApp](https://jsfiddle.net/johnny2136/br7qzL1t/2/) after going though the videos I came up with this[VueJS_ToDoList](https://jsfiddle.net/johnny2136/g72evm4L/) the next steps being getting this in my local dev environment Need further Debugging.

### Resources used:
  * [Github repo for todoApp](https://github.com/Johnny2136/my-todo-app)
  * [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)
  * [Vue.js.org](https://vuejs.org/)
  * [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html)

It compiles but still doesn't render... continued debugging tomorrow.

```javascript
<script>
/* eslint-disable */
export default {
  name: 'HelloWorld'
  props: {
    message: 'Welcome to Todo App',
    addTodoInput: '',
    lists: [],
    hasError: false
  },
  methods:{
    addTask(){

      if(!this.addTodoInput){
        this.hasError = true;
        return;
      }

      this.hasError = false;

      this.lists.push({
        id:this.lists.length+1,
        title: this.addTodoInput,
        isComplete: false
      });

      this.addTodoInput = '';
    },

    updateTask(e, list){
      e.preventDefault();
      list.title = e.target.innerText;
      e.target.blur();
    },

    completeTask(list){
      list.isComplete = !list.isComplete;
    }

  }
});

//generate dummy data for demo purpose
todoApp.lists = [{
      id: 1,
      title: 'Hello Vue.JS',
      isComplete: false
    },
    {
      id: 2,
      title: 'Learn JavaScript',
      isComplete: false
    },
    {
      id: 3,
      title: 'Learn Vue',
      isComplete: false
    },
    {
      id: 4,
      title: 'Play around in JSFiddle',
      isComplete: true
    }]
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

```


**Link(s) to work**

1. Working on my TODO application in local environment.

Code is at [https://github.com/Johnny2136/my-todo-app](https://github.com/Johnny2136/my-todo-app).



![Tuesday](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/ToDoDebug.png)

### Day 70: October 02, Tuesday

**Today 's Progress**: Debugging [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)and [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html) ported into a local dev environment.

**Thoughts**: I am tiring to add features and update my first todo list here[VueApp](https://jsfiddle.net/johnny2136/br7qzL1t/2/) after going though the videos I came up with this[VueJS_ToDoList](https://jsfiddle.net/johnny2136/g72evm4L/) the next steps being getting this in my local dev environment Need further Debugging.

### Resources used:
  * [Github repo for todoApp](https://github.com/Johnny2136/my-todo-app)
  * [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)
  * [Vue.js.org](https://vuejs.org/)
  * [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html)
  
It compiles but still doesn't render... continued debugging tomorrow.

```javascript
<template>
  <div id="todoApp">
  <h2> {{message}} </h2>
  <p>
  New Tasks can be added below:
  </p>
  <form name="todo-form" method="post" action="" v-on:submit.prevent="addTask">
    <input name="add-todo" type="text" v-model="addTodoInput" v-bind:class="{error: hasError}"/>
    <button type="submit">Add</button>
  </form>
   <div class="todo-lists" v-if="lists.length"><br />
    <h3>My Todo Tasks:</h3>
    <ul>
      <li v-for="list in lists" :key="list.id">
        <input type="checkbox" v-on:change="completeTask(list)" v-bind:checked="list.isComplete"/>
        <del v-if="list.isComplete">
        {{list.title}}
        </del>
         <span v-else class="title" contenteditable="true" v-on:keydown.enter="updateTask($event, list)" v-on:blur="updateTask($event, list)" v-bind:class="{completed: list.isComplete}">{{list.title}}</span>
      </li>
    </ul>
  </div>
  </div>
</template>

<script>
/* eslint-disable */
var todoApp = new Vue({
  el: '#todoApp',
  data: {
    message: 'Welcome to Todo App',
    addTodoInput: '',
    lists: [],
    hasError: false
  },
  methods:{
    addTask(){

      if(!this.addTodoInput){
        this.hasError = true;
        return;
      }

      this.hasError = false;

      this.lists.push({
        id:this.lists.length+1,
        title: this.addTodoInput,
        isComplete: false
      });

      this.addTodoInput = '';
    },

    updateTask(e, list){
      e.preventDefault();
      list.title = e.target.innerText;
      e.target.blur();
    },

    completeTask(list){
      list.isComplete = !list.isComplete;
    }

  }
});

//generate dummy data for demo purpose
todoApp.lists = [{
      id: 1,
      title: 'Hello Vue.JS',
      isComplete: false
    },
    {
      id: 2,
      title: 'Learn JavaScript',
      isComplete: false
    },
    {
      id: 3,
      title: 'Learn Vue',
      isComplete: false
    },
    {
      id: 4,
      title: 'Play around in JSFiddle',
      isComplete: true
    }]
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
body {
  background: #000;
  ;
  padding: 20px;
  font-family: Helvetica;
}

#todoApp {
  background: #fff;
  border-radius: 4px;
  padding: 20px;
  transition: all 0.2s;
}

li {
  margin: 8px 0;
}

h2 {
  font-weight: bold;
  margin-bottom: 15px;
}

del {
  color: rgba(0, 0, 0, 0.3);
}
</style>
```


**Link(s) to work**

1. Working on my TODO application in local environment.

Code is at [https://github.com/Johnny2136/my-todo-app](https://github.com/Johnny2136/my-todo-app).



![Monday](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/LocalToDo.png)

## Day 69: October 01, Monday

**Today 's Progress**: I am working through getting [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)and [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html) ported into a local dev environment.

**Thoughts**: Following these I am tiring to add features and update my first todo list here[VueApp](https://jsfiddle.net/johnny2136/br7qzL1t/2/) after going though the videos I came up with this[VueJS_ToDoList](https://jsfiddle.net/johnny2136/g72evm4L/) the next steps being getting this in my local dev environment.

### Resources used:
  * [Github repo for todoApp](https://github.com/Johnny2136/my-todo-app)
  * [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)
  * [Vue.js.org](https://vuejs.org/)
  * [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html)
Errors in... debugging tomorrow.
```javascript
// The Vue build version to load with the `import` command
// (runtime-only or standalone) has been set in webpack.base.conf with an alias.
import Vue from 'vue'
import App from './App'
import router from './router'

Vue.config.productionTip = false

/* eslint-disable no-new */
  var app = new Vue({
    el: '#todoApp',
    data: {
      message: 'Welcome to Todo App',
      addTodoInput: '',
      lists: [],
      hasError: false
    },
    methods:{
      addTask(){

        if(!this.addTodoInput){
          this.hasError = true;
          return;
        }

        this.hasError = false;

        this.lists.push({
          id:this.lists.length+1,
          title: this.addTodoInput,
          isComplete: false
        });

        this.addTodoInput = '';
      },

      updateTask(e, list){
        e.preventDefault();
        list.title = e.target.innerText;
        e.target.blur();
      },

      completeTask(list){
        list.isComplete = !list.isComplete;
      }

    }
  });

  //generate dummy data for demo purpose
  todoApp.lists = [{
        id: 1,
        title: "Hello Vue.JS",
        isComplete: false
      },
      {
        id: 2,
        title: "Learn JavaScript",
        isComplete: false
      },
      {
        id: 3,
        title: "Learn Vue",
        isComplete: false
      },
      {
        id: 4,
        title: "Play around in JSFiddle",
        isComplete: true
      }];
```


**Link(s) to work**

1. Working on my TODO application in local environment.

Code is at [https://github.com/Johnny2136/my-todo-app](https://github.com/Johnny2136/my-todo-app).



![sunday](http://blog.whooosreading.org/wp-content/uploads/2017/10/meditation.jpg)

### Day 68: September 30, Sunday

**Today 's Progress**: Gave up on Docker I have to have windows 10 pro and I do not have pro. So fell back 10 yards and punted. So on with learning by tutorials I am working through [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)and [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html).

**Thoughts**: Following these I am tring to add fetures and update my first todo list here[VueApp](https://jsfiddle.net/johnny2136/br7qzL1t/2/) after going though the videos I came up with this[VueJS_ToDoList](https://jsfiddle.net/johnny2136/g72evm4L/)

### Resources used:
  * [VueJS_ToDoList](https://jsfiddle.net/johnny2136/g72evm4L/)
  * [INTERMEDIATE: Learn Vue 2: Step By Step](https://laracasts.com/series/learn-vue-2-step-by-step)
  * [Vue.js.org](https://vuejs.org/)
  * [VUE.JS - SIMPLE TODO APP - PART 1](http://iamkumaran.github.io/vue-js/vue-js-todo-app-part-1.html)

```html
<div id="todoApp">
  <h2> {{message}} </h2>
  <p>
  New Tasks can be added below:
  </p>
  <form name="todo-form" method="post" action="" v-on:submit.prevent="addTask">
    <input name="add-todo" type="text" v-model="addTodoInput" v-bind:class="{error: hasError}"/>

    <button type="submit">Add</button>
  </form>

  <div class="todo-lists" v-if="lists.length"><br />
    <h3>My Todo Tasks:</h3>
    <ul>
      <li v-for="list in lists" :key="list.id">
        <input type="checkbox" v-on:change="completeTask(list)" v-bind:checked="list.isComplete"/>
        <del v-if="list.isComplete">
        {{list.title}}
        </del>
         <span v-else class="title" contenteditable="true" v-on:keydown.enter="updateTask($event, list)" v-on:blur="updateTask($event, list)" v-bind:class="{completed: list.isComplete}">{{list.title}}</span>
      </li>
    </ul>
  </div>
  <script>
  var todoApp = new Vue({
  el: '#todoApp',
  data: {
    message: 'Welcome to Todo App',
    addTodoInput: '',
    lists: [],
    hasError: false
  },
  methods:{
    addTask(){

      if(!this.addTodoInput){
        this.hasError = true;
        return;
      }

      this.hasError = false;

      this.lists.push({
        id:this.lists.length+1,
        title: this.addTodoInput,
        isComplete: false
      });

      this.addTodoInput = '';
    },

    updateTask(e, list){
      e.preventDefault();
      list.title = e.target.innerText;
      e.target.blur();
    },

    completeTask(list){
      list.isComplete = !list.isComplete;
    }

  }
});
//generate dummy data for demo purpose
todoApp.lists = [{
      id: 1,
      title: "Hello Vue.JS",
      isComplete: false
    },
    {
      id: 2,
      title: "Learn JavaScript",
      isComplete: false
    },
    {
      id: 3,
      title: "Learn Vue",
      isComplete: false
    },
    {
      id: 4,
      title: "Play around in JSFiddle",
      isComplete: true
    }];
  </script>
```


**Link(s) to work**

1. Working on my TODO application jsfiddle.

Code is at [https://jsfiddle.net/johnny2136/g72evm4L/](https://jsfiddle.net/johnny2136/g72evm4L/).


![VSCode](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/VSCode.png)

## Day 67: September 29, Saturday

**Today 's Progress**: Coded my local dev environment on my PC added Docker and tried to compiled a sample application.

**Thoughts**: Following this [Dockerize Vue.js App](https://vuejs.org/v2/cookbook/dockerize-vuejs-app.html)

### Resources used:
  * [Dockerize Vue.js App](https://vuejs.org/v2/cookbook/dockerize-vuejs-app.html)
  * [VueJS Tutorial](https://www.tutorialspoint.com/vuejs/index.htm)
  * [https://code.visualstudio.com/](https://code.visualstudio.com/)
  * [Webpack for vuejs](https://github.com/vuejs-templates/webpack)

```dockerfile
FROM node:9.11.1-alpine

# install simple http server for serving static content
RUN npm install -g http-server

# make the 'app' folder the current working directory
WORKDIR /app

# copy both 'package.json' and 'package-lock.json' (if available)
COPY package*.json ./

# install project dependencies
RUN npm install

# copy project files and folders to the current working directory (i.e. 'app' folder)
COPY . .

# build app for production with minification
RUN npm run build

EXPOSE 8080
CMD [ "http-server", "dist" ]
```


**Link(s) to work**

1. Started work on dockerizing my application local development Environment.

**Introduction to Vue.js**
Worked through setting up my local dev Environment

Code is at [https://github.com/Johnny2136/myproject](https://github.com/Johnny2136/myproject).



![First Vue Local](https://github.com/Johnny2136/johnny2136.github.io/blob/master/images/myvueproject.png)

### Day 66: September 28, Friday

**Today 's Progress**: Set up local dev environment on my PC added VSCode and compiled a sample application.

**Thoughts**: Following this [VueJS - Environment Setup](https://www.tutorialspoint.com/vuejs/vuejs_environment_setup.htm)

### Resources used:
  * [JSFiddle](https://jsfiddle.net/johnny2136/br7qzL1t/)
  * [VueJS Tutorial](https://www.tutorialspoint.com/vuejs/index.htm)
  * [https://code.visualstudio.com/](https://code.visualstudio.com/)
  * [Webpack for vuejs](https://github.com/vuejs-templates/webpack)

```HTML
<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to my first Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
```


**Link(s) to work**

1. Started work on my local development Environment.

**Introduction to Vue.js**
Worked through setting up my local dev Environment

Code is at [https://github.com/Johnny2136/myproject](https://github.com/Johnny2136/myproject).


### Day 65: September 27, Thursday

**Today 's Progress**: Did the next lesson on [Learn Vue.js for free](https://scrimba.com/g/glearnvue).

**Thoughts**: Working on local development of Vue.js so set up the lesson tutorial in Gitlab to clone locally worked through the methods video tutorial for learning Vue. [ScribaConsol](https://scrimba.com/p/pZ45Hz/c6bL6Uy)

### Resources used:
  * [JSFiddle](https://jsfiddle.net/johnny2136/br7qzL1t/)
  * [Vue in CodeSandbox](https://codesandbox.io/s/vue)
  * [Repl.it Vue project](https://repl.it/@JohnJohnson2/NarrowProductiveMonads)
  * [Learn Vue.js for free](https://scrimba.com/g/glearnvue)

```HTML
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<meta name="viewport" content="width=device-width, initial-scale=1">
		<link rel="stylesheet" href="https://cdn.rawgit.com/jgthms/minireset.css/master/minireset.css">
		<link rel="stylesheet" href="css/debug.css">
		<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Roboto:400,500,700,900">
		<script src="https://cdn.jsdelivr.net/npm/vue@2.5.16/dist/vue.js"></script>
		<style>

:root {
	font: 1rem/1.175 "BlinkMacSystemFont", -apple-system, "Roboto", sans-serif;
}

#app {
	display: flex;
	justify-content: center; align-items: center;
	width: 100vw; height: 100vh;
	font-weight: 900; font-size: 8rem;
	color: hsl(0, 0%, 100%);
	background: hsl(240, 100%, 67%);
	user-select: none;
}

img {
	width: 8rem; height: 8rem;
	vertical-align: calc(-0.12109375em);
}

		</style>
	</head>
	<body>

		<div id="app">
			<p>{{  }}</p>
		</div>

		<script>

"use strict"

// emojify returns the corresponding emoji image
function emojify(name) {
	var out = `<img src="emojis/` + name + `.png">`
	return out
}

// cast returns a spell (function) that decorates the wizard
function cast(emoji) {
    if (!emoji) {
        emoji = "¯\\_(ツ)_/¯"
    }
	return function (wizard) {
		return emoji + wizard + emoji
	}
}

var app = new Vue({
	el: "#app",
	data: {
		wizard: emojify("wizard")
	},
    methods: {
        lumos: cast(emojify("lumos")),
        incendio: cast(emojify("incendio"))
    }
})

		</script>

	</body>
</html>
```


**Link(s) to work**

1. Started work on [Introduction to Vue.js](https://scrimba.com/c/c6bL6Uy).

**Introduction to Vue.js**
Worked through first three videos https://scrimba.com/p/pZ45Hz/cyLQNAM

All code is Scriba [https://scrimba.com/@Johnny2136](https://scrimba.com/@Johnny2136).

![humpday](https://image.spreadshirtmedia.com/image-server/v1/compositions/108410594/views/1,width=650,height=650,appearanceId=6,version=1486019171/.jpg)

### Day 64: September 26, Wednesday

**Today 's Progress**: Putting lessons on D3 on hold while I study Vue.JS and SpringBoot which is the chosen framework for my work environment  lessons on [Learn Vue.js for free](https://scrimba.com/g/glearnvue).

**Thoughts**: Paused the D3.js lessons and Challenges, At `#freeCodeCamp` To start Vue.js working through video tutorials for learning Vue. [ScribaConsol](https://scrimba.com/p/pZ45Hz/c6bL6Uy)

### Resources used:
  * [JSFiddle](https://jsfiddle.net/johnny2136/br7qzL1t/)
  * [Vue in CodeSandbox](https://codesandbox.io/s/vue)
  * [Learn Vue.js for free](https://scrimba.com/g/glearnvue)

  ![vue.js_sandbox](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/Vue.js.png)

**Link(s) to work**

1. Started work on [Introduction to Vue.js](https://scrimba.com/c/c6bL6Uy).

**Introduction to Vue.js**
Worked through first three videos https://scrimba.com/p/pZ45Hz/cyLQNAM

All code is Scriba [https://scrimba.com/@Johnny2136](https://scrimba.com/@Johnny2136).



### Day 63: September 25, Tuesday

**Today 's Progress**: Continued lessons on [Introduction to the Data Visualization with D3 Challenges](https://learn.freecodecamp.org/data-visualization/data-visualization-with-d3).

**Thoughts**: Continued the D3.js lessons and Challenges, aside from content missing from `#freeCodeCamp` The examples disappeared. So two days of hellish commutes lasing 4 hours on Monday and 3.5 hours round trip today. I'm tired.

### Resources used:
  * [JSFiddle](https://jsfiddle.net/johnny2136/1pLubnqc/)
  * [REPL.IT](https://repl.it/@JohnJohnson2/FCCD3)
  * [GitHub_FCC_Repo](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/DataVisualizationWithD3.md)
  * [D3: setting style conditionally with immediately invoked arrow function and ternary](https://stackoverflow.com/questions/45593251/d3-setting-style-conditionally-with-immediately-invoked-arrow-function-and-tern/45654334)
  * [D3 Tutorial](https://www.dashingd3js.com/table-of-contents)
  * [D3 in Depth](https://d3indepth.com/)

  **Display Shapes with SVG**
  **Example:**
  none, a freaking example would have been awesome!
  ```html
  <svg width="400" height="180">
   <rect x="50" y="20" width="150" height="150" style="fill:blue;stroke:pink;stroke-width:5;fill-opacity:0.1;stroke-opacity:0.9" />
  </svg>
  ```

  **Challange Instructions:**
  Add a rect shape to the svg using append(), and give it a width attribute of 25 and height attribute of 100. Also, give the rect x and y attributes each set to 0.

  *Resources:*

  **My solution**
  ```html
  <body>
    <script>
      const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];

      const w = 500;
      const h = 100;

      const svg = d3.select("body")
                    .append("svg")
                    .attr("width", w)
                    .attr("height", h)
                    // Add your code below this line
                    .append("rect")
                    .attr("x", 0)
                    .attr("y", 0)
                    .attr("width", 25)
                    .attr("height", 100);           
                    // Add your code above this line
    </script>
  </body>
  ```
**Link(s) to work**

1. Started work on [Introduction to the Data Visualization with D3 Challenges](https://learn.freecodecamp.org/data-visualization/data-visualization-with-d3).

**Introduction to the Data Visualization with D3 Challenges**

 - [x] Learn About SVG in D3
 - [x] Display Shapes with SVG

All code is in GitHub [FCC_Challenges/DataVisualizationWithD3.md](https://github.com/Johnny2136/FCC-Projects/edit/master/FCC_Challenges/DataVisualizationWithD3.md).


![Monday](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/D3_Day62.png)

## Day 62: September 24, Monday

**Today 's Progress**: Continued lessons on [Introduction to the Data Visualization with D3 Challenges](https://learn.freecodecamp.org/data-visualization/data-visualization-with-d3).

**Thoughts**: Continued the D3.js lessons and Challenges, confirmed there is some content missing from `#freeCodeCamp` The examples that are there are pretty good some are not needed.

### Resources used:
  * [JSFiddle](https://jsfiddle.net/johnny2136/1pLubnqc/)
  * [REPL.IT](https://repl.it/@JohnJohnson2/FCCD3)
  * [GitHub_FCC_Repo](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/DataVisualizationWithD3.md)
  * [D3: setting style conditionally with immediately invoked arrow function and ternary](https://stackoverflow.com/questions/45593251/d3-setting-style-conditionally-with-immediately-invoked-arrow-function-and-tern/45654334)
  * [D3 Tutorial](https://www.dashingd3js.com/table-of-contents)
  * [D3 in Depth](https://d3indepth.com/)

**Change the Presentation of a Bar Chart** (Last challenge I did)
**Example:** none

**Challenge Instructions:** First, add a margin of `2px` to the bar class in the style tag. Next, change the callback function in the `style()` method so it returns a value 10 times the original data value (plus the "px").

*Note: Multiplying each data point by the same constant only alters the scale. It's like zooming in, and it doesn't change the meaning of the underlying data.*

**My solution**
```html
<style>
  .bar {
    width: 25px;
    height: 100px;
    /* Add your code below this line */
    margin: 2px;
    /* Add your code above this line */
    display: inline-block;
    background-color: blue;
  }
</style>
<body>
  <script>
    const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];    
    d3.select("body").selectAll("div")
      .data(dataset)
      .enter()
      .append("div")
      .attr("class", "bar")
      // Add your code below this line
      .style("height", (d) => (d * 10 + "px"));      
      // Add your code above this line
  </script>
</body>
```
**Link(s) to work**

1. Started work on [Introduction to the Data Visualization with D3 Challenges](https://learn.freecodecamp.org/data-visualization/data-visualization-with-d3).

**Introduction to the Data Visualization with D3 Challenges**

 - [x] Change Styles Based on Data
 - [x] Add Classes with D3
 - [x] Update the Height of an Element Dynamically
 - [x] Change the Presentation of a Bar Chart
 
All code is in GitHub [FCC_Challenges/DataVisualizationWithD3.md](https://github.com/Johnny2136/FCC-Projects/edit/master/FCC_Challenges/DataVisualizationWithD3.md).


![Sunday](https://discourse-user-assets.s3.amazonaws.com/original/3X/1/3/13f966666ac2e06ae8cd3f7cfda01641494e0946.png)

### Day 61: September 23, Sunday

**Today 's Progress**: Started lessons on [Introduction to the Data Visualization with D3 Challenges](https://learn.freecodecamp.org/data-visualization/data-visualization-with-d3).

**Thoughts**: Started the D3.js lessons and Challenges, I feel there is some content missing from `#freeCodeCamp` On a positive note so far most of examples are pretty good.

#### Resources used:
  * [JSFiddle](https://jsfiddle.net/johnny2136/1pLubnqc/)
  * [REPL.IT](https://repl.it/@JohnJohnson2/FCCD3)
  * [GitHub_FCC_Repo](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/DataVisualizationWithD3.md)
  * [Binding Data to DOM Elements](https://www.dashingd3js.com/binding-data-to-dom-elements)
  * [D3 Tutorial](https://www.dashingd3js.com/table-of-contents)
  * [D3 in Depth](https://d3indepth.com/)

  #### Add Document Elements with D3

  **The Lesson:**
  D3 has several methods that let you add and change elements in your document.

  The `select()` method selects one element from the document. It takes an argument for the name of the element you want and returns an HTML node for the first element in the document that matches the name. Here's an example:

  `const anchor = d3.select("a");`

  The above example finds the first anchor tag on the page and saves an HTML node for it in the variable anchor. You can use the selection with other methods. The "d3" part of the example is a reference to the D3 object, which is how you access D3 methods.

  Two other useful methods are `append()` and `text()`.

  The `append()` method takes an argument for the element you want to add to the document. It appends an HTML node to a selected item, and returns a handle to that node.

  The `text()` method either sets the text of the selected node, or gets the current text. To set the value, you pass a string as an argument inside the parentheses of the method.

  **Example:**
  Here's an example that selects an unordered list, appends a list item, and adds text:
  ```JavaScript
  d3.select("ul")
    .append("li")
    .text("Very important item");
  ```
  D3 allows you to chain several methods together with periods to perform a number of actions in a row.

  **Challange Instructions:**
  Use the select method to select the `body` tag in the document. Then append an `h1` tag to it, and add the text "Learning D3" into the `h1` element.

  **MySolution**
  ```JavaScript
  <body>
    <script>
      // Add your code below this line
      d3.select("body")
        .append("h1")
        .text("Learning D3");    
      // Add your code above this line
    </script>
  </body>
  ```


  #### Select a Group of Elements with D3

  **The Lesson:**
  D3 also has the `selectAll()` method to select a group of elements. It returns an array of HTML nodes for all the items in the document that match the input string. Here's an example to select all the anchor tags in a document:

  **Example:**
  `const anchors = d3.selectAll("a");`

  Like the `select()` method, `selectAll()` supports method chaining, and you can use it with other methods.

  **Challange Instructions:**
  Select all of the `li` tags in the document, and change their text to "list item" by chaining the `.text()` method.

  *notes:* I would have made the following example:

  ```JavaScript
  <body>
    <a href="">Example</a>
    <a href="">Example</a>
    <a href="">Example</a>
    <script>
       const anchors = d3.selectAll("a")
        .test("SomeURL");     
    </script>
  </body>
  ```
  *Resources:* https://d3indepth.com/selections/

  **My solution**
  ```JavaScript
  <body>
    <ul>
      <li>Example</li>
      <li>Example</li>
      <li>Example</li>
    </ul>
    <script>
      // Add your code below this line
      const anchors = d3.selectAll("li")
        .text("list item");     
      // Add your code above this line
    </script>
  </body>
  ```


  #### Work with Data in D3

  **The Lesson:**
  The D3 library focuses on a data-driven approach. When you have a set of data, you can apply D3 methods to display it on the page. Data comes in many formats, but this challenge uses a simple array of numbers.

  The first step is to make D3 aware of the data. The `data()` method is used on a selection of DOM elements to attach the data to those elements. The data set is passed as an argument to the method.

  A common workflow pattern is to create a new element in the document for each piece of data in the set. D3 has the `enter()` method for this purpose.

  When `enter()` is combined with the `data()` method, it looks at the selected elements from the page and compares them to the number of data items in the set. If there are fewer elements than data items, it creates the missing elements.

  **Example:**
  Here is an example that selects a ul element and creates a new list item based on the number of entries in the array:
  ```html
  <body>
    <ul></ul>
    <script>
      const dataset = ["a", "b", "c"];
      d3.select("ul").selectAll("li")
        .data(dataset)
        .enter()
        .append("li")
        .text("New item");
    </script>
  </body>
  ```
  It may seem confusing to select elements that don't exist yet. This code is telling D3 to first `select` the `ul` on the page. Next, `select all` list items, which returns an empty selection. Then the `data()` method reviews the dataset and runs the following code three times, once for each item in the array. The `enter()` method sees there are no `li` elements on the page, but it needs 3 (one for each piece of data in dataset). New `li` elements are appended to the `ul` and have the text "New item".

  **Challange Instructions:**
  Select the `body` node, then select all `h2` elements. Have D3 create and `append` an `h2` tag for each item in the dataset array. The text in the `h2` should say "New Title". Your code should use the `data()` and `enter()` methods.

  *Resources:* https://www.dashingd3js.com/binding-data-to-dom-elements

  **My solution**
  ```JavaScript
  <body>
    <script>
      const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];

      // Add your code below this line
      d3.select("body").selectAll("h2")
        .data(dataset)
        .enter()
        .append("h2")
        .text("New Title #3");   
      // Add your code above this line
    </script>
  </body>
  ```


  #### Work with Dynamic Data in D3

  **The Lesson:**
  The last two challenges cover the basics of displaying data dynamically with D3 using the `data()` and `enter()` methods. These methods take a data set and, together with the `append()` method, create a new DOM element for each entry in the data set.

  In the previous challenge, you created a new `h2` element for each item in the dataset array, but they all contained the same text, "New Title". This is because you have not made use of the data that is bound to each of the `h2` elements.
  **Example:**
  The D3 `text()` method can take a string or a callback function as an argument:

  `selection.text((d) => d)` adding `d + 'text');` Would have been helpfull???

  In the example above, the parameter d refers to a single entry in the dataset that a selection is bound to.

  Using the current example as context, the first `h2` element is bound to 12, the second `h2` element is bound to 31, the third `h2` element is bound to 22, and so on.

  **Challange Instructions:**
  Change the `text()` method so that each `h2` element displays the corresponding value from the dataset array with a single space and "USD". For example, the first heading should be "12 USD".

  *Resources:* https://forum.freecodecamp.org/t/work-with-dynamic-data-in-d3-help/222552/4

  **My solution**
  ```JavaScript
  <body>
    <script>    
      const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];        
        d3.select("body").selectAll("h2")
        .data(dataset)
        .enter()
        .append("h2")
        // Add your code below this line      
        .text((d) => d + ' USD');      
        // Add your code above this line    
    </script>
  </body>
  ```


  #### Add Inline Styling to Elements

  **The Lesson:**
  D3 lets you add inline CSS styles on dynamic elements with the style() method.

  The style() method takes a comma-separated key-value pair as an argument.

  **Example:**
  Here's an example to set the selection's text color to blue:

  `selection.style("color","blue");`

  **Challange Instructions:**
  Add the style() method to the code in the editor to make all the displayed text have a font-family of verdana.

  *Resources:* Easy one...

  **My solution**
  ```JavaScript
  <body>
    <script>
      const dataset = [12, 31, 22, 17, 25, 18, 29, 14, 9];    
      d3.select("body").selectAll("h2")
        .data(dataset)
        .enter()
        .append("h2")
        .text((d) => (d + " USD"))
        // Add your code below this line
        .style("font-family","verdana");      
        // Add your code above this line
    </script>
  </body>
  ```

**Link(s) to work**

1. Started work on [Introduction to the Data Visualization with D3 Challenges](https://learn.freecodecamp.org/data-visualization/data-visualization-with-d3).

**Introduction to the Data Visualization with D3 Challenges**

 - [x] Add Document Elements with D3
 - [x] Select a Group of Elements with D3
 - [x] Work with Data in D3
 - [x] Work with Dynamic Data in D3
 - [x] Add Inline Styling to Elements

All code is in GitHub [FCC_Challenges/DataVisualizationWithD3.md](https://github.com/Johnny2136/FCC-Projects/edit/master/FCC_Challenges/DataVisualizationWithD3.md).



![Saturday](https://i.imgur.com/dnekHhQ.jpg)

### Day 60: September 22, Saturday

**Today 's Progress**: Finally finished the [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects).

**Thoughts**: Finished the fifth project toward the Front End Certification at free code camp. This one was absolute Hell!!! I really struggled to make the user stories pass. It needs a better UI but I was scared to refactor once the tests passed. Everytime I tried to make something better 5 more user tests broke! Going to bed now :(

### Resources used:
  * [Color tag editor](https://www.google.com/search?q=%234d4d4d&oq=%234d4d4d&aqs=chrome..69i57j69i61&sourceid=chrome&ie=UTF-8)
  * [Web Safe Fonts](https://www.w3schools.com/cssref/css_websafe_fonts.asp)
  * [Create-React-App](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md)
  * [Shadow boxing](https://www.w3schools.com/cssref/css3_pr_box-shadow.asp)
  * [setInterval timing slowly drifts away from staying accurate](http://stackoverflow.com/questions/8173580/setinterval-timing-slowly-drifts-away-from-staying-accurate)
  * [Project example](https://codepen.io/freeCodeCamp/full/XpKrrW)


  **Front End Libraries Projects - Build a Pomodoro Clock**

**Objective:** Build a CodePen.io app that is functionally similar to this: https://codepen.io/freeCodeCamp/full/XpKrrW.

Fulfill the below user stories and get all of the tests to pass. Give it your own personal style.

You can use any mix of HTML, JavaScript, CSS, Bootstrap, SASS, React, Redux, and jQuery to complete this project. You should use a frontend framework (like React for example) because this section is about learning frontend frameworks. Additional technologies not listed above are not recommended and using them is at your own risk. We are looking at supporting other frontend frameworks like Angular and Vue, but they are not currently supported. We will accept and try to fix all issue reports that use the suggested technology stack for this project. Happy coding!

- [X] User Story #1: I can see an element with id="break-label" that contains a string (e.g. "Break Length").
- [X] User Story #2: I can see an element with id="session-label" that contains a string (e.g. "Session Length").
- [X] User Story #3: I can see two clickable elements with corresponding IDs: id="break-decrement" and id="session-decrement".
- [X] User Story #4: I can see two clickable elements with corresponding IDs: id="break-increment" and id="session-increment".
- [X] User Story #5: I can see an element with a corresponding id="break-length", which by default (on load) displays a value of 5.
- [X] User Story #6: I can see an element with a corresponding id="session-length", which by default displays a value of 25.
- [X] User Story #7: I can see an element with a corresponding id="timer-label", that contains a string indicating a session is initialized (e.g. "Session").
- [X] User Story #8: I can see an element with corresponding id="time-left". NOTE: Paused or running, the value in this field should always be displayed in mm:ss format (i.e. 25:00).
- [X] User Story #9: I can see a clickable element with a corresponding id="start_stop".
- [X] User Story #10: I can see a clickable element with a corresponding id="reset".
- [X] User Story #11: When I click the element with the id of reset, any running timer should be stopped, the value within id="break-length" should return to 5, the value within id="session-length" should return to 25, and the element with id="time-left" should reset to it's default state.
- [X] User Story #12: When I click the element with the id of break-decrement, the value within id="break-length" decrements by a value of 1, and I can see the updated value.
- [X] User Story #13: When I click the element with the id of break-increment, the value within id="break-length" increments by a value of 1, and I can see the updated value.
- [X] User Story #14: When I click the element with the id of session-decrement, the value within id="session-length" decrements by a value of 1, and I can see the updated value.
- [X] User Story #15: When I click the element with the id of session-increment, the value within id="session-length" increments by a value of 1, and I can see the updated value.
- [X] User Story #16: I should not be able to set a session or break length to <= 0.
- [X] User Story #17: I should not be able to set a session or break length to > 60.
- [X] User Story #18: When I first click the element with id="start_stop", the timer should begin running from the value currently displayed in id="session-length", even if the value has been incremented or decremented from the original value of 25.
- [X] User Story #19: If the timer is running, the element with the id of time-left should display the remaining time in mm:ss format (decrementing by a value of 1 and updating the display every 1000ms).
- [X] User Story #20: If the timer is running and I click the element with id="start_stop", the countdown should pause.
User Story #21: If the timer is paused and I click the element with id="start_stop", the countdown should resume running from the point at which it was paused.
- [X] User Story #22: When a session countdown reaches zero (NOTE: timer MUST reach 00:00), and a new countdown begins, the element with the id of timer-label should display a string indicating a break has begun.
- [X] User Story #23: When a session countdown reaches zero (NOTE: timer MUST reach 00:00), a new break countdown should begin, counting down from the value currently displayed in the id="break-length" element.
- [X] User Story #24: When a break countdown reaches zero (NOTE: timer MUST reach 00:00), and a new countdown begins, the element with the id of timer-label should display a string indicating a session has begun.
- [X] User Story #25: When a break countdown reaches zero (NOTE: timer MUST reach 00:00), a new session countdown should begin, counting down from the value currently displayed in the id="session-length" element.
- [X] User Story #26: When a countdown reaches zero (NOTE: timer MUST reach 00:00), a sound indicating that time is up should play. This should utilize an HTML5 audio tag and have a corresponding id="beep".
- [X] User Story #27: The audio element with id="beep" must be 1 second or longer.
- [X] User Story #28: The audio element with id of beep must stop playing and be rewound to the beginning when the element with the id of reset is clicked.

You can build your project by forking this CodePen pen. Or you can use this CDN link to run the tests in any environment you like: https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js

Once you're done, submit the URL to your working project with all its tests passing.
Remember to use the Read-Search-Ask method if you get stuck.

**Solution:** https://codepen.io/johnny2136/pen/rZZMNq

![PomodoroClock](https://raw.githubusercontent.com/Johnny2136/FCC-Projects/master/images/PomodoroClock.png)

**Link(s) to work**

1. Finished work on [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects). (Trying to use React on Redux)

**Introduction to the Front End Libraries Projects**

 -[x] Build a Random Quote Machine
 -[x] Build a Markdown Previewer
 -[x] Build a Drum Machine
 -[x] Build a JavaScript Calculator
 -[X] Build a Pomodoro Clock

All code is in GitHub [Introduction to the Front End Libraries Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_Front_End_Libraries_Projects).

### Day 59: September 21, Friday

**Today 's Progress**: Continued working on the [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects).

**Thoughts**: Still working on the fifth project toward the Front End Certification at free code camp. This one is Really tough!!! I am struggling to make the user stories pass. I need to refactor and try and do so without breaking the passing tests. I fixed 5 broke user test now number 12 is failing to fix another ARRRRRRGGGGHHHHH!!!!! Going to bed now :(

### Resources used:
  * [Color tag editor](https://www.google.com/search?q=%234d4d4d&oq=%234d4d4d&aqs=chrome..69i57j69i61&sourceid=chrome&ie=UTF-8)
  * [Web Safe Fonts](https://www.w3schools.com/cssref/css_websafe_fonts.asp)
  * [Create-React-App](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md)


  **Front End Libraries Projects - Build a Pomodoro Clock**

**Objective:** Build a CodePen.io app that is functionally similar to this: https://codepen.io/freeCodeCamp/full/XpKrrW.

Fulfill the below user stories and get all of the tests to pass. Give it your own personal style.

You can use any mix of HTML, JavaScript, CSS, Bootstrap, SASS, React, Redux, and jQuery to complete this project. You should use a frontend framework (like React for example) because this section is about learning frontend frameworks. Additional technologies not listed above are not recommended and using them is at your own risk. We are looking at supporting other frontend frameworks like Angular and Vue, but they are not currently supported. We will accept and try to fix all issue reports that use the suggested technology stack for this project. Happy coding!

- [X] User Story #1: I can see an element with id="break-label" that contains a string (e.g. "Break Length").
- [X] User Story #2: I can see an element with id="session-label" that contains a string (e.g. "Session Length").
- [X] User Story #3: I can see two clickable elements with corresponding IDs: id="break-decrement" and id="session-decrement".
- [X] **User Story #4: I can see two clickable elements with corresponding IDs: id="break-increment" and id="session-increment".**
- [X] **User Story #5: I can see an element with a corresponding id="break-length", which by default (on load) displays a value of 5.**
- [X] User Story #6: I can see an element with a corresponding id="session-length", which by default displays a value of 25.
- [X] User Story #7: I can see an element with a corresponding id="timer-label", that contains a string indicating a session is initialized (e.g. "Session").
- [X] User Story #8: I can see an element with corresponding id="time-left". NOTE: Paused or running, the value in this field should always be displayed in mm:ss format (i.e. 25:00).
- [X] User Story #9: I can see a clickable element with a corresponding id="start_stop".
- [X] User Story #10: I can see a clickable element with a corresponding id="reset".
- [ ] User Story #11: When I click the element with the id of reset, any running timer should be stopped, the value within id="break-length" should return to 5, the value within id="session-length" should return to 25, and the element with id="time-left" should reset to it's default state.
- [X] User Story #12: When I click the element with the id of break-decrement, the value within id="break-length" decrements by a value of 1, and I can see the updated value.
- [X] User Story #13: When I click the element with the id of break-increment, the value within id="break-length" increments by a value of 1, and I can see the updated value.
- [X] User Story #14: When I click the element with the id of session-decrement, the value within id="session-length" decrements by a value of 1, and I can see the updated value.
- [X] User Story #15: When I click the element with the id of session-increment, the value within id="session-length" increments by a value of 1, and I can see the updated value.
- [X] User Story #16: I should not be able to set a session or break length to <= 0.
- [X] User Story #17: I should not be able to set a session or break length to > 60.
- [X] User Story #18: When I first click the element with id="start_stop", the timer should begin running from the value currently displayed in id="session-length", even if the value has been incremented or decremented from the original value of 25.
- [X] User Story #19: If the timer is running, the element with the id of time-left should display the remaining time in mm:ss format (decrementing by a value of 1 and updating the display every 1000ms).
- [ ] User Story #20: If the timer is running and I click the element with id="start_stop", the countdown should pause.
User Story #21: If the timer is paused and I click the element with id="start_stop", the countdown should resume running from the point at which it was paused.
- [ ] User Story #22: When a session countdown reaches zero (NOTE: timer MUST reach 00:00), and a new countdown begins, the element with the id of timer-label should display a string indicating a break has begun.
- [ ] User Story #23: When a session countdown reaches zero (NOTE: timer MUST reach 00:00), a new break countdown should begin, counting down from the value currently displayed in the id="break-length" element.
- [ ] User Story #24: When a break countdown reaches zero (NOTE: timer MUST reach 00:00), and a new countdown begins, the element with the id of timer-label should display a string indicating a session has begun.
- [ ] User Story #25: When a break countdown reaches zero (NOTE: timer MUST reach 00:00), a new session countdown should begin, counting down from the value currently displayed in the id="session-length" element.
- [ ] User Story #26: When a countdown reaches zero (NOTE: timer MUST reach 00:00), a sound indicating that time is up should play. This should utilize an HTML5 audio tag and have a corresponding id="beep".
- [ ] User Story #27: The audio element with id="beep" must be 1 second or longer.
- [ ] User Story #28: The audio element with id of beep must stop playing and be rewound to the beginning when the element with the id of reset is clicked.

You can build your project by forking this CodePen pen. Or you can use this CDN link to run the tests in any environment you like: https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js

Once you're done, submit the URL to your working project with all its tests passing.
Remember to use the Read-Search-Ask method if you get stuck.

**Solution:** https://codepen.io/johnny2136/pen/rZZMNq


**Link(s) to work**

1. Continued work on [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects). (Trying to use React on Redux)

**Introduction to the Front End Libraries Projects**

 -[x] Build a Random Quote Machine
 -[x] Build a Markdown Previewer
 -[x] Build a Drum Machine
 -[x] Build a JavaScript Calculator
 -[ ] Build a Pomodoro Clock

All code is in GitHub [Introduction to the Front End Libraries Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_Front_End_Libraries_Projects).

### Day 58: September 20, Wednesday

**Today 's Progress**: Took a break from the [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects).

**Thoughts**: Set up a local Open Shift cluster on my laptop, and deploying a test application into a tomcat container then make changes then roll back the changes Going to bed now :(

### Resources used:
  * [https://docs.okd.io/latest/minishift/getting-started/installing.html](https://docs.okd.io/latest/minishift/getting-started/installing.html)

All code is in GitHub [Introduction to the Front End Libraries Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_Front_End_Libraries_Projects).

### Day 57: September 19, Wednesday

**Today 's Progress**: Continued working on the [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects).

**Thoughts**: Still working on the fifth project toward the Front End Certification at free code camp. This one is pretty tough I am struggling to make the user stories pass. I need to refactor and try and do so without breaking the passing tests. I fixed the one broke user test now number six is failing to fix another ARRRRRRGGGGHHHHH!!!!! Going to bed now :(

### Resources used:
  * [Color tag editor](https://www.google.com/search?q=%234d4d4d&oq=%234d4d4d&aqs=chrome..69i57j69i61&sourceid=chrome&ie=UTF-8)
  * [Web Safe Fonts](https://www.w3schools.com/cssref/css_websafe_fonts.asp)
  * [Create-React-App](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md)


  **Front End Libraries Projects - Build a Pomodoro Clock**

**Objective:** Build a CodePen.io app that is functionally similar to this: https://codepen.io/freeCodeCamp/full/XpKrrW.

Fulfill the below user stories and get all of the tests to pass. Give it your own personal style.

You can use any mix of HTML, JavaScript, CSS, Bootstrap, SASS, React, Redux, and jQuery to complete this project. You should use a frontend framework (like React for example) because this section is about learning frontend frameworks. Additional technologies not listed above are not recommended and using them is at your own risk. We are looking at supporting other frontend frameworks like Angular and Vue, but they are not currently supported. We will accept and try to fix all issue reports that use the suggested technology stack for this project. Happy coding!

- [X] User Story #1: I can see an element with id="break-label" that contains a string (e.g. "Break Length").
- [X] User Story #2: I can see an element with id="session-label" that contains a string (e.g. "Session Length").
- [X] User Story #3: I can see two clickable elements with corresponding IDs: id="break-decrement" and id="session-decrement".
- [X] **User Story #4: I can see two clickable elements with corresponding IDs: id="break-increment" and id="session-increment".**
- [X] **User Story #5: I can see an element with a corresponding id="break-length", which by default (on load) displays a value of 5.**
- [ ] User Story #6: I can see an element with a corresponding id="session-length", which by default displays a value of 25.
- [ ] User Story #7: I can see an element with a corresponding id="timer-label", that contains a string indicating a session is initialized (e.g. "Session").
- [ ] User Story #8: I can see an element with corresponding id="time-left". NOTE: Paused or running, the value in this field should always be displayed in mm:ss format (i.e. 25:00).
- [ ] User Story #9: I can see a clickable element with a corresponding id="start_stop".
- [ ] User Story #10: I can see a clickable element with a corresponding id="reset".
- [ ] User Story #11: When I click the element with the id of reset, any running timer should be stopped, the value within id="break-length" should return to 5, the value within id="session-length" should return to 25, and the element with id="time-left" should reset to it's default state.
- [ ] User Story #12: When I click the element with the id of break-decrement, the value within id="break-length" decrements by a value of 1, and I can see the updated value.
- [ ] User Story #13: When I click the element with the id of break-increment, the value within id="break-length" increments by a value of 1, and I can see the updated value.
- [ ] User Story #14: When I click the element with the id of session-decrement, the value within id="session-length" decrements by a value of 1, and I can see the updated value.
- [ ] User Story #15: When I click the element with the id of session-increment, the value within id="session-length" increments by a value of 1, and I can see the updated value.
- [ ] User Story #16: I should not be able to set a session or break length to <= 0.
- [ ] User Story #17: I should not be able to set a session or break length to > 60.
- [ ] User Story #18: When I first click the element with id="start_stop", the timer should begin running from the value currently displayed in id="session-length", even if the value has been incremented or decremented from the original value of 25.
- [ ] User Story #19: If the timer is running, the element with the id of time-left should display the remaining time in mm:ss format (decrementing by a value of 1 and updating the display every 1000ms).
- [ ] User Story #20: If the timer is running and I click the element with id="start_stop", the countdown should pause.
User Story #21: If the timer is paused and I click the element with id="start_stop", the countdown should resume running from the point at which it was paused.
- [ ] User Story #22: When a session countdown reaches zero (NOTE: timer MUST reach 00:00), and a new countdown begins, the element with the id of timer-label should display a string indicating a break has begun.
- [ ] User Story #23: When a session countdown reaches zero (NOTE: timer MUST reach 00:00), a new break countdown should begin, counting down from the value currently displayed in the id="break-length" element.
- [ ] User Story #24: When a break countdown reaches zero (NOTE: timer MUST reach 00:00), and a new countdown begins, the element with the id of timer-label should display a string indicating a session has begun.
- [ ] User Story #25: When a break countdown reaches zero (NOTE: timer MUST reach 00:00), a new session countdown should begin, counting down from the value currently displayed in the id="session-length" element.
- [ ] User Story #26: When a countdown reaches zero (NOTE: timer MUST reach 00:00), a sound indicating that time is up should play. This should utilize an HTML5 audio tag and have a corresponding id="beep".
- [ ] User Story #27: The audio element with id="beep" must be 1 second or longer.
- [ ] User Story #28: The audio element with id of beep must stop playing and be rewound to the beginning when the element with the id of reset is clicked.

You can build your project by forking this CodePen pen. Or you can use this CDN link to run the tests in any environment you like: https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js

Once you're done, submit the URL to your working project with all its tests passing.
Remember to use the Read-Search-Ask method if you get stuck.

**Solution:** https://codepen.io/johnny2136/pen/rZZMNq


**Link(s) to work**

1. Continued work on [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects). (Trying to use React on Redux)

**Introduction to the Front End Libraries Projects**

 -[x] Build a Random Quote Machine
 -[x] Build a Markdown Previewer
 -[x] Build a Drum Machine
 -[x] Build a JavaScript Calculator
 -[ ] Build a Pomodoro Clock

All code is in GitHub [Introduction to the Front End Libraries Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_Front_End_Libraries_Projects).

### Day 56: September 18, Tuesday

**Today 's Progress**: Continued working on the [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects).

**Thoughts**: Still working on the fifth project toward the Front End Certification at free code camp. This one is pretty tough I am struggling to make the user stories pass. I need to refactor and try and do so without breaking the passing tests. I broke one user test tying to fix another ARRRRRRGGGGHHHHH!!!!! Going to bed now :(

### Resources used:
  * [Color tag editor](https://www.google.com/search?q=%234d4d4d&oq=%234d4d4d&aqs=chrome..69i57j69i61&sourceid=chrome&ie=UTF-8)
  * [Web Safe Fonts](https://www.w3schools.com/cssref/css_websafe_fonts.asp)
  * [Create-React-App](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md)


  **Front End Libraries Projects - Build a Pomodoro Clock**

**Objective:** Build a CodePen.io app that is functionally similar to this: https://codepen.io/freeCodeCamp/full/XpKrrW.

Fulfill the below user stories and get all of the tests to pass. Give it your own personal style.

You can use any mix of HTML, JavaScript, CSS, Bootstrap, SASS, React, Redux, and jQuery to complete this project. You should use a frontend framework (like React for example) because this section is about learning frontend frameworks. Additional technologies not listed above are not recommended and using them is at your own risk. We are looking at supporting other frontend frameworks like Angular and Vue, but they are not currently supported. We will accept and try to fix all issue reports that use the suggested technology stack for this project. Happy coding!

- [X] User Story #1: I can see an element with id="break-label" that contains a string (e.g. "Break Length").
- [X] User Story #2: I can see an element with id="session-label" that contains a string (e.g. "Session Length").
- [X] User Story #3: I can see two clickable elements with corresponding IDs: id="break-decrement" and id="session-decrement".
- [ ] **User Story #4: I can see two clickable elements with corresponding IDs: id="break-increment" and id="session-increment".**
- [ ] User Story #5: I can see an element with a corresponding id="break-length", which by default (on load) displays a value of 5.
- [ ] User Story #6: I can see an element with a corresponding id="session-length", which by default displays a value of 25.
- [ ] User Story #7: I can see an element with a corresponding id="timer-label", that contains a string indicating a session is initialized (e.g. "Session").
- [ ] User Story #8: I can see an element with corresponding id="time-left". NOTE: Paused or running, the value in this field should always be displayed in mm:ss format (i.e. 25:00).
- [ ] User Story #9: I can see a clickable element with a corresponding id="start_stop".
- [ ] User Story #10: I can see a clickable element with a corresponding id="reset".
- [ ] User Story #11: When I click the element with the id of reset, any running timer should be stopped, the value within id="break-length" should return to 5, the value within id="session-length" should return to 25, and the element with id="time-left" should reset to it's default state.
- [ ] User Story #12: When I click the element with the id of break-decrement, the value within id="break-length" decrements by a value of 1, and I can see the updated value.
- [ ] User Story #13: When I click the element with the id of break-increment, the value within id="break-length" increments by a value of 1, and I can see the updated value.
- [ ] User Story #14: When I click the element with the id of session-decrement, the value within id="session-length" decrements by a value of 1, and I can see the updated value.
- [ ] User Story #15: When I click the element with the id of session-increment, the value within id="session-length" increments by a value of 1, and I can see the updated value.
- [ ] User Story #16: I should not be able to set a session or break length to <= 0.
- [ ] User Story #17: I should not be able to set a session or break length to > 60.
- [ ] User Story #18: When I first click the element with id="start_stop", the timer should begin running from the value currently displayed in id="session-length", even if the value has been incremented or decremented from the original value of 25.
- [ ] User Story #19: If the timer is running, the element with the id of time-left should display the remaining time in mm:ss format (decrementing by a value of 1 and updating the display every 1000ms).
- [ ] User Story #20: If the timer is running and I click the element with id="start_stop", the countdown should pause.
User Story #21: If the timer is paused and I click the element with id="start_stop", the countdown should resume running from the point at which it was paused.
- [ ] User Story #22: When a session countdown reaches zero (NOTE: timer MUST reach 00:00), and a new countdown begins, the element with the id of timer-label should display a string indicating a break has begun.
- [ ] User Story #23: When a session countdown reaches zero (NOTE: timer MUST reach 00:00), a new break countdown should begin, counting down from the value currently displayed in the id="break-length" element.
- [ ] User Story #24: When a break countdown reaches zero (NOTE: timer MUST reach 00:00), and a new countdown begins, the element with the id of timer-label should display a string indicating a session has begun.
- [ ] User Story #25: When a break countdown reaches zero (NOTE: timer MUST reach 00:00), a new session countdown should begin, counting down from the value currently displayed in the id="session-length" element.
- [ ] User Story #26: When a countdown reaches zero (NOTE: timer MUST reach 00:00), a sound indicating that time is up should play. This should utilize an HTML5 audio tag and have a corresponding id="beep".
- [ ] User Story #27: The audio element with id="beep" must be 1 second or longer.
- [ ] User Story #28: The audio element with id of beep must stop playing and be rewound to the beginning when the element with the id of reset is clicked.

You can build your project by forking this CodePen pen. Or you can use this CDN link to run the tests in any environment you like: https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js

Once you're done, submit the URL to your working project with all its tests passing.
Remember to use the Read-Search-Ask method if you get stuck.

**Solution:** https://codepen.io/johnny2136/pen/rZZMNq


**Link(s) to work**

1. Continued work on [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects). (Trying to use React on Redux)

**Introduction to the Front End Libraries Projects**

 -[x] Build a Random Quote Machine
 -[x] Build a Markdown Previewer
 -[x] Build a Drum Machine
 -[x] Build a JavaScript Calculator
 -[ ] Build a Pomodoro Clock

All code is in GitHub [Introduction to the Front End Libraries Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_Front_End_Libraries_Projects).

### Day 55: September 17, Monday

**Today 's Progress**: Continued working on the [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects).

**Thoughts**: Still working on the fifth project toward the Front End Certification at free code camp. This one is pretty tough I seem to be getting through some of the user stories but hey there are a lot more here than the other projects. I need to refactor and try and do so without breaking the passing tests.

### Resources used:
  * [Color tag editor](https://www.google.com/search?q=%234d4d4d&oq=%234d4d4d&aqs=chrome..69i57j69i61&sourceid=chrome&ie=UTF-8)
  * [Web Safe Fonts](https://www.w3schools.com/cssref/css_websafe_fonts.asp)
  * [Create-React-App](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md)


  **Front End Libraries Projects - Build a Pomodoro Clock**

**Objective:** Build a CodePen.io app that is functionally similar to this: https://codepen.io/freeCodeCamp/full/XpKrrW.

Fulfill the below user stories and get all of the tests to pass. Give it your own personal style.

You can use any mix of HTML, JavaScript, CSS, Bootstrap, SASS, React, Redux, and jQuery to complete this project. You should use a frontend framework (like React for example) because this section is about learning frontend frameworks. Additional technologies not listed above are not recommended and using them is at your own risk. We are looking at supporting other frontend frameworks like Angular and Vue, but they are not currently supported. We will accept and try to fix all issue reports that use the suggested technology stack for this project. Happy coding!

- [X] User Story #1: I can see an element with id="break-label" that contains a string (e.g. "Break Length").
- [X] User Story #2: I can see an element with id="session-label" that contains a string (e.g. "Session Length").
- [X] User Story #3: I can see two clickable elements with corresponding IDs: id="break-decrement" and id="session-decrement".
- [X] User Story #4: I can see two clickable elements with corresponding IDs: id="break-increment" and id="session-increment".
- [ ] User Story #5: I can see an element with a corresponding id="break-length", which by default (on load) displays a value of 5.
- [ ] User Story #6: I can see an element with a corresponding id="session-length", which by default displays a value of 25.
- [ ] User Story #7: I can see an element with a corresponding id="timer-label", that contains a string indicating a session is initialized (e.g. "Session").
- [ ] User Story #8: I can see an element with corresponding id="time-left". NOTE: Paused or running, the value in this field should always be displayed in mm:ss format (i.e. 25:00).
- [ ] User Story #9: I can see a clickable element with a corresponding id="start_stop".
- [ ] User Story #10: I can see a clickable element with a corresponding id="reset".
- [ ] User Story #11: When I click the element with the id of reset, any running timer should be stopped, the value within id="break-length" should return to 5, the value within id="session-length" should return to 25, and the element with id="time-left" should reset to it's default state.
- [ ] User Story #12: When I click the element with the id of break-decrement, the value within id="break-length" decrements by a value of 1, and I can see the updated value.
- [ ] User Story #13: When I click the element with the id of break-increment, the value within id="break-length" increments by a value of 1, and I can see the updated value.
- [ ] User Story #14: When I click the element with the id of session-decrement, the value within id="session-length" decrements by a value of 1, and I can see the updated value.
- [ ] User Story #15: When I click the element with the id of session-increment, the value within id="session-length" increments by a value of 1, and I can see the updated value.
- [ ] User Story #16: I should not be able to set a session or break length to <= 0.
- [ ] User Story #17: I should not be able to set a session or break length to > 60.
- [ ] User Story #18: When I first click the element with id="start_stop", the timer should begin running from the value currently displayed in id="session-length", even if the value has been incremented or decremented from the original value of 25.
- [ ] User Story #19: If the timer is running, the element with the id of time-left should display the remaining time in mm:ss format (decrementing by a value of 1 and updating the display every 1000ms).
- [ ] User Story #20: If the timer is running and I click the element with id="start_stop", the countdown should pause.
User Story #21: If the timer is paused and I click the element with id="start_stop", the countdown should resume running from the point at which it was paused.
- [ ] User Story #22: When a session countdown reaches zero (NOTE: timer MUST reach 00:00), and a new countdown begins, the element with the id of timer-label should display a string indicating a break has begun.
- [ ] User Story #23: When a session countdown reaches zero (NOTE: timer MUST reach 00:00), a new break countdown should begin, counting down from the value currently displayed in the id="break-length" element.
- [ ] User Story #24: When a break countdown reaches zero (NOTE: timer MUST reach 00:00), and a new countdown begins, the element with the id of timer-label should display a string indicating a session has begun.
- [ ] User Story #25: When a break countdown reaches zero (NOTE: timer MUST reach 00:00), a new session countdown should begin, counting down from the value currently displayed in the id="session-length" element.
- [ ] User Story #26: When a countdown reaches zero (NOTE: timer MUST reach 00:00), a sound indicating that time is up should play. This should utilize an HTML5 audio tag and have a corresponding id="beep".
- [ ] User Story #27: The audio element with id="beep" must be 1 second or longer.
- [ ] User Story #28: The audio element with id of beep must stop playing and be rewound to the beginning when the element with the id of reset is clicked.

You can build your project by forking this CodePen pen. Or you can use this CDN link to run the tests in any environment you like: https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js

Once you're done, submit the URL to your working project with all its tests passing.
Remember to use the Read-Search-Ask method if you get stuck.

**Solution:** https://codepen.io/johnny2136/pen/rZZMNq


**Link(s) to work**

1. Continued work on [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects). (Trying to use React on Redux)

**Introduction to the Front End Libraries Projects**

 -[x] Build a Random Quote Machine
 -[x] Build a Markdown Previewer
 -[x] Build a Drum Machine
 -[x] Build a JavaScript Calculator
 -[ ] Build a Pomodoro Clock

All code is in GitHub [Introduction to the Front End Libraries Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_Front_End_Libraries_Projects).

## Day 54: September 16, Sunday

**Today 's Progress**: Continued working on the [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects).

**Thoughts**: Started the fifth project toward the Front End Certification at free code camp. This one is going to take a lot of you tube video's!

### Resources used:
  * [Color tag editor](https://www.google.com/search?q=%234d4d4d&oq=%234d4d4d&aqs=chrome..69i57j69i61&sourceid=chrome&ie=UTF-8)
  * [Web Safe Fonts](https://www.w3schools.com/cssref/css_websafe_fonts.asp)
  * [Create-React-App](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md)


  **Front End Libraries Projects - Build a Pomodoro Clock**

**Objective:** Build a CodePen.io app that is functionally similar to this: https://codepen.io/freeCodeCamp/full/XpKrrW.

Fulfill the below user stories and get all of the tests to pass. Give it your own personal style.

You can use any mix of HTML, JavaScript, CSS, Bootstrap, SASS, React, Redux, and jQuery to complete this project. You should use a frontend framework (like React for example) because this section is about learning frontend frameworks. Additional technologies not listed above are not recommended and using them is at your own risk. We are looking at supporting other frontend frameworks like Angular and Vue, but they are not currently supported. We will accept and try to fix all issue reports that use the suggested technology stack for this project. Happy coding!

- [ ] User Story #1: I can see an element with id="break-label" that contains a string (e.g. "Break Length").
- [ ] User Story #2: I can see an element with id="session-label" that contains a string (e.g. "Session Length").
- [ ] User Story #3: I can see two clickable elements with corresponding IDs: id="break-decrement" and id="session-decrement".
- [ ] User Story #4: I can see two clickable elements with corresponding IDs: id="break-increment" and id="session-increment".
- [ ] User Story #5: I can see an element with a corresponding id="break-length", which by default (on load) displays a value of 5.
- [ ] User Story #6: I can see an element with a corresponding id="session-length", which by default displays a value of 25.
- [ ] User Story #7: I can see an element with a corresponding id="timer-label", that contains a string indicating a session is initialized (e.g. "Session").
- [ ] User Story #8: I can see an element with corresponding id="time-left". NOTE: Paused or running, the value in this field should always be displayed in mm:ss format (i.e. 25:00).
- [ ] User Story #9: I can see a clickable element with a corresponding id="start_stop".
- [ ] User Story #10: I can see a clickable element with a corresponding id="reset".
- [ ] User Story #11: When I click the element with the id of reset, any running timer should be stopped, the value within id="break-length" should return to 5, the value within id="session-length" should return to 25, and the element with id="time-left" should reset to it's default state.
- [ ] User Story #12: When I click the element with the id of break-decrement, the value within id="break-length" decrements by a value of 1, and I can see the updated value.
- [ ] User Story #13: When I click the element with the id of break-increment, the value within id="break-length" increments by a value of 1, and I can see the updated value.
- [ ] User Story #14: When I click the element with the id of session-decrement, the value within id="session-length" decrements by a value of 1, and I can see the updated value.
- [ ] User Story #15: When I click the element with the id of session-increment, the value within id="session-length" increments by a value of 1, and I can see the updated value.
- [ ] User Story #16: I should not be able to set a session or break length to <= 0.
- [ ] User Story #17: I should not be able to set a session or break length to > 60.
- [ ] User Story #18: When I first click the element with id="start_stop", the timer should begin running from the value currently displayed in id="session-length", even if the value has been incremented or decremented from the original value of 25.
- [ ] User Story #19: If the timer is running, the element with the id of time-left should display the remaining time in mm:ss format (decrementing by a value of 1 and updating the display every 1000ms).
- [ ] User Story #20: If the timer is running and I click the element with id="start_stop", the countdown should pause.
User Story #21: If the timer is paused and I click the element with id="start_stop", the countdown should resume running from the point at which it was paused.
- [ ] User Story #22: When a session countdown reaches zero (NOTE: timer MUST reach 00:00), and a new countdown begins, the element with the id of timer-label should display a string indicating a break has begun.
- [ ] User Story #23: When a session countdown reaches zero (NOTE: timer MUST reach 00:00), a new break countdown should begin, counting down from the value currently displayed in the id="break-length" element.
- [ ] User Story #24: When a break countdown reaches zero (NOTE: timer MUST reach 00:00), and a new countdown begins, the element with the id of timer-label should display a string indicating a session has begun.
- [ ] User Story #25: When a break countdown reaches zero (NOTE: timer MUST reach 00:00), a new session countdown should begin, counting down from the value currently displayed in the id="session-length" element.
- [ ] User Story #26: When a countdown reaches zero (NOTE: timer MUST reach 00:00), a sound indicating that time is up should play. This should utilize an HTML5 audio tag and have a corresponding id="beep".
- [ ] User Story #27: The audio element with id="beep" must be 1 second or longer.
- [ ] User Story #28: The audio element with id of beep must stop playing and be rewound to the beginning when the element with the id of reset is clicked.

You can build your project by forking this CodePen pen. Or you can use this CDN link to run the tests in any environment you like: https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js

Once you're done, submit the URL to your working project with all its tests passing.
Remember to use the Read-Search-Ask method if you get stuck.

**Solution:** https://codepen.io/johnny2136/pen/rZZMNq


**Link(s) to work**

1. Continued work on [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects). (Trying to use React on Redux)

**Introduction to the Front End Libraries Projects**

 -[x] Build a Random Quote Machine
 -[x] Build a Markdown Previewer
 -[x] Build a Drum Machine
 -[x] Build a JavaScript Calculator
 -[ ] Build a Pomodoro Clock

All code is in GitHub [Introduction to the Front End Libraries Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_Front_End_Libraries_Projects).


![xkcd](http://imgs.xkcd.com/comics/escape_artist.png)

### Day 53: September 15, Saturday

**Today 's Progress**: Continued working on the [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects).

**Thoughts**: Finished the fourth project toward the Front End Certification at free code camp. I'm glad that's done this one took two days and a lot of you tube video's!

### Resources used:
  * [Build a Markdown Previewer](https://www.freeformatter.com/regex-tester.html)
  * [https://github.com/alvarotrigo/fullPage.js/issues/854](https://github.com/alvarotrigo/fullPage.js/issues/854)
  * [Color tag editor](https://www.google.com/search?q=%234d4d4d&oq=%234d4d4d&aqs=chrome..69i57j69i61&sourceid=chrome&ie=UTF-8)
  * [Web Safe Fonts](https://www.w3schools.com/cssref/css_websafe_fonts.asp)
  * [Create-React-App](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md)
  * [Create a simple calculator app in react Medium.com](https://medium.com/@krissanawat/create-a-simple-calculator-app-in-react-742022250d8f)
  * [RegExr Test Site](https://regexr.com/)

  **Front End Libraries Projects - Build a JavaScript Calculator**

  Objective: Build a CodePen.io app that is functionally similar to this: https://codepen.io/freeCodeCamp/full/wgGVVX.

  Fulfill the below user stories and get all of the tests to pass. Give it your own personal style.
  You can use any mix of HTML, JavaScript, CSS, Bootstrap, SASS, React, Redux, and jQuery to complete this project. You should use a frontend framework (like React for example) because this section is about learning frontend frameworks. Additional technologies not listed above are not recommended and using them is at your own risk. We are looking at supporting other frontend frameworks like Angular and Vue, but they are not currently supported. We will accept and try to fix all issue reports that use the suggested technology stack for this project. Happy coding!

  - [x] User Story #1: My calculator should contain a clickable element containing an = (equal sign) with a corresponding id="equals".
  - [x] User Story #2: My calculator should contain 10 clickable elements containing one number each from 0-9, with the following corresponding IDs: id="zero", id="one", id="two", id="three", id="four", id="five", id="six", id="seven", id="eight", and id="nine".
  - [x] User Story #3: My calculator should contain 4 clickable elements each containing one of the 4 primary mathematical operators with the following corresponding IDs: id="add", id="subtract", id="multiply", id="divide".
  - [x] User Story #4: My calculator should contain a clickable element containing a . (decimal point) symbol with a corresponding id="decimal".
  - [x] User Story #5: My calculator should contain a clickable element with an id="clear".
  - [x] User Story #6: My calculator should contain an element to display values with a corresponding id="display".
  - [x] User Story #7: At any time, pressing the clear button clears the input and output values, and returns the calculator to its initialized state; 0 should be shown in the element with the id of display.
  - [x] User Story #8: As I input numbers, I should be able to see my input in the element with the id of display.
  - [x] User Story #9: In any order, I should be able to add, subtract, multiply and divide a chain of numbers of any length, and when I hit =, the correct result should be shown in the element with the id of display.
  - [x] User Story #10: When inputting numbers, my calculator should not allow a number to begin with multiple zeros.
  - [x] User Story #11: When the decimal element is clicked, a . should append to the currently displayed value; two . in one number should not be accepted.
  - [x] User Story #12: I should be able to perform any operation ``(+, -, *, /)`` on numbers containing decimal points.
  - [x] User Story #13: If 2 or more operators are entered consecutively, the operation performed should be the last operator entered.
  - [x] User Story #14: Pressing an operator immediately following = should start a new calculation that operates on the result of the previous evaluation.
  - [x] User Story #15: My calculator should have several decimal places of precision when it comes to rounding (note that there is no exact standard, but you should be able to handle calculations like 2 / 7 with reasonable precision to at least 4 decimal places).

  *Note On Calculator Logic:* It should be noted that there are two main schools of thought on calculator input logic: immediate execution logic and formula logic. Our example utilizes formula logic and observes order of operation precedence, immediate execution does not. Either is acceptable, but please note that depending on which you choose, your calculator may yield different results than ours for certain equations (see below example). As long as your math can be verified by another production calculator, please do not consider this a bug.

  EXAMPLE: `3 + 5 x 6 - 2 / 4 =`
  Immediate Execution Logic: `11.5`
  Formula/Expression Logic: `32.5`

  You can build your project by forking this [CodePen pen](https://codepen.io/freeCodeCamp/pen/MJjpwO). Or you can use this CDN link to run the tests in any environment you like: https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js

  Once you're done, submit the URL to your working project with all its tests passing.
  Remember to use the Read-Search-Ask method if you get stuck.

  Solution: https://codepen.io/johnny2136/pen/jvppEM

  Resources:
  https://www.hexcolortool.com/AC3939#109428

  https://freshman.tech/calculator/

  https://developers.google.com/web/updates/2016/04/keyboardevent-keys-codes

  https://www.w3.org/Style/Examples/007/fonts.en.html

  https://www.spycolor.com/web-safe-colors

  https://css-tricks.com/inheriting-box-sizing-probably-slightly-better-best-practice/

  https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent/key

  https://developer.mozilla.org/en-US/docs/Web/Events/keydown#Related_Events

  https://medium.freecodecamp.org/how-to-bind-this-in-react-without-a-constructor-3a694f5d1b34



![Image of projects](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/JavaScriptCalculator.png)

**Link(s) to work**

1. Continued work on [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects). (Trying to use React on Redux)

**Introduction to the Front End Libraries Projects**

 -[x] Build a Random Quote Machine
 -[x] Build a Markdown Previewer
 -[x] Build a Drum Machine
 -[x] Build a JavaScript Calculator
 -[ ] Build a Pomodoro Clock

All code is in GitHub [Introduction to the Front End Libraries Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_Front_End_Libraries_Projects).

![TGIF](http://wallpaperen.com/wp-content/uploads/2018/01/best-tgif-meme-funny-funny-friday-memes-enjoy-and-share-tgif-meme-funny.jpg)

### Day 52: September 14, Friday

**Today 's Progress**: Continued working on the [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects).

**Thoughts**: Finished the third project toward the Front End Certification at free code camp. I'm glad that's done!

### Resources used:
  * [Build a Markdown Previewer](https://codepen.io/freeCodeCamp/full/GrZVVO),
  * [https://codepen.io/](https://codepen.io/)

  **Front End Libraries Projects - Build a Drum Machine**
Objective: Build a CodePen.io app that is functionally similar to this: https://codepen.io/freeCodeCamp/full/MJyNMd.

Fulfill the below user stories and get all of the tests to pass. Give it your own personal style.

You can use any mix of HTML, JavaScript, CSS, Bootstrap, SASS, React, Redux, and jQuery to complete this project. You should use a frontend framework (like React for example) because this section is about learning frontend frameworks. Additional technologies not listed above are not recommended and using them is at your own risk. We are looking at supporting other frontend frameworks like Angular and Vue, but they are not currently supported. We will accept and try to fix all issue reports that use the suggested technology stack for this project. Happy coding!

- [x] User Story #1: I should be able to see an outer container with a corresponding id="drum-machine" that contains all other elements.
- [x] User Story #2: Within #drum-machine I can see an element with a corresponding id="display".
- [x] User Story #3: Within #drum-machine I can see 9 clickable drum pad elements, each with a class name of drum-pad, a unique id that describes the audio clip the drum pad will be set up to trigger, and an inner text that corresponds to one of the following keys on the keyboard: Q, W, E, A, S, D, Z, X, C. The drum pads MUST be in this order.
- [x] User Story #4: Within each .drum-pad, there should be an HTML5 audio element which has a src attribute pointing to an audio clip, a class name of clip, and an id corresponding to the inner text of its parent .drum-pad (e.g. id="Q", id="W", id="E" etc.).
- [x] User Story #5: When I click on a .drum-pad element, the audio clip contained in its child audio element should be triggered.
- [X] User Story #6: When I press the trigger key associated with each .drum-pad, the audio clip contained in its child audio element should be triggered (e.g. pressing the Q key should trigger the drum pad which contains the string "Q", pressing the W key should trigger the drum pad which contains the string "W", etc.).
- [x] User Story #7: When a .drum-pad is triggered, a string describing the associated audio clip is displayed as the inner text of the #display element (each string must be unique).

You can build your project by forking this CodePen pen. Or you can use this CDN link to run the tests in any environment you like: https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js
Once you're done, submit the URL to your working project with all its tests passing.
Remember to use the Read-Search-Ask method if you get stuck.

Solution: [https://codepen.io/johnny2136/pen/WgJYBK](https://codepen.io/johnny2136/pen/WgJYBK)


  * [CodePen: My Application](https://codepen.io/johnny2136/pen/WgJYBK)

![Image of projects](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/DrumMachine.png)

**Link(s) to work**

1. Continued work on [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects). (Trying to use React on Redux)

**Introduction to the Front End Libraries Projects**

 -[x] Build a Random Quote Machine
 -[x] Build a Markdown Previewer
 -[x] Build a Drum Machine
 -[ ] Build a JavaScript Calculator
 -[ ] Build a Pomodoro Clock

All code is in GitHub [Introduction to the Front End Libraries Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_Front_End_Libraries_Projects).


### Day 51: September 13, Thursday

**Today 's Progress**: Continued working on the [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects).

**Thoughts**: Still working on the third project toward the Front End Certification at free code camp. I officially hate this project!

### Resources used:
  * [Build a Markdown Previewer](https://codepen.io/freeCodeCamp/full/GrZVVO),
  * [https://codepen.io/](https://codepen.io/)

  **Front End Libraries Projects - Build a Drum Machine**
Objective: Build a CodePen.io app that is functionally similar to this: https://codepen.io/freeCodeCamp/full/MJyNMd.

Fulfill the below user stories and get all of the tests to pass. Give it your own personal style.

You can use any mix of HTML, JavaScript, CSS, Bootstrap, SASS, React, Redux, and jQuery to complete this project. You should use a frontend framework (like React for example) because this section is about learning frontend frameworks. Additional technologies not listed above are not recommended and using them is at your own risk. We are looking at supporting other frontend frameworks like Angular and Vue, but they are not currently supported. We will accept and try to fix all issue reports that use the suggested technology stack for this project. Happy coding!

- [x] User Story #1: I should be able to see an outer container with a corresponding id="drum-machine" that contains all other elements.
- [x] User Story #2: Within #drum-machine I can see an element with a corresponding id="display".
- [x] User Story #3: Within #drum-machine I can see 9 clickable drum pad elements, each with a class name of drum-pad, a unique id that describes the audio clip the drum pad will be set up to trigger, and an inner text that corresponds to one of the following keys on the keyboard: Q, W, E, A, S, D, Z, X, C. The drum pads MUST be in this order.
- [x] User Story #4: Within each .drum-pad, there should be an HTML5 audio element which has a src attribute pointing to an audio clip, a class name of clip, and an id corresponding to the inner text of its parent .drum-pad (e.g. id="Q", id="W", id="E" etc.).
- [x] User Story #5: When I click on a .drum-pad element, the audio clip contained in its child audio element should be triggered.
- [ ] User Story #6: When I press the trigger key associated with each .drum-pad, the audio clip contained in its child audio element should be triggered (e.g. pressing the Q key should trigger the drum pad which contains the string "Q", pressing the W key should trigger the drum pad which contains the string "W", etc.).
- [x] User Story #7: When a .drum-pad is triggered, a string describing the associated audio clip is displayed as the inner text of the #display element (each string must be unique).

You can build your project by forking this CodePen pen. Or you can use this CDN link to run the tests in any environment you like: https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js
Once you're done, submit the URL to your working project with all its tests passing.
Remember to use the Read-Search-Ask method if you get stuck.

Solution: [https://codepen.io/johnny2136/pen/WgJYBK](https://codepen.io/johnny2136/pen/WgJYBK)


  * [CodePen: My Application](https://codepen.io/johnny2136/pen/WgJYBK)

![Image of projects](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/Day50.png)

**Link(s) to work**

1. Continued work on [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects). (Trying to use React on Redux)

**Introduction to the Front End Libraries Projects**

 -[x] Build a Random Quote Machine
 -[x] Build a Markdown Previewer
 -[ ] Build a Drum Machine
 -[ ] Build a JavaScript Calculator
 -[ ] Build a Pomodoro Clock

All code is in GitHub [Introduction to the Front End Libraries Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_Front_End_Libraries_Projects).


### Day 50: September 12, Wednesday

**Today 's Progress**: Continued working on the [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects).

**Thoughts**: Started working on the third project toward the Front End Certification at free code camp.

### Resources used:
  * [Build a Markdown Previewer](https://codepen.io/freeCodeCamp/full/GrZVVO),
  * [https://codepen.io/](https://codepen.io/)

  **Front End Libraries Projects - Build a Drum Machine**
Objective: Build a CodePen.io app that is functionally similar to this: https://codepen.io/freeCodeCamp/full/MJyNMd.

Fulfill the below user stories and get all of the tests to pass. Give it your own personal style.

You can use any mix of HTML, JavaScript, CSS, Bootstrap, SASS, React, Redux, and jQuery to complete this project. You should use a frontend framework (like React for example) because this section is about learning frontend frameworks. Additional technologies not listed above are not recommended and using them is at your own risk. We are looking at supporting other frontend frameworks like Angular and Vue, but they are not currently supported. We will accept and try to fix all issue reports that use the suggested technology stack for this project. Happy coding!

- [x] User Story #1: I should be able to see an outer container with a corresponding id="drum-machine" that contains all other elements.
- [x] User Story #2: Within #drum-machine I can see an element with a corresponding id="display".
- [x] User Story #3: Within #drum-machine I can see 9 clickable drum pad elements, each with a class name of drum-pad, a unique id that describes the audio clip the drum pad will be set up to trigger, and an inner text that corresponds to one of the following keys on the keyboard: Q, W, E, A, S, D, Z, X, C. The drum pads MUST be in this order.
- [x] User Story #4: Within each .drum-pad, there should be an HTML5 audio element which has a src attribute pointing to an audio clip, a class name of clip, and an id corresponding to the inner text of its parent .drum-pad (e.g. id="Q", id="W", id="E" etc.).
- [x] User Story #5: When I click on a .drum-pad element, the audio clip contained in its child audio element should be triggered.
- [ ] User Story #6: When I press the trigger key associated with each .drum-pad, the audio clip contained in its child audio element should be triggered (e.g. pressing the Q key should trigger the drum pad which contains the string "Q", pressing the W key should trigger the drum pad which contains the string "W", etc.).
- [ ] User Story #7: When a .drum-pad is triggered, a string describing the associated audio clip is displayed as the inner text of the #display element (each string must be unique).

You can build your project by forking this CodePen pen. Or you can use this CDN link to run the tests in any environment you like: https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js
Once you're done, submit the URL to your working project with all its tests passing.
Remember to use the Read-Search-Ask method if you get stuck.

Solution: [https://codepen.io/johnny2136/pen/WgJYBK](https://codepen.io/johnny2136/pen/WgJYBK)


  * [CodePen: My Application](https://codepen.io/johnny2136/pen/WgJYBK)

![Image of projects](https://raw.githubusercontent.com/Johnny2136/johnny2136.github.io/master/images/Day50.png)

**Link(s) to work**

1. Started work on [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects). (Trying to use React on Redux)

**Introduction to the Front End Libraries Projects**

 -[x] Build a Random Quote Machine
 -[x] Build a Markdown Previewer
 -[ ] Build a Drum Machine
 -[ ] Build a JavaScript Calculator
 -[ ] Build a Pomodoro Clock

All code is in GitHub [Introduction to the Front End Libraries Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_Front_End_Libraries_Projects).

### Day 49: September 11, Tuesday

**Today 's Progress**: Continued working on the [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects).

**Thoughts**: Finished the second project toward the Front End Certification at free code camp.

### Resources used:
  * [Build a Markdown Previewer](https://codepen.io/freeCodeCamp/full/GrZVVO),
  * [https://codepen.io/](https://codepen.io/)

  **Front End Libraries Projects - Build a Markdown Previewer**

  Objective: Build a CodePen.io app that is functionally similar to this: https://codepen.io/freeCodeCamp/full/GrZVVO.

  Fulfill the below user stories and get all of the tests to pass. Give it your own personal style.
  You can use any mix of HTML, JavaScript, CSS, Bootstrap, SASS, React, Redux, and jQuery to complete this project. You should use a frontend framework (like React for example) because this section is about learning frontend frameworks. Additional technologies not listed above are not recommended and using them is at your own risk. We are looking at supporting other frontend frameworks like Angular and Vue, but they are not currently supported. We will accept and try to fix all issue reports that use the suggested technology stack for this project. Happy coding!

  - [x] User Story #1: I can see a textarea element with a corresponding id="editor".
  - [x] User Story #2: I can see an element with a corresponding id="preview".
  - [x] User Story #3: When I enter text into the #editor element, the #preview element is updated as I type to display the content of the textarea.
  - [x] User Story #4: When I enter GitHub flavored markdown into the #editor element, the text is rendered as HTML in the #preview element as I type (HINT: You don't need to parse Markdown yourself - you can import the Marked library for this: https://cdnjs.com/libraries/marked).
  - [X] User Story #5: When my markdown previewer first loads, the default text in the #editor field should contain valid markdown that represents at least one of each of the following elements: a header (H1 size), a sub header (H2 size), a link, inline code, a code block, a list item, a blockquote, an image, and bolded text.
  - [X] User Story #6: When my markdown previewer first loads, the default markdown in the #editor field should be rendered as HTML in the #preview element.
  - [X] Optional Bonus (you do not need to make this test pass): When I click a link rendered by my markdown previewer, the link is opened up in a new tab (HINT: read the Marked.js docs for this one!).
  - [X] Optional Bonus (you do not need to make this test pass): My markdown previewer interprets carriage returns and renders them as br (line break) elements.

  You can build your project by forking this [CodePen pen](https://codepen.io/freeCodeCamp/pen/MJjpwO). Or you can use this CDN link to run the tests in any environment you like: https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js
  Once you're done, submit the URL to your working project with all its tests passing.
  Remember to use the Read-Search-Ask method if you get stuck.

  Solution:(https://codepen.io/johnny2136/pen/aaqYWv)

  * [CodePen: My Application](https://codepen.io/johnny2136/pen/aaqYWv)

![Image of projects](https://raw.githubusercontent.com/Johnny2136/FCC-Projects/master/images/FCCProject2.png)

**Link(s) to work**

1. Started work on [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects). (Trying to use React on Redux)

**Introduction to the Front End Libraries Projects**

 -[] Build a Markdown Previewer

All code is in GitHub [Introduction to the Front End Libraries Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_Front_End_Libraries_Projects).

### Day 48: September 10, Monday

**Today 's Progress**: Continued working on the [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects).

**Thoughts**: Continued working on the second project toward the Front End Certification at free code camp.

### Resources used:
  * [Build a Markdown Previewer](https://codepen.io/freeCodeCamp/full/GrZVVO),
  * [https://codepen.io/](https://codepen.io/)

  # Front End Libraries Projects - Build a Markdown Previewer

  Objective: Build a CodePen.io app that is functionally similar to this: https://codepen.io/freeCodeCamp/full/GrZVVO.

  Fulfill the below user stories and get all of the tests to pass. Give it your own personal style.
  You can use any mix of HTML, JavaScript, CSS, Bootstrap, SASS, React, Redux, and jQuery to complete this project. You should use a frontend framework (like React for example) because this section is about learning frontend frameworks. Additional technologies not listed above are not recommended and using them is at your own risk. We are looking at supporting other frontend frameworks like Angular and Vue, but they are not currently supported. We will accept and try to fix all issue reports that use the suggested technology stack for this project. Happy coding!

  - [x] User Story #1: I can see a textarea element with a corresponding id="editor".
  - [x] User Story #2: I can see an element with a corresponding id="preview".
  - [x] User Story #3: When I enter text into the #editor element, the #preview element is updated as I type to display the content of the textarea.
  - [x] User Story #4: When I enter GitHub flavored markdown into the #editor element, the text is rendered as HTML in the #preview element as I type (HINT: You don't need to parse Markdown yourself - you can import the Marked library for this: https://cdnjs.com/libraries/marked).
  - [ ] User Story #5: When my markdown previewer first loads, the default text in the #editor field should contain valid markdown that represents at least one of each of the following elements: a header (H1 size), a sub header (H2 size), a link, inline code, a code block, a list item, a blockquote, an image, and bolded text.
  - [ ] User Story #6: When my markdown previewer first loads, the default markdown in the #editor field should be rendered as HTML in the #preview element.
  - [ ] Optional Bonus (you do not need to make this test pass): When I click a link rendered by my markdown previewer, the link is opened up in a new tab (HINT: read the Marked.js docs for this one!).
  - [ ] Optional Bonus (you do not need to make this test pass): My markdown previewer interprets carriage returns and renders them as br (line break) elements.

  You can build your project by forking this [CodePen pen](https://codepen.io/freeCodeCamp/pen/MJjpwO). Or you can use this CDN link to run the tests in any environment you like: https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js
  Once you're done, submit the URL to your working project with all its tests passing.
  Remember to use the Read-Search-Ask method if you get stuck.

  Solution:(https://codepen.io/johnny2136/pen/aaqYWv)

  * [CodePen Example](https://codepen.io/johnny2136/pen/aaqYWv)

```HTML
<style>
 .box {
       display: flex;
          }
 .one {
       flex: 1;
          }
 .two {
       flex: 1;
          }
</style>
<body>

<div id="app"></div>

<script>
class App extends React.Component {  
  constructor(props) {
    super(props);
    this.state = {
      markdownInput: '# Heading\n## Sub-heading\n\n[This is a link.](https://www.freecodecamp.org)\n\n`This is inline code.`\n\n```\nThis is a code block.\n```\n\nThis is a list:\n* item 1\n* item 2\n* item 3\n\n> This is a blockquote.\n\n![Image](https://raw.githubusercontent.com/Johnny2136/FCC-Projects/master/images/images.png)\n\n**This is bolded text.**'
    };
    this.handleChange = this.handleChange.bind(this);
  }  
  handleChange(event) {
    this.setState({
      markdownInput: event.target.value
    });
  }  
  render() {    
    const renderer = new marked.Renderer();
    renderer.link = (href, title, text) => `<a href="${href}" target="_blank">${text}</a>`;    
    return (
      <div className="container-fluid">
        {/* HEADER */}
        <header>
          <h1 className="text-center app-heading">Markdown Previewer</h1>
        </header>
        <main>
          <div class="box">
            {/* EDIT TAB */}
            <div class="one" title=" Edit" >
              <textarea className="form-control" rows="20" aria-label="type GitHub Flavored Markdown text" onChange={(event) => this.handleChange(event)} value={this.state.markdownInput} id="editor"  />
            </div>
            {/* PREVIEW TAB */}
            <div class="two" title=" Preview">
              <div className="preview" dangerouslySetInnerHTML={{__html: marked(this.state.markdownInput, {breaks: true, renderer})}} id="preview"></div>
            </div>          
          </div>
        </main>
        {/* FOOTER */}
        <footer className="text-center">Coded by <a href="https://johnny2136.github.io/" target="_blank">Johnny2136</a></footer>
      </div>
    );
  }
};
ReactDOM.render(<App />, document.getElementById('app'));
</script>
</body>
```
**Link(s) to work**

1. Started work on [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects). (Trying to use React on Redux)

**Introduction to the Front End Libraries Projects**

 -[] Build a Markdown Previewer

All code is in GitHub [Introduction to the Front End Libraries Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_Front_End_Libraries_Projects).

### Day 47: September 9, Sunday

**Today 's Progress**: Started working on the [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects).

**Thoughts**: Completed first project toward the Front End Certification at freecodecamp.

### Resources used:
  * [Example Quote generator](https://codepen.io/c-herr/pen/dNWjby),
  * [https://codepen.io/](https://codepen.io/)
  * [JSFiddle version](https://jsfiddle.net/johnny2136/oz4aqpyL/2/)

**Front End Libraries Projects - Build a Random Quote Machine**

  Objective: Build a CodePen.io app that is functionally similar to this: https://codepen.io/freeCodeCamp/full/qRZeGZ.

  Fulfill the below user stories and get all of the tests to pass. Give it your own personal style.
  You can use any mix of HTML, JavaScript, CSS, Bootstrap, SASS, React, Redux, and jQuery to complete this project. You should use a frontend framework (like React for example) because this section is about learning frontend frameworks. Additional technologies not listed above are not recommended and using them is at your own risk. We are looking at supporting other frontend frameworks like Angular and Vue, but they are not currently supported. We will accept and try to fix all issue reports that use the suggested technology stack for this project. Happy coding!
  - [x] User Story #1: I can see a wrapper element with a corresponding id="quote-box".
  - [x] User Story #2: Within #quote-box, I can see an element with a corresponding id="text".
  - [x] User Story #3: Within #quote-box, I can see an element with a corresponding id="author".
  - [x] User Story #4: Within #quote-box, I can see a clickable element with a corresponding id="new-quote".
  - [x] User Story #5: Within #quote-box, I can see a clickable element with a corresponding id="tweet-quote".
  - [x] User Story #6: On first load, my quote machine displays a random quote in the element with id="text".
  - [x] User Story #7: On first load, my quote machine displays the random quote's author in the element with id="author".
  - [x] User Story #8: When the #new-quote button is clicked, my quote machine should fetch a new quote and display it in the #text element.
  - [x] User Story #9: My quote machine should fetch the new quote's author when the #new-quote button is clicked and display it in the #author element.
  - [x] User Story #10: I can tweet the current quote by clicking on the #tweet-quote a element. This a element should include the "twitter.com/intent/tweet" path in it's href attribute to tweet the current quote.
  - [x] User Story #11: The #quote-box wrapper element should be horizontally centered. Please run tests with browser's zoom level at 100% and page maximized.

  You can build your project by forking this CodePen pen. Or you can use this CDN link to run the tests in any environment you like: https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js
  Once you're done, submit the URL to your working project with all its tests passing.
  Remember to use the Read-Search-Ask method if you get stuck.

  Solution: https://codepen.io/johnny2136/pen/BOzEVz/

  * [JSFiddle version](https://jsfiddle.net/johnny2136/oz4aqpyL/2/)

  * [CodePen Example](https://codepen.io/johnny2136/pen/BOzEVz/)

```Javascript
const project_name = 'random-quote-machine';

const quotes = [{
  text: 'Well Bones, do the new medical facilities meet with your approval?',
  author: '-Kirk'
}, {
  text: 'Live long and prosper',
  author: '-Spock'
}, {
  text: 'Computers make excellent and efficient servants, but I have no wish to serve under them.',
  author: '-Spock'
}, {
  text: 'In critical moments, men sometimes see exactly what they wish to see.',
  author: '-Spock'
}, {
  text: 'When you eliminate the impossible, whatever remains, however improbable, must be the truth.',
  author: '-Spock'
}, {
text: 'The needs of the many outweigh the needs of the few.',
  author: '-Spock'
}, {
text: 'What am I, a doctor or a moon-shuttle conductor?',
  author: '-McCoy'
}, {
text: 'Resistance Is Futile',
  author: '-Borg '
}, {
text: 'In Space, all warriors are Cold Warriors.',
  author: '-Klingon Proverb'
}, {
  text: 'How we deal with death is at least as important as how we deal with life',
  author: '-Kirk'
}]

const textDiv = document.getElementById('text');
const authorDiv = document.getElementById('author');
const newQuoteBtn = document.getElementById('new-quote');
const tweetBtn = document.getElementById('tweet-quote');
let currentRnd = -1;

function fetchQuote() {
  let rnd;
  do {
    rnd = Math.floor(Math.random() * quotes.length)
  } while (currentRnd === rnd)

  currentRnd = rnd;

  textDiv.innerHTML = quotes[rnd].text;
  authorDiv.innerHTML = quotes[rnd].author;

  tweetBtn.setAttribute('href', `//twitter.com/intent/tweet?text=${textDiv.innerHTML}`)

}

(function() {
  fetchQuote();
})();

newQuoteBtn.addEventListener('click', () => {
  fetchQuote();
})
```
**Link(s) to work**

1. Started work on [Introduction to the Front End Libraries Projects](https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects). (Trying to use React on Redux)

**Introduction to the Front End Libraries Projects**

* PassedBuild a Random Quote Machine

All code is in GitHub [Introduction to the Front End Libraries Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_Front_End_Libraries_Projects).

!["Done with REACT/Redux!"](https://derpicdn.net/img/view/2012/9/16/99468__safe_pinkie+pie_sweet+and+elite_animated_partillery_party+cannon.gif)

## Day 46: September 8, Saturday

**Today 's Progress**: Finished work on the React on Redux challenges, One piece of advice I can give someone going through this is don't over think the misleading instructions. Google is your friend! The content is here: [Introduction to the React and Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/react-and-redux).

**Thoughts**: Took a several hours to figure this last one out. I think I must have read the instruction 10 times and trying to figure out how to tackle this monster. All I know is React and Redux are tough.

### Resources used:
  * [Redux middleware is not defined](https://stackoverflow.com/questions/32804097/redux-middleware-is-not-defined),
  * [https://codepen.io/](https://codepen.io/)


  **React and Redux: Moving Forward From Here**
  OMG I totally spent 2 hours trying to get this!!! TOTALLY TERRIBLE!
* Congratulations! You finished the lessons on React and Redux. There's one last item worth pointing out before you move on. Typically, you won't write React apps in a code editor like this. This challenge gives you a glimpse of what the syntax looks like if you're working with npm and a file system on your own machine. The code should look similar, except for the use of import statements (these pull in all of the dependencies that have been provided for you in the challenges). The "Managing Packages with npm" section covers npm in more detail.

Finally, writing React and Redux code generally requires some configuration. This can get complicated quickly. If you are interested in experimenting on your own machine, the

[Create React App](https://github.com/facebook/create-react-app) comes configured and ready to go.

Alternatively, you can enable Babel as a JavaScript Preprocessor in [CodePen](https://codepen.io/), add React and ReactDOM as external JavaScript resources, and work there as well.


**Log the message 'Now I know React and Redux!' to the console.**

```Javascript
// import React from 'react'
// import ReactDOM from 'react-dom'
// import { Provider, connect } from 'react-redux'
// import { createStore, combineReducers, applyMiddleware } from 'redux'
// import thunk from 'redux-thunk'

// import rootReducer from './redux/reducers'
// import App from './components/App'

// const store = createStore(
//   rootReducer,
//   applyMiddleware(thunk)
// );

// ReactDOM.render(
//   <Provider store={store}>
//     <App/>
//   </Provider>,
//   document.getElementById('root')
// );

// change code below this line
console.log('Now I know React and Redux!');//Added this to make test pass?????
```
**Link(s) to work**

1. Finished work on [Introduction to the React and Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/react-and-redux). (Trying to understand React on Redux)

**Introduction to the React and Redux Challenges**

* PassedMoving Forward From Here

All code is in GitHub [FCC_Challenges/ReactAndRedux.md](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/ReactAndRedux.md).


!["JavaScript just got harder REACT/Redux!"](http://imgs.xkcd.com/comics/ui_change.png)

### Day 45: September 7, Friday

**Today 's Progress**: Continuing work on the React on Redux challenge, here we go back to misleading instructions and no examples! I knew it was too good to be true!!! The content is here: [Introduction to the React and Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/react-and-redux).

**Thoughts**: Took a several hours to figure these out. First few weren't too bad, but the last one was pure hell! It had bad instructions no examples. I think these were written by different people. React and Redux would be easier to wrap my head around if there were more relevant examples. These challenges are getting slightly easier! once I got the solution the instructions sort of made sense but as I struggled I was cursing them!I think I was reading the instruction and trying to over think it. All I know is React and Redux are tough to get my head wrapped around.

### Resources used:
  * [GitHub react-redux Issues](https://github.com/reduxjs/react-redux/issues),
  * [Use Provider to Connect Redux to React](https://forum.freecodecamp.org/t/use-provider-to-connect-redux-to-react/202759)


  **Extract Local State into Redux**
  Once again back to misguiding instructions and no examples worked for a long time on this. TOTALLY TERRIBLE!
  * In the `Presentational` component, first, remove the `messages` property in the local `state`. These `messages` will be managed by Redux. Next, modify the `submitMessage()` method so that it dispatches `submitNewMessage()` from `this.props`, and pass in the current message input from local state as an argument. Because you removed messages from local state, remove the `messages` property from the call to `this.setState()` here as well. Finally, modify the `render()` method so that it maps over the messages received from `props` rather than `state`.

  * Once these changes are made, the app will continue to function the same, except Redux manages the `state`. This example also illustrates how a component may have local `state:` your component still tracks user input locally in its own `state`. You can see how Redux provides a useful state management framework on top of React. You achieved the same result using only React's local state at first, and this is usually possible with simple apps. However, as your apps become larger and more complex, so does your state management, and this is the problem Redux solves.


  ```Javascript
  // Redux:
  const ADD = 'ADD';
  const addMessage = (message) => {
    return {
      type: ADD,
      message: message
    }
  };
  const messageReducer = (state = [], action) => {
    switch (action.type) {
      case ADD:
        return [
          ...state,
          action.message
        ];
      default:
        return state;
    }
  };
  const store = Redux.createStore(messageReducer);
  // React:
  const Provider = ReactRedux.Provider;
  const connect = ReactRedux.connect;
  // Change code below this line
  class Presentational extends React.Component {
    constructor(props) {
      super(props);
      this.state = {
        input: '',
        //messages: []
      }
      this.handleChange = this.handleChange.bind(this);
      this.submitMessage = this.submitMessage.bind(this);
    }
    handleChange(event) {
      this.setState({
        input: event.target.value
      });
    }
    submitMessage() {
      this.setState({
        input: '',
        //messages: this.state.messages.concat(this.state.input)
      });
      this.props.submitNewMessage(this.state.input);
    }
    render() {
      return (
        <div>
          <h2>Type in a new Message:</h2>
          <input
            value={this.state.input}
            onChange={this.handleChange}/><br/>
          <button onClick={this.submitMessage}>Submit</button>
          <ul>
            {this.props.messages.map((message, idx) => { //changed state to props
                return (
                   <li key={idx}>{message}</li>
                );
              })
            };
          </ul>
        </div>
      );
    };
  };
  // Change code above this line
  const mapStateToProps = (state) => {
    return {messages: state}
  };
  const mapDispatchToProps = (dispatch) => {
    return {
      submitNewMessage: (message) => {
        dispatch(addMessage(message))
      }
    }
  };
  const Container = connect(mapStateToProps, mapDispatchToProps)(Presentational);
  class AppWrapper extends React.Component {
    render() {
      return (
        <Provider store={store}>
          <Container/>
        </Provider>
      );
    }
  };
  ```
**Link(s) to work**

1. Continued work on [Introduction to the React and Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/react-and-redux). (Trying to understand React on Redux)

**Introduction to the React and Redux Challenges**

* PassedMap State to Props
* PassedMap Dispatch to Props
* PassedConnect Redux to React
* PassedConnect Redux to the Messages App
* PassedExtract Local State into Redux

All code is in GitHub [FCC_Challenges/ReactAndRedux.md](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/ReactAndRedux.md).


!["Not too bad!"](http://diasporina.com/wp/wp-content/uploads/2016/12/ntb.png)

### Day 44: September 6, Thursday

**Today 's Progress**: Continuing work on the React on Redux challenge instructions are starting to make more sense but examples are not accurate. I refuse to let this get to me!!! The content is here: [Introduction to the React and Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/react-and-redux).

**Thoughts**: Took a couple hours to figure these out. First one was bad but the second one started making more sense! React and Redux would be easier to wrap my head around if there were more relevant examples. These challenges are getting slightly easier!

### Resources used:
  * [GitHub react-redux Issues](https://github.com/reduxjs/react-redux/issues),
  * [Use Provider to Connect Redux to React](https://forum.freecodecamp.org/t/use-provider-to-connect-redux-to-react/202759)
   

**Use Provider to Connect Redux to React**
This one wasn't too bad... (one change I would make is:)

*Example:*
```Javascript
render(){
    return(
      <Provider store={store}>
      <App/>
      </Provider>
    );
   };
   ```
The code editor now shows all your Redux and React code from the past several challenges. It includes the Redux store, actions, and the DisplayMessages component. The only new piece is the AppWrapper component at the bottom. Use this top level component to render the Provider from ReactRedux, and pass the Redux store as a prop. Then render the DisplayMessages component as a child. Once you are finished, you should see your React component rendered to the page.

Note: React Redux is available as a global variable here, so you can access the Provider with dot notation. The code in the editor takes advantage of this and sets it to a constant Provider for you to use in the AppWrapper render method.

[Can't get store from context #193](https://github.com/reduxjs/react-redux/issues/193)

```Javascript
// Redux Code:
const ADD = 'ADD';
const addMessage = (message) => {
  return {
    type: ADD,
    message
  }
};
const messageReducer = (state = [], action) => {
  switch (action.type) {
    case ADD:
      return [
        ...state,
        action.message
      ];
    default:
      return state;
  }
};
const store = Redux.createStore(messageReducer);

// React Code:
class DisplayMessages extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      input: '',
      messages: []
    }
    this.handleChange = this.handleChange.bind(this);
    this.submitMessage = this.submitMessage.bind(this);
  }
  handleChange(event) {
    this.setState({
      input: event.target.value
    });
  }
  submitMessage() {
    const currentMessage = this.state.input;
    this.setState({
      input: '',
      messages: this.state.messages.concat(currentMessage)
    });
  }
  render() {
    return (
      <div>
        <h2>Type in a new Message:</h2>
        <input
          value={this.state.input}
          onChange={this.handleChange}/><br/>
        <button onClick={this.submitMessage}>Submit</button>
        <ul>
          {this.state.messages.map( (message, idx) => {
              return (
                 <li key={idx}>{message}</li>
              )
            })
          }
        </ul>
      </div>
    );
  }
};
const Provider = ReactRedux.Provider;
class AppWrapper extends React.Component {
  // render the Provider here
    render(){
    return(
      <Provider store={store}>
        <DisplayMessages/>
      </Provider>
    );
  };
  // change code above this line
};
```
**Link(s) to work**

1. Continued work on [Introduction to the React and Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/react-and-redux). (Trying to understand React on Redux)

**Introduction to the React and Redux Challenges**

* PassedExtract State Logic to Redux
* PassedUse Provider to Connect Redux to React

All code is in GitHub [FCC_Challenges/ReactAndRedux.md](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/ReactAndRedux.md).



![EXTREAM FRUSTRATION..."](https://fafysio.files.wordpress.com/2015/03/frustrert.gif)

### Day 43: September 5, Wednesday

**Today 's Progress**: I started work on the pure hell of React on Redux with misleading instructions and no examples Really frustrating stuff! The hellish content is here: [Introduction to the React and Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/react-and-redux).

**Thoughts**: Took hours to figure these out. Worst of the worst! React and Redux would be easier to wrap my head around if there were accurate instructions and relevant examples these challenges are VERY hard!

### Resources used:
  * [Understanding unique keys for array children in React.js](https://stackoverflow.com/questions/28329382/understanding-unique-keys-for-array-children-in-react-js),
  * [React — to Bind or Not to Bind](https://medium.com/shoutem/react-to-bind-or-not-to-bind-7bf58327e22a)
  * [React and Redux: Manage State Locally First - freeCodeCamp Solution](https://www.youtube.com/watch?v=PPt0AS3RQ2Q)

  **Getting Started with React Redux**
  This should be a nice review of what you learned in the React lessons.(Just shoot me now!!!)
  Start with a DisplayMessages component. Add a constructor to this component and initialize it with a state that has two properties: input, that's set to an empty string, and messages, that's set to an empty array.
  [React Redux this.props.getClasses is not a function](https://stackoverflow.com/questions/50835770/react-redux-this-props-getclasses-is-not-a-function)
  ```javascript
  class DisplayMessages extends React.Component {
    // change code below this line
      constructor(props){
        super(props);
        this.state = {
          input:"",
          messages:[]
        }
      };    
    // change code above this line
    render() {
      return <div />
    }
  };
  ```

  **React and Redux: Manage State Locally First**
  WORST one YET!!!(Just shoot me now!!!)
  * First, in the render() method, have the component render an input element, button element, and ul element. When the input element changes, it should trigger a handleChange() method. Also, the input element should render the value of input that's in the component's state. The button element should trigger a submitMessage() method when it's clicked.

  * Second, write these two methods. The handleChange() method should update the input with what the user is typing. The submitMessage() method should concatenate the current message (stored in input) to the messages array in local state, and clear the value of the input.

  * Finally, use the ul to map over the array of messages and render it to the screen as a list of li elements.
  * [React Redux youTube Video on this challange](https://www.youtube.com/watch?v=PPt0AS3RQ2Q)
  ```javascript
  class DisplayMessages extends React.Component {
    constructor(props) {
      super(props);
      this.state = {
        input: '',
        messages: []
      }
      this.handleChange=this.handleChange.bind(this)//had to bind handleChange
      this.submitMessage=this.submitMessage.bind(this)//had to bind submitMessage
    }
    // add handleChange() and submitMessage() methods here
    handleChange(event){
      this.setState({
        input: event.target.value
      })    
    }
    submitMessage(){
      this.setState({
        messages: [...this.state.messages,this.state.input],
        input: ''
      })    
    }
    render() {
      return (
        <div>
          <h2>Type in a new Message:</h2>
          { /* render an input, button, and ul here */ }
            <input value={this.state.input} onChange={this.handleChange}/>

            <button onClick={this.submitMessage}>Submit</button>
            <ul>
            {this.state.messages.map(message => <li key={Date}>{message}</li>)}
            </ul>
          { /* change code above this line */ }
        </div>
      );
    }
  };
  ```
**Link(s) to work**

1. Started work on [Introduction to the React and Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/react-and-redux). (trying to) learn React on Redux.

**Introduction to the React Challenges**

* PassedGetting Started with React Redux
* PassedManage State Locally First

All code is in GitHub [FCC_Challenges/ReactAndRedux.md](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/ReactAndRedux.md).



![Day 42 "the answer to the greatest question of the universe and everything..."](https://vignette.wikia.nocookie.net/googology/images/e/e0/954.jpg/revision/latest?cb=20180103021656)

## Day 42: September 4, Tuesday

**Today 's Progress**: I finished work on Redux [Introduction to the Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/redux).

**Thoughts**: Done with Redux and will start React and Redux tomorrow misleading instructions and no relevant examples these challenges are NOT a good way to learn these two frameworks.

### Resources used:
  * [Using Object Spread Operator](https://redux.js.org/recipes/usingobjectspreadoperator),
  * [Is this the correct way to delete an item using redux?](hhttps://stackoverflow.com/questions/34582678/is-this-the-correct-way-to-delete-an-item-using-redux)

  ## Remove an Item from an Array
  Instructions sucked and an example would have been nice...
  Finish writing the reducer so a new state array is returned with the item at the specific index removed.
  ```Redux
  const immutableReducer = (state = [0,1,2,3,4,5], action) => {
    switch(action.type) {
      case 'REMOVE_ITEM':
        // don't mutate state here or the tests will fail
        let newArr = [...state.filter((elem, idx) => { // [1,2,3,5]
          return idx !== action.index
        })];
        return newArr;
      default:
        return state;
    }
  };
  const removeItem = (index) => {
    return {
      type: 'REMOVE_ITEM',
      index
    }
  };
  const store = Redux.createStore(immutableReducer);
  ```

  ## Copy an Object with Object.assign
  Edit the code to return a new state object for actions with type ONLINE, which set the status property to the string online. Try to use Object.assign() to complete the challenge.
  ```Redux
  const defaultState = {
    user: 'CamperBot',
    status: 'offline',
    friends: '732,982',
    community: 'freeCodeCamp'
  };
  const immutableReducer = (state = defaultState, action) => {
    switch(action.type) {
      case 'ONLINE':
        // don't mutate state here or the tests will fail
        const newObject = Object.assign({}, state, {status:'online'})
        return newObject;
      default:
        return state;
    }
  };
  const wakeUp = () => {
    return {
      type: 'ONLINE'
    }
  };
  const store = Redux.createStore(immutableReducer);
  ```
**Link(s) to work**

1. Finished work on [Introduction to the Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/redux) (trying to) learn Redux.

**Introduction to the React Challenges**

* PassedRemove an Item from an Array
* PassedCopy an Object with Object.assign

All code is in GitHub [FCC-Introduction to the redux Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/redux.md).

![Image from React and Redux](http://onsen.io.s3-website-us-east-1.amazonaws.com/blog/content/images/2016/Jun/react_redux.png)

### Day 41: September, Monday

**Today 's Progress**: I continued work on Redux [Introduction to the Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/redux).

**Thoughts**: Only two more Redux before I go on to React and Redux (I know lucky me) ambiguous instructions hardly no relevant examples I don't think these challenges are a good way to learn these two frameworks.

### Resources used:
  * [4 ways to dispatch actions with Redux](https://blog.bam.tech/developper-news/4-ways-to-dispatch-actions-with-redux),
  * [React Redux this.props.getClasses is not a function](https://stackoverflow.com/questions/50835770/react-redux-this-props-getclasses-is-not-a-function)

```Redux
const INCREMENT = 'INCREMENT'; // define a constant for increment action types
const DECREMENT = 'DECREMENT'; // define a constant for decrement action types
const counterReducer = (state = 0, action) => {
  switch(action.type){
  case INCREMENT:
    return state + 1;
    break;
  case DECREMENT :
    return state -1;
    break;
  default:
    return state;
  }  
}; // define the counter reducer which will increment or decrement the state based on the action it receives
const incAction = () => {
  return {
    type : INCREMENT
  }
}; // define an action creator for incrementing
const decAction = () => {  
  return {
    type: DECREMENT
  }  
}; // define an action creator for decrementing
const store = Redux.createStore(counterReducer); // define the Redux store here, passing in your reducers
```

Worst one yet!!! poor instructions and no clear examples expects you to look at past challenges..

**Link(s) to work**

1. Continued work on [Introduction to the Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/redux) (trying to) learn Redux.

**Introduction to the React Challenges**

* PassedRegister a Store Listener
* PassedCombine Multiple Reducers
* PassedSend Action Data to the Store
* PassedUse Middleware to Handle Asynchronous Actions
* PassedWrite a Counter with Redux
* PassedNever Mutate State
* PassedUse the Spread Operator on Arrays

All code is in GitHub [FCC-Introduction to the redux Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/redux.md).


![Image from XKCD](https://imgs.xkcd.com/comics/wisdom_of_the_ancients.png)

### Day 40: September, Sunday

**Today 's Progress**: I continued work on Redux [Introduction to the Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/redux).

**Thoughts**: Redux and react are pretty crappy!

### Resources used:
  * [What listener() does in the Redux store?](https://stackoverflow.com/questions/36163442/what-listener-does-in-the-redux-store),
  * [Redux Dispatch With Event Listeners](https://learn.co/lessons/redux-dispatch-with-event-listeners)

```Redux
const ADD = 'ADD';
const reducer = (state = 0, action) => {
  switch(action.type) {
    case ADD:
      return state + 1;
    default:
      return state;
  }
};
const store = Redux.createStore(reducer);
// global count variable:
let count = 0;
// change code below this line
const incrementCounter = () => count +=1
store.subscribe(incrementCounter);
// change code above this line
store.dispatch({type: ADD});
console.log(count);
store.dispatch({type: ADD});
console.log(count);
store.dispatch({type: ADD});
console.log(count);
```

This was a pretty hard challenge, instructions were not very clear at all and there were no examples.

**Link(s) to work**

1. Continued work on [Introduction to the Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/redux) (trying to) learn Redux.

**Introduction to the React Challenges**

* PassedDispatch an Action Event
* PassedHandle an Action in the Store
* PassedUse a Switch Statement to Handle Multiple Actions
* PassedUse const for Action Types

All code is in GitHub [FCC-Introduction to the redux Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/redux.md).


### Day 39: September, Saturday

**Today 's Progress**: I started Redux [Introduction to the Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/redux).

**Thoughts**: Just when you think you are done with a frustrating framework, there comes Redux ARRRRGGGGHHHH!!!!! Worse than ReactJS!!!!

### Resources used:
  * [A Simple Naming Convention for Action Creators in Redux.js](https://decembersoft.com/posts/a-simple-naming-convention-for-action-creators-in-redux-js/)
```Redux
const action = {
  type: 'LOGIN'
}
// Define an action creator here:
function actionCreator(action){
    return {
        type: LOGIN,
    action
    };
};
```

This was a VERY hard challenge, instructions were not very clear at all and there were no examples.

**Link(s) to work**

1. Started work on [Introduction to the Redux Challenges](https://learn.freecodecamp.org/front-end-libraries/redux) learning Redux.

**Introduction to the React Challenges**

* PassedCreate a Redux Store
* PassedGet State from the Redux Store
* PassedDefine a Redux Action
* PassedDefine an Action Creator

All code is in GitHub [FCC-Introduction to the redux Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/redux.md).


### Day 38: August 31, Friday

**Today 's Progress**: I finally finished React.js [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react).

**Thoughts**: I AM SO HAPPY the React challenges are finally done. I don't like ReactJS

### Resources used:
  * [reactjs.org/docs/getting-started](https://reactjs.org/docs/getting-started.html)

```reactjs
//Give Sibling Elements a Unique Key Attribute
const frontEndFrameworks = [
  'React',
  'Angular',
  'Ember',
  'Knockout',
  'Backbone',
  'Vue'
];
function Frameworks() {
  // change code here
  const renderFrameworks = frontEndFrameworks.map((renderFrameworks) => <li key={renderFrameworks.toString()}>{renderFrameworks}</li>)
  return (
    <div>
      <h1>Popular Front End JavaScript Frameworks</h1>
      <ul>
        {renderFrameworks}
      </ul>
    </div>
  );
};



//Use Array.filter() to Dynamically Filter an Array
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      users: [
        {
          username: 'Jeff',
          online: true
        },
        {
          username: 'Alan',
          online: false
        },
        {
          username: 'Mary',
          online: true
        },
        {
          username: 'Jim',
          online: false
        },
        {
          username: 'Sara',
          online: true
        },
        {
          username: 'Laura',
          online: true
        }
      ]
    }
  }
  render() {
    const usersOnline = this.state.users.filter(user => user.online); // change code here
    const renderOnline = usersOnline.map(x => <li key={x.username}>{x.username}</li>); // change code here
    return (
       <div>
         <h1>Current Online Users:</h1>
         <ul>
           {renderOnline}
         </ul>
       </div>
    );
  }
};



//Render React on the Server with renderToString
class App extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return <div/>
  }
};
// change code below this line
ReactDOMServer.renderToString(<App />);
```

This was a VERY hard challenge, instructions were not very clear and for the most part examples were non existent.

**Link(s) to work**

1. Finished work on [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react) learning React.js.

**Introduction to the React Challenges**

* PassedChange Inline CSS Conditionally Based on Component State
* PassedUse Array.map() to Dynamically Render Elements
* PassedGive Sibling Elements a Unique Key Attribute
* PassedUse Array.filter() to Dynamically Filter an Array
* PassedRender React on the Server with renderToString

All code is in GitHub [FCC-Introduction to the React Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/reactjs.txt).



## Day 37: August 30, Thursday

**Today 's Progress**: I continued work on React.js [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react).

**Thoughts**: Still struggling through the React challenges I did find some examples through google. I endeavor to persevere. Tonight it was pretty hard I hope this helps with [React: Render Conditionally from Props](https://learn.freecodecamp.org/front-end-libraries/react/render-conditionally-from-props)

### Resources used:
  * [reactjs.org/docs/getting-started](https://reactjs.org/docs/getting-started.html)

```reactjs
//Render Conditionally from Props
//This was totally awful... poor instructions, no good examples, took a long time to get this.
class Results extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
   /* change code here ALSO!!! (but this isn't in the original setup!) */
   const { fiftyFifty } = this.props;
    return (
      <h1>
      {
        /* change code here */
        fiftyFifty ? 'You Win!' : 'You Lose!'
      }
      </h1>
    )
  };
};
class GameOfChance extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      counter: 1
    }
    this.handleClick = this.handleClick.bind(this);
  }
  handleClick() {
    this.setState({
      counter: this.state.counter + 1 // change code here "this.state.counter + 1"
    });
  }
  render() {
    let expression = Math.random() > .5; // change code here "Math.random() > .5;"
    return (
      <div>
        <button onClick={this.handleClick}>Play Again</button>
        { /* change code below this line */ }
          <Results fiftyFifty={expression} /> //And lastly here!
        { /* change code above this line */ }
        <p>{'Turn: ' + this.state.counter}</p>
      </div>
    );
  }
};
```

This was a VERY hard one, instructions were not very clear I hope this helps someone who is struggling like I was.

**Link(s) to work**

1. continued work on [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react) learning React.js.

**Introduction to the React Challenges**

* PassedUse && for a More Concise Conditional
* PassedUse a Ternary Expression for Conditional Rendering
* PassedRender Conditionally from Props

All code is in GitHub [FCC-Introduction to the React Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/reactjs.txt).


## Day 36: August 29, Wednesday

**Today 's Progress**: I continued work on React.js [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react).

**Thoughts**: Still struggling through the React challenges I did find some examples on google. I endeavor to persevere.

### Resources used:
  * [reactjs.org/docs/getting-started](https://reactjs.org/docs/getting-started.html)

```reactjs
//Use Advanced JavaScript in React Render Method
//An example would have been nice!
const inputStyle = {
  width: 235,
  margin: 5
}
class MagicEightBall extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      userInput: '',
      randomIndex: ''
    }
    this.ask = this.ask.bind(this);
    this.handleChange = this.handleChange.bind(this);
  }
  ask() {
    if (this.state.userInput) {
      this.setState({
        randomIndex: Math.floor(Math.random() * 20),
        userInput: ''
      });
    }
  }
  handleChange(event) {
    this.setState({
      userInput: event.target.value
    });
  }
  render() {
    const possibleAnswers = [
      'It is certain',
      'It is decidedly so',
      'Without a doubt',
      'Yes, definitely',
      'You may rely on it',
      'As I see it, yes',
      'Outlook good',
      'Yes',
      'Signs point to yes',
      'Reply hazy try again',
      'Ask again later',
      'Better not tell you now',
      'Cannot predict now',
      'Concentrate and ask again',
      'Don\'t count on it',
      'My reply is no',
      'My sources say no',
      'Most likely',
      'Outlook not so good',
      'Very doubtful'
    ];
    const answer = possibleAnswers[this.state.randomIndex] // << change code here
    return (
      <div>
        <input
          type="text"
          value={this.state.userInput}
          onChange={this.handleChange}
          style={inputStyle} /><br />
        <button onClick={this.ask}>
          Ask the Magic Eight Ball!
        </button><br />
        <h3>Answer:</h3>
        <p>
          { /* change code below this line */ }
          {answer}
          { /* change code above this line */ }
        </p>
      </div>
    );
  }
};
```

This could be a good example for framework for the random quote machine.

**Link(s) to work**

1. continued work on [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react) learning React.js.

**Introduction to the React Challenges**

* PassedOptimize Re-Renders with shouldComponentUpdate
* PassedIntroducing Inline Styles
* PassedAdd Inline Styles in React
* PassedUse Advanced JavaScript in React Render Method

All code is in GitHub [FCC-Introduction to the React Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/reactjs.txt).


### Day 35: August 28, Tuesday

**Today 's Progress**: I continued work on React.js [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react).

**Thoughts**: Still struggling through the React challenges with no relevant examples. I don't see the benefit to the added complexity at all I am going to hate the projects for this.

### Resources used:
  * [reactjs.org/docs/getting-started](https://reactjs.org/docs/getting-started.html)
  * [CodeSandbox](https://codesandbox.io/?from-app=1)

```reactjs
//Add Event Listeners
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      message: ''
    };
    this.handleEnter = this.handleEnter.bind(this);
    this.handleKeyPress = this.handleKeyPress.bind(this);
  }
  // change code below this line
  componentDidMount() {
    document.addEventListener('keydown', this.handleKeyPress)
  }
  componentWillUnmount() {
     document.removeEventListener('keydown', this.handleKeyPress)
  }
  // change code above this line
  handleEnter() {
    this.setState({
      message: this.state.message + 'You pressed the enter key! '
    });
  }
  handleKeyPress(event) {
    if (event.keyCode === 13) {
      this.handleEnter();
    }
  }
  render() {
    return (
      <div>
        <h3>Input Render:</h3>
        <p>{this.props.input}</p>
        <h1>{this.state.message}</h1>
      </div>
    );
  }
};
```

A few relevant examples would be Awesome. I think I need to find a few good tutorials.

**Link(s) to work**

1. continued work on [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react) learning React.js.

**Introduction to the React Challenges**

* PassedCreate a Controlled Form
* PassedPass State as Props to Child Components
* PassedPass a Callback as Props
* PassedUse the Lifecycle Method componentWillMount
* PassedUse the Lifecycle Method componentDidMount
* PassedAdd Event Listeners
* PassedManage Updates with Lifecycle Methods

All code is in GitHub [FCC-Introduction to the React Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/reactjs.txt).

### Day 34: August 27, monday

**Today 's Progress**: I continued work on React.js [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react).

**Thoughts**: The React challenges have hardly no relevant examples, Would it kill them to put in some relevant examples??? I read the React Docs and tutorials. I just don't see the benefit to the added complexity.

### Resources used:
  * [reactjs.org/docs/getting-started](https://reactjs.org/docs/getting-started.html)
  * [CodeSandbox](https://codesandbox.io/?from-app=1)

```reactjs
//Review Using Props with Stateless Functional Components
//NO GOOD EXAMPLE!!!
class CampSite extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <Camper name='camper' />
      </div>
    );
  }
};
// change code below this line
class Camper extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <p>{this.props.name}</p>
    );
  }
};
Camper.propTypes = {name:PropTypes.string.isRequired};
Camper.defaultProps = { name : 'CamperBot'};
```

A few relevant examples would be nice.

**Link(s) to work**

1. continued work on [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react) learning React.js.

**Introduction to the React Challenges**

* PassedUse PropTypes to Define the Props You Expect
* PassedAccess Props Using this.props
* PassedReview Using Props with Stateless Functional Components
* PassedCreate a Stateful Component
* PassedRender State in the User Interface
* PassedRender State in the User Interface Another Way
* PassedSet State with this.setState
* PassedBind 'this' to a Class Method
* PassedUse State to Toggle an Element
* PassedWrite a Simple Counter
* PassedCreate a Controlled Input

All code is in GitHub [FCC-Introduction to the React Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/reactjs.txt).

![Image of one third](https://static.abcteach.com/free_preview/f/fractions_1third_rgb_p.png)

### Day 33: August 26, Sunday

**Today 's Progress**: I continued work on React.js [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react).

**Thoughts**: Again the React challenges have had very little relevant examples, and I'm not the only one struggling with this because now I see there are a few more students asking for help. I read the React Docs and did a bunch of google searches. I'm pretty sure I don't like React too much. Also the sand box for react is problematic.

### Resources used:
  * [reactjs.org/docs/getting-started](https://reactjs.org/docs/getting-started.html)
  * [repl.it/FCCReactjs](https://repl.it/@JohnJohnson2/FCCReactjs)

```reactjs
//Override Default Props
const Items = (props) => {
  return <h1>Current Quantity of Items in Cart: {props.quantity}</h1>
}
Items.defaultProps = {
  quantity: 0
}
class ShoppingCart extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    { /* change code below this line */ }
    return (
      <Items quantity = {10} />);
    { /* change code above this line */ }
  }
};
```

I'm really sure I don't like react at this point.

**Link(s) to work**

1. continued work on [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react) learning React.js.

**Introduction to the React Challenges**

* PassedWrite a React Component from Scratch
* PassedPass Props to a Stateless Functional Component
* PassedPass an Array as Props
* PassedUse Default Props
* PassedOverride Default Props

All code is in GitHub [FCC-Introduction to the React Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/reactjs.txt).



![Image of reactjs](https://cdn-images-1.medium.com/max/1600/1*ZzZhMpsnsVPaFYLwZ0fs5g.jpeg)

### Day 31: August 24, Friday

**Today 's Progress**: I continued work on React.js [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react).

**Thoughts**: The React challenges for the most part so far have had very little relevant examples, and I guess I'm the only one struggling with this because there are very few students asking for help. I read the React Docs and did a bunch of google searches. I'm pretty sure I don't like React too much.

### Resources used:
  * [reactjs.org/docs/getting-started](https://reactjs.org/docs/getting-started.html)
  * [repl.it/FCCReactjs](https://repl.it/@JohnJohnson2/FCCReactjs)

```reactjs
//Use React to Render Nested Components
const TypesOfFruit = () => {
  return (
    <div>
      <h2>Fruits:</h2>
      <ul>
        <li>Apples</li>
        <li>Blueberries</li>
        <li>Strawberries</li>
        <li>Bananas</li>
      </ul>
    </div>
  );
};
const Fruits = () => {
  return (
    <div>
      { /* change code below this line */ }
      <TypesOfFruit />
      { /* change code above this line */ }
    </div>
  );
};
class TypesOfFood extends React.Component {
  constructor(props) {
    super(props);
  };
  render() {
    return (
      <div>
        <h1>Types of Food:</h1>
        { /* change code below this line */ }
        <Fruits />
        { /* change code above this line */ }
      </div>
    );
  };
};



//Compose React Components
class Fruits extends React.Component {
  constructor(props) {
    super(props);
  };
  render() {
    return (
      <div>
        <h2>Fruits:</h2>
        { /* change code below this line */ }
          <NonCitrus />
          <Citrus />
        { /* change code above this line */ }
      </div>
    );
  }
};
class TypesOfFood extends React.Component {
  constructor(props) {
     super(props);
  };
  render() {
    return (
      <div>
        <h1>Types of Food:</h1>
        { /* change code below this line */ }
          < Fruits />
        { /* change code above this line */ }
        <Vegetables />
      </div>
    );
  };
};



//Render a Class Component to the DOM
class TypesOfFood extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>Types of Food:</h1>
        {/* change code below this line */}
        < Fruits />
        < Vegetables />
        {/* change code above this line */}
      </div>
    );
  }
};
// change code below this line
 ReactDOM.render(<TypesOfFood />, document.getElementById('challenge-node'));
```

I'm pretty sure I don't like react at this point.

**Link(s) to work**

1. continued work on [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react) learning React.js.

**Introduction to the React Challenges**

* PassedRender HTML Elements to the DOM
* PassedDefine an HTML Class in JSX
* PassedLearn About Self-Closing JSX Tags
* PassedCreate a Stateless Functional Component
* PassedCreate a React Component
* PassedCreate a Component with Composition
* PassedUse React to Render Nested Components
* PassedCompose React Components
* PassedRender a Class Component to the DOM

All code is in GitHub and validated at repl.it here: [Repl.it/ Johnny's/ FCCReactjs](https://repl.it/@JohnJohnson2/FCCReactjs) or [FCC-Introduction to the React Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/reactjs.txt).

![Image of reactjs](https://cdn.lynda.com/static/landing/images/hero/React_Developer-1200x630-1503423022468.jpg)

### Day 31: August 24, Friday

**Today 's Progress**: I finished work on [Introduction to the Sass Challenges](https://learn.freecodecamp.org/front-end-libraries/sass) and started on React.js [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react).

**Thoughts**: The [Introduction to the Sass Challenges](https://learn.freecodecamp.org/front-end-libraries/sass) at first seemed pretty buggy but I can confirm it makes a big difference to use Chrome. I used Chrome to get though the last challenges and had no issues.

### Resources used:
  * [Sass (Syntactically Awesome StyleSheets)](http://sass-lang.com/documentation/file.SASS_REFERENCE.html)
  * [Sass Lang Guide](https://sass-lang.com/guide)
  * [Sass Validator](https://www.sassmeister.com/)
  * [reactjs.org/docs/getting-started](https://reactjs.org/docs/getting-started.html)
  * [repl.it/FCCReactjs](https://repl.it/@JohnJohnson2/FCCReactjs)

```reactjs
//Introduction to the React Challenges:
//Create a Simple JSX Element
//JavaScript within curly braces: { 'this is treated as JavaScript code' }
//under the hood the challenges are calling ReactDOM.render(JSX, document.getElementById('root'))
const JSX = <h1>Hello JSX!</h1>;


//Create a Complex JSX Element
const JSX = (<div>
             <h1>Heading One</h1>
             <p>Paragraph Two</p>
             <ul>
               <li>List one</li>
               <li>List Two</li>
               <li>List Three</li>
             </ul>
            </div>);


//Add Comments in JSX
const JSX = (
  <div>
    <h1>This is a block of JSX</h1>
    {/* This is a comment! */}
    <p>Here's a subtitle</p>
  </div>
);
```

This is something new not sure how I feel about it yet.

**Link(s) to work**

1. Finished work on [Introduction to the Sass Challenges](https://learn.freecodecamp.org/front-end-libraries/sass).

**Introduction to the Sass Challenges**

* PassedUse @each to Map Over Items in a List
* PassedApply a Style Until a Condition is Met with @while
* PassedSplit Your Styles into Smaller Chunks with Partials
* PassedExtend One Set of CSS Styles to Another Element

All code is in GitHub and Sass meister here: [Sass meister Johnny's gist](https://www.sassmeister.com/gist/09ea7ae1748eab1f8fa9056705463a77) or [FCC-introductionToTheSassChallenges.sass](https://github.com/Johnny2136/FCC-Projects/blob/Feature/FCC_Challenges/introductionToTheSassChallenges.sass)

2. Started work on [Introduction to the React Challenges](https://learn.freecodecamp.org/front-end-libraries/react) learning React.js.

**Introduction to the React Challenges**

* PassedCreate a Simple JSX Element
* PassedCreate a Complex JSX Element
* PassedAdd Comments in JSX

All code is in GitHub and validated at repl.it here: [Repl.it/ Johnny's/ FCCReactjs](https://repl.it/@JohnJohnson2/FCCReactjs) or [FCC-Introduction to the React Challenge](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/reactjs.txt).


![Image of buggy code](https://imgs.xkcd.com/comics/code_quality_3.png)

### Day 30: August 23, Thursday

**Today 's Progress**: I started work on [Introduction to the Sass Challenges](https://learn.freecodecamp.org/front-end-libraries/sass) I had completed a couple sections previously those were:
* [Introduction to the Bootstrap Challenges](https://learn.freecodecamp.org/front-end-libraries/bootstrap)
* [Introduction to jQuery](https://learn.freecodecamp.org/front-end-libraries/jquery)

**Thoughts**: The [Introduction to the Sass Challenges](https://learn.freecodecamp.org/front-end-libraries/sass) seem pretty buggy it makes a big difference to use Chrome. Firefox should work but in the last challenge I did I knew the code was correct based on [Sass Validator](https://www.sassmeister.com/) results, but the unit tests failed, so I tried the same code in chrome and it passed I'm not sure what the issue was.

### Resources used:
  * [Sass (Syntactically Awesome StyleSheets)](http://sass-lang.com/documentation/file.SASS_REFERENCE.html)
  * [Sass Lang Guide](https://sass-lang.com/guide)
  * [Sass Validator](https://www.sassmeister.com/)

```html
#Use @for to Create a Sass Loop(Passes in Chrome)
<style type='text/sass'>
  @for $j from 1 to 6 {
    .text-#{$j} {font-size: 10px * $j; }
   }  
</style>

<p class="text-1">Hello</p>
<p class="text-2">Hello</p>
<p class="text-3">Hello</p>
<p class="text-4">Hello</p>
<p class="text-5">Hello</p>
```
To make it pass in Firefox... use:
```html
#Use @for to Create a Sass Loop(Passes in Firefox)
<style type='text/sass'>
  @for $j from 1 to 6 {
    .text-#{$j} {font-size: 10px * $j; }
   }  
</style>

<p class="text-1" style="font-size:10px;">Hello</p>
<p class="text-2" style="font-size:20px;">Hello</p>
<p class="text-3" style="font-size:30px;">Hello</p>
<p class="text-4" style="font-size:40px;">Hello</p>
<p class="text-5" style="font-size:50px;">Hello</p>
```
This also was a frustrating challenge I worked pretty hard getting the tests to pass. Took changing browsers (I did find a way to get the tests to pass in Firefox by adding style to P tags).

**Link(s) to work**

1. Started work on [Introduction to the Sass Challenges](https://learn.freecodecamp.org/front-end-libraries/sass).

**Introduction to the Sass Challenges**

* PassedStore Data with Sass Variables
* PassedNest CSS with Sass
* PassedCreate Reusable CSS with Mixins
* PassedUse `@if` and `@else` to Add Logic To Your Styles
* PassedUse `@for` to Create a Sass Loop

All code is in GitHub and repl.it here: [Sass meister Johnny's gist](https://www.sassmeister.com/gist/09ea7ae1748eab1f8fa9056705463a77) or [FCC-introductionToTheSassChallenges.sass](https://github.com/Johnny2136/FCC-Projects/blob/Feature/FCC_Challenges/introductionToTheSassChallenges.sass

![Image of Certification](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_JS_Projects/JS_Certification.png)

### Day 29: August 22, Wednesday

**Today 's Progress**: I Finnished work on [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Thoughts**: Today focused on completing the Cash Register challenge. This is all about combining lessons learned in previous challenges the code is located here: [FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_JS_Projects/cashRegister.js).

After examining the requirements I made the following user story, As a user I want to: pass arguments to a cash register drawer function checkCashRegister() that accepts purchase price as the first argument (price), payment as the second argument (cash), and cash-in-drawer (cid) as the third argument. The checkCashRegister() function should always return an object with a status key and a change key.

**Other notes**
* cid is a 2D array listing available currency.
* Return {status: "INSUFFICIENT_FUNDS", change: []} if cash-in-drawer is less than the change due, or if you cannot return the exact change.
* Return {status: "CLOSED", change: [...]} with cash-in-drawer as the value for the key change if it is equal to the change due.
* Otherwise, return {status: "OPEN", change: [...]}, with the change due in coins and bills, sorted in highest to lowest order, as the value of the change key.

  * [JS Array Reduce](https://forum.freecodecamp.org/t/javascript-array-prototype-reduce/14299)
  * [JS Reduce Made Easy](https://forum.freecodecamp.org/t/using-array-prototype-reduce-to-reduce-conceptual-boilerplate-for-problems-on-arrays/14687)
  * [JS Loops](https://forum.freecodecamp.org/t/javascript-loops/14681)
  * [JS Array Push](https://forum.freecodecamp.org/t/javascript-array-prototype-push/14298)

```javascript
/***************************************************************
 * JavaScript Algorithms and Data Structures Projects:         *
 * Cash Register, JJ 2018                                      *
 * https://repl.it/@JohnJohnson2/FCCProject-cashRegisterjs     *
 ***************************************************************/
//My solution
// Create myArr Array of objects which hold the monitary values (the challenge forgot about fifty-cent(HALF-DOLLAR) pieces which are fairly common)
const myArr = [
  { id: 'ONE HUNDRED', val: 100.00},
  { id: 'TWENTY', val: 20.00},
  { id: 'TEN', val: 10.00},
  { id: 'FIVE', val: 5.00},
  { id: 'ONE', val: 1.00},// could be bill or coin.
  { id: 'HALF-DOLLAR', val:0.50},//coin should be added.
  { id: 'QUARTER', val: 0.25},
  { id: 'DIME', val: 0.10},
  { id: 'NICKEL', val: 0.05},
  { id: 'PENNY', val: 0.01}
];
function checkCashRegister(price, cash, cid) {
  //Use .reduce to transform CID array into  register drawer (regDrw).
  let regDrw = cid.reduce(function(acc, curr) {
    acc.total += curr[1];
    acc[curr[0]] = curr[1];
    //console.log(acc);//debugging
    return acc;
  }, { total: 0 });
  // Handle exact change
  let messageArr = { status: null, change: [] };// 2d message arr.
  let change = cash - price;
  if (regDrw.total === change) {
    messageArr.status = 'CLOSED';
    messageArr.change = cid;
    console.log(messageArr);//debugging
    return messageArr;
  };
  // Handle insufficient funds
  if (regDrw.total < change) {
    messageArr.status = 'INSUFFICIENT_FUNDS';
    console.log(messageArr)//debugging
    return messageArr;
  };
  // Loop through the monitary amounts myArray
  var change_arr = myArr.reduce(function(acc, curr) {
    var value = 0;
    // need to refactor this...
    while (regDrw[curr.id] > 0 && change >= curr.val) {// While money is in the drawer
    // And while the id: value: is larger than the change in drawer
      change -= curr.val;
      regDrw[curr.id] -= curr.val;
      value += curr.val;
      // Round change to the nearest hundreth 'PENNY'.
      change = Math.round(change * 100) / 100;
    };
    // Add this currency id to the messageArr only if any was used.
    if (value > 0) {
        acc.push([ curr.id, value ]);
    };
    return acc; // Return the current pushed acc
  }, []); // Empty array for .reduce
  // If no elements in change_arr or leftover change, return "Insufficient Funds"
  if (change_arr.length < 1 || change > 0) {
    messageArr.status = 'INSUFFICIENT_FUNDS';
    console.log(messageArr);//debugging
    return messageArr;
  };
  // Here is your change, ma'am.
  messageArr.status = 'OPEN';
  messageArr.change = change_arr;
  console.log(messageArr);//debugging
  return messageArr;
};
// test here (the first one I wrote to test for 1/2 Dollar Coins)
checkCashRegister(19.25, 70.00, [["PENNY", 1.01], ["NICKEL", 2.05], ["DIME", 3.10], ["QUARTER", .25], ["HALF-DOLLAR", 4.00], ["ONE", 0.00], ["FIVE", 5.00], ["TEN", 20.00], ["TWENTY", 40.00], ["ONE HUNDRED", 100.00]]);//Wrote my own test for 1/2 dollar coin should return { status: 'OPEN', change: [[ 'HALF-DOLLAR', 0.5 ] ] }.
checkCashRegister(19.5, 20, [["PENNY", 1.01], ["NICKEL", 2.05], ["DIME", 3.1], ["QUARTER", 4.25], ["ONE", 90], ["FIVE", 55], ["TEN", 20], ["TWENTY", 60], ["ONE HUNDRED", 100]]); //should return {status: "OPEN", change: [["QUARTER", 0.5]]}.
checkCashRegister(3.26, 100, [["PENNY", 1.01], ["NICKEL", 2.05], ["DIME", 3.1], ["QUARTER", 4.25], ["ONE", 90], ["FIVE", 55], ["TEN", 20], ["TWENTY", 60], ["ONE HUNDRED", 100]]); //should return {status: "OPEN", change: [["TWENTY", 60], ["TEN", 20], ["FIVE", 15], ["ONE", 1], ["QUARTER", 0.5], ["DIME", 0.2], ["PENNY", 0.04]]}.
checkCashRegister(19.5, 20, [["PENNY", 0.01], ["NICKEL", 0], ["DIME", 0], ["QUARTER", 0], ["ONE", 0], ["FIVE", 0], ["TEN", 0], ["TWENTY", 0], ["ONE HUNDRED", 0]]); //should return {status: "INSUFFICIENT_FUNDS", change: []}.
checkCashRegister(19.5, 20, [["PENNY", 0.01], ["NICKEL", 0], ["DIME", 0], ["QUARTER", 0], ["ONE", 1], ["FIVE", 0], ["TEN", 0], ["TWENTY", 0], ["ONE HUNDRED", 0]]); //should return {status: "INSUFFICIENT_FUNDS", change: []}.
checkCashRegister(19.5, 20, [["PENNY", 0.5], ["NICKEL", 0], ["DIME", 0], ["QUARTER", 0], ["ONE", 0], ["FIVE", 0], ["TEN", 0], ["TWENTY", 0], ["ONE HUNDRED", 0]]); //should return {status: "CLOSED", change: [["PENNY", 0.5], ["NICKEL", 0], ["DIME", 0], ["QUARTER", 0], ["ONE", 0], ["FIVE", 0], ["TEN", 0], ["TWENTY", 0], ["ONE HUNDRED", 0]]
```
This also was a very hard challenge I worked pretty hard getting one of the tests to pass (I forgot an if statement) and had to work a couple hours to get the tests to pass, Like the other one I actually started working on it yesterday and finally finished today.

**Link(s) to work**

1. finished Projects [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Introduction to the Functional Programming Challenges**

* PassedCash Register

All code is in GitHub and repl.it here: [repl.it FCCProjectcashRegisterjs](https://repl.it/@JohnJohnson2/FCCProject-cashRegisterjs) or [FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_JS_Projects)

### Day 28: August 21, Tuesday

**Today 's Progress**: I continue work on [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Thoughts**: Today focused on the Telephone Number Validator challenge This is all about RegEx to pass This project. The telephoneNumberValidator.js is located here:[FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_JS_Projects/telephoneNumberValidator.js).

After examining the requirements I made the following user story, As a user I want to: pass a number to a function that returns true if the passed string looks like a valid US phone number.

For example: For this challenge you will be presented with a string such as 800-692-7753 or 8oo-six427676;laskdjf. Your job is to validate or reject the US phone number based on any combination of the formats provided above. The area code is required. If the country code is provided, you must confirm that the country code is 1. Return true if the string is a valid US phone number; otherwise return false.
* Sample validation data was provided.
* [RegExp](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp),
* [regexpal.com](https://www.regexpal.com/index.php),
* [regex101.com](https://regex101.com/r/h2HCMZ/1/)

```javascript
/***********************************************************************
 * JavaScript Algorithms and Data Structures Projects:                 *
 * Telephone Number Validator, JJ 2018                                 *
 * https://repl.it/@JohnJohnson2/FCCProjectTelephoneNumberValidatorjs  *
 ***********************************************************************/
//My solution
function telephoneCheck(str) {
  // Good luck!
  //RegExp was validated here: https://regex101.com/r/h2HCMZ/1/
 var phoNum = /^(1\s?)?(\(\d{3}\)|\d{3})[\s\-]?\d{3}[\s\-]?\d{4}$/;
 console.log(phoNum.test(str));
 return phoNum.test(str);
};
//Tests Here:
telephoneCheck("555-555-5555");// should return a boolean.
telephoneCheck("1 555-555-5555");// should return true.
telephoneCheck("1 (555) 555-5555");// should return true.
telephoneCheck("5555555555");// should return true.
telephoneCheck("555-555-5555");// should return true.
telephoneCheck("(555)555-5555");// should return true.
telephoneCheck("1(555)555-5555");// should return true.
telephoneCheck("555-5555");// should return false.
telephoneCheck("5555555");// should return false.
telephoneCheck("1 555)555-5555");// should return false.
telephoneCheck("1 555 555 5555");// should return true.
telephoneCheck("1 456 789 4444");// should return true.
telephoneCheck("123**&!!asdf#");// should return false.
telephoneCheck("55555555");// should return false.
telephoneCheck("(6054756961)");// should return false
telephoneCheck("2 (757) 622-7382");// should return false.
telephoneCheck("0 (757) 622-7382");// should return false.
telephoneCheck("-1 (757) 622-7382");// should return false
telephoneCheck("2 757 622-7382");// should return false.
telephoneCheck("10 (757) 622-7382");// should return false.
telephoneCheck("27576227382");// should return false.
telephoneCheck("(275)76227382");// should return false.
telephoneCheck("2(757)6227382");// should return false.
telephoneCheck("2(757)622-7382");// should return false.
telephoneCheck("555)-555-5555");// should return false.
telephoneCheck("(555-555-5555");// should return false.
telephoneCheck("(555)5(55?)-5555");// should return false.
```
This also was not too hard but validating the regexp to get the tests to pass took a lot of time I actually started working on it yesterday.

**Link(s) to work**

1. Work on Projects [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Introduction to the Functional Programming Challenges**

* PassedTelephone Number Validator

All code is in GitHub and repl.it here: [repl.it FCCProjectTelephoneNumberValidator.js](https://repl.it/@JohnJohnson2/FCCProjectTelephoneNumberValidatorjs) or [FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_JS_Projects)

### Day 27: August 20, Monday

**Today 's Progress**: I continue work on [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Thoughts**: Today focused on trying to define the challenge Caesar Cipher (or ROT13) and meet the requirements to pass This project. CaesarCipher.js is located here:[FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_JS_Projects).

After examining the requirements I made the following user story, As a user I want to: enter a ROT13 encoded string as input to a function which will returns a decoded plain text string. also:
* All letters will be uppercase.
* Do not transform any non-alphabetic character (i.e. spaces, punctuation), but be sure to pass them on in the result. I used the following:
* [String.prototype.replace()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace),
* [String.fromCharCode()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/fromCharCode),
* [ternary operator](https://www.w3schools.com/js/js_operators.asp)

```javascript
console.log("Caesars Cipher")
//Write a function which takes a ROT13 encoded string as input and returns a decoded string.
/***************************************************************
 * JavaScript Algorithms and Data Structures Projects:         *
 * CaesarsCipher, JJ 2018                                      *
 * https://repl.it/@JohnJohnson2/FCCProjectCaesarsCipher       *
 ***************************************************************/
//My solution
function rot13(str) { // LBH QVQ VG!
  let myStr = "";
  console.log(str + "");//Debugging str contents
  console.log((str + "").replace(/[A-Z]/gi, function (myStr) { return String.fromCharCode(myStr.charCodeAt(0) + (myStr.toLowerCase() < "n" ? 13 : -13));}));//Debugging conversion routine, should decode in ROT 13 or encode if plain text
  return (str + "").replace(/[A-Z]/gi, function (myStr) {
    return String.fromCharCode(myStr.charCodeAt(0) + (myStr.toLowerCase() < "n" ? 13 : -13));
  });
};
// Change the inputs below to test
rot13("SERR PBQR PNZC");
rot13("My Test");
```
This was not too hard but I did have some minor code problems that caused a couple refactoring of the code get the tests to pass. Then I wasn't happy and wanted to use ternary operator `?` and `.replace`.

**Link(s) to work**

1. Work on Projects [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Introduction to the Functional Programming Challenges**

* PassedCaesars Cipher

All code is in GitHub and repl.it here: [repl.it FCCProjectCaesarsCipher](https://repl.it/@JohnJohnson2/FCCProjectCaesarsCipher) or [FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_JS_Projects)


### Day 26: August 19, Sunday

**Today 's Progress**: I Started work on [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Thoughts**: I focused on trying to define the challenge and fully understand the requirements to pass these projects. This isn't like the other challenges as these are for the certification.  I made a place in the FCC-Projects repo on GitHub here in [FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_JS_Projects) to store my projects. I had previously did the first project so moved on to the second today. my goal is to complete one a day but some may take longer.

After examining the requirements I made the following user story, As a user I want to: convert the given number into a roman numeral, and all roman numerals answers should be upper-case. I used the following:
* [Modulus (Division Remainder)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators)
* [Array.lengthr](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length),
* [Assignment operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Assignment_Operators)
* [Converting Decimal Number lying between 1 to 3999 to Roman Numerals](https://www.geeksforgeeks.org/converting-decimal-number-lying-between-1-to-3999-to-roman-numerals/),

```javascript
console.log("Roman Numeral Converter")
//Convert the given number into a roman numeral. All roman numerals answers should be provided in upper-case.
 /**************************************************************
 * JavaScript Algorithms and Data Structures Projects:         *
 * Roman Numeral Converter, JJ 2018                            *
 * https://jsfiddle.net/johnny2136/8m6937xd/20/                *
 ***************************************************************/
function convertToRoman(num) {
  //Make 2 arrays.
  const decArr = [1000, 900, 500, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1];
  const romArr = ["M", "CM","D","CD","C", "XC", "L", "XL", "X","IX","V","IV","I"];
  //Variable for solution.
  let romNum = "";// Be carfull not to accidentally add whitespace
  //While loop inside a for to convert the Number to Roman number
  //console.log("Number: " + num);//Debugging
  for (let i = 0; i <= decArr.length; i++) {     
    while (num % decArr[i] < num) {
      //console.log(num);//Debugging
      romNum += romArr[i];       
      num -= decArr[i];
      //console.log(romNum);//Debugging
      //console.log(num);//Debugging
    };
  };
  console.log(romNum);
  return romNum;
};
//Unit tests:
convertToRoman(36);//should return "XXXVI"
convertToRoman(2); //should return "II".
convertToRoman(3); //should return "III".
convertToRoman(4); //should return "IV".
convertToRoman(5); //should return "V".
convertToRoman(9); //should return "IX".
convertToRoman(12); //should return "XII".
convertToRoman(16); //should return "XVI".
convertToRoman(29); //should return "XXIX".
convertToRoman(44); //should return "XLIV".
convertToRoman(45); //should return "XLV"
convertToRoman(68); //should return "LXVIII"
convertToRoman(83); //should return "LXXXIII"
convertToRoman(97); //should return "XCVII"
convertToRoman(99); //should return "XCIX"
convertToRoman(400); //should return "CD"
convertToRoman(500); //should return "D"
convertToRoman(501); //should return "DI"
convertToRoman(649); //should return "DCXLIX"
convertToRoman(798); //should return "DCCXCVIII"
convertToRoman(891); //should return "DCCCXCI"
convertToRoman(1000); //should return "M"
convertToRoman(1004); //should return "MIV"
convertToRoman(1006); //should return "MVI"
convertToRoman(1023); //should return "MXXIII"
convertToRoman(2014); //should return "MMXIV"
convertToRoman(3999); //should return "MMMCMXCIX"
```
This was pretty straight forward but I did have some minor code problems that caused hours of debugging to get the tests to pass.

**Link(s) to work**

1. Work on Projects [Introduction to the JavaScript Algorithms and Data Structures Projects](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects).

**Introduction to the Functional Programming Challenges**

* PassedPalindrome Checker
* PassedRoman Numeral Converter

All code is in GitHub and repl.it here: [repl.it FCC_Projects_RomanNumeralConverter.js](https://repl.it/@JohnJohnson2/FCCProjects-RomanNumeralConverterjs) or [FCC-Projects/FCC_JS_Projects](https://github.com/Johnny2136/FCC-Projects/tree/master/FCC_JS_Projects)


## Day 25: August 18, Saturday

**Today 's Progress**: I completed work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: I focused on trying to understand the algorithm process and writing code. The Algorithms today were very complex, I once again had to rely on hints. I used the following resources in developing my solutions.

After searching and studying, I learned something new from the following:
* [Object.prototype.hasOwnProperty()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/hasOwnProperty)
* [Conditional (ternary) Operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator),
* [Wikipedia Orbital Period](https://en.wikipedia.org/wiki/Orbital_period)
* [javascript-splice-vs-slice](http://www.tothenew.com/blog/javascript-splice-vs-slice/),

```javascript
console.log("Map the Debris");
//Return a new array that transforms the elements' average altitude into their orbital periods (in seconds). The array will contain objects in the format {name: 'name', avgAlt: avgAlt}. You can read about orbital periods on [Wikipedia](https://en.wikipedia.org/wiki/Orbital_period). The values should be rounded to the nearest whole number. The body being orbited is Earth. The radius of the earth is 6367.4447 kilometers, and the GM value of earth is 398600.4418 km3s-2.
function orbitalPeriod(arr) {
  const GM = 398600.4418;
  const earthRadius = 6367.4447;
  let a = 2 * Math.PI;
  let myArr = [];
  let getOrbPeriod = function(obj) {
    let c = Math.pow(earthRadius + obj.avgAlt, 3);
    let b = Math.sqrt(c / GM);
    let orbPeriod = Math.round(a * b);
    delete obj.avgAlt;
    obj.orbitalPeriod = orbPeriod;
    return obj;
  };
  for (var element in arr) {
    myArr.push(getOrbPeriod(arr[element]));
  }
  console.log(myArr);
  return myArr;
};
// test here
orbitalPeriod([{name : "sputnik", avgAlt : 35873.5553}]);
console.log("<----------------------next exercise------------------------->");
```
Once more I had to rely heavily on the hints when my first attempts failed. also [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference) I can't say enough about this reference!

**Link(s) to work**

1. Finished [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedEverything Be True
* PassedArguments Optional
* PassedMake a Person
* PassedMap the Debris

All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)

### Day 24: August 17, Friday

**Today 's Progress**: I continue work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: After a very long week I am finally able to relax a bit I took today off so I could focus on resting and writing code. So the Algorithms today were a mixed bag, some easier than others. I used the following resources in developing my solutions.

After searching and studying, I learned something new from the following:
* [String.fromCharCode()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/fromCharCode)
* [String.prototype.split()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)
* [Array.prototype.findIndex()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex),
* [Conditional (ternary) Operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator),
* [JavaScript Operators](https://www.w3schools.com/js/js_operators.asp)
* [javascript-splice-vs-slice](http://www.tothenew.com/blog/javascript-splice-vs-slice/),

```javascript
console.log("Drop it");
//Given the array arr, iterate through and remove each element starting from the first element (the 0 index) until the function func returns true when the iterated element is passed through it. Then return the rest of the array once the condition is satisfied, otherwise, arr should be returned as an empty array.
//Resources to solve this: [Array.prototype.findIndex()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex), [Conditional (ternary) Operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator), [JavaScript Operators](https://www.w3schools.com/js/js_operators.asp), [javascript-splice-vs-slice](http://www.tothenew.com/blog/javascript-splice-vs-slice/),
function dropElements(arr, func) {
  console.log(arr.slice(arr.findIndex(func) >= 0
    ? arr.findIndex(func): arr.length, arr.length));//Used for debugging
  return arr.slice(arr.findIndex(func) >= 0
    ? arr.findIndex(func): arr.length, arr.length);
};
// test here
dropElements([1, 2, 3, 4], function(n) {return n >= 3;});
console.log("<----------------------next exercise------------------------->");

console.log("Steamroller");
//Flatten a nested array. You must account for varying levels of nesting.
function steamrollArray(arr) {
  let myArr = [].concat(...arr);
  console.log(myArr);//Debugging
  //console.log(myArr.some(Array.isArray) ? steamrollArray(myArr) : myArr);//Debugging
  return myArr.some(Array.isArray)
    ? steamrollArray(myArr) : myArr;
   //console.log(myArr); //Debugging
};
// test here
steamrollArray([[["a"]], [["b"]]]);// should return ["a", "b"].
steamrollArray([1, [2], [3, [[4]]]]);// should return [1, 2, 3, 4].
steamrollArray([1, [], [3, [[4]]]]);// should return [1, 3, 4].
steamrollArray([1, {}, [3, [[4]]]]);// should return [1, {}, 3, 4].
console.log("<----------------------next exercise------------------------->");
```
I still find myself having to rely heavily on the hints and [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference) I can't say enough about this reference!

**Link(s) to work**

1. Continuing [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedDrop it
* PassedSteamroller
* PassedBinary Agents

All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)


### Day 23: August 16, Thursday

**Today 's Progress**: I continue work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: Another long day and long commute, barely got through one challenge.

```javascript
console.log("Smallest Common Multiple");
//Find the smallest common multiple of the provided parameters that can be evenly divided by both, as well as by all sequential numbers in the range between these parameters. The range will be an array of two numbers that will not necessarily be in numerical order. For example, if given 1 and 3, find the smallest common multiple of both 1 and 3 that is also evenly divisible by all numbers between 1 and 3. The answer here would be 6.
function smallestCommons(arr) {
let max = Math.max(arr[0],arr[1]);
let min = Math.min(arr[0],arr[1]);
//console.log(max + " & " + min);//Debugging

  function smallComMulti(a, b){ //find smallest Common Multiple
    for(var i = 1; i <= b; i++){     
      if((i * a) % b === 0){
        //console.log(i * a);//Debugging
        return (i * a);
      }
    }   
  };    
  let myNum = smallComMulti(max, min);
  for(var ii = min + 1; ii < max; ii++) {    
    myNum = smallComMulti(myNum, ii);   
  }
  console.log(myNum);
  return myNum;
};
// test here
smallestCommons([1,5]);
console.log("<----------------------next exercise------------------------->");
```
I had to rely on the hints and [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference).

**Link(s) to work**

1. Started [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedSmallest Common Multiple

All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)


### Day 22: August 15, Wednesday

**Today 's Progress**: I continue work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: Another long day and longer commute, barely got through two challenges.

```javascript
console.log("Sum All Primes");
//Sum all the prime numbers up to and including the provided number. A prime number is defined as a number greater than one and having only two divisors, one and itself. For example, 2 is a prime number because it's only divisible by one and two. The provided number may not be a prime.
function sumPrimes(num) {
  function myPrime(number){
      for (let i = 2; i <= number; i++){
          if(number % i === 0 && number!= i){
             return false;
          }
       }
    return true;
  };
  if (num === 1){
    return 0;
  };
  if(myPrime(num) === false){
    return sumPrimes(num - 1);
  };
  // Check if your number is prime
  if(myPrime(num) === true){
    return num + sumPrimes(num - 1);
  }
};
// test here
console.log(sumPrimes(10));
console.log("<----------------------next exercise------------------------->");
```
I had to rely on the hints to get this.

**Link(s) to work**

1. Started [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedSum All Odd Fibonacci Numbers
* PassedSum All Primes
All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)


### Day 21: August 14, Tuesday

**Today 's Progress**: I continue work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: Don't have much time tonight, only worked through two challenges. I started a third but didn't finish it.

```javascript
console.log("Convert HTML Entities");
//Convert the characters &, <, >, " (double quote), and ' (apostrophe), in a string to their corresponding HTML entities. (You got to be kidding me!!!)
 function convertHTML(str) {
      const htmlEnt={
        '&':'&amp;',
        '<':'&lt;',
        '>':'&gt;',
        '\"':'&quot;',
        '\'':"&apos;"
      };
  return str.split('').map(function(ojbect){//Use Split and map function to filter str.
        return htmlEnt[ojbect] || ojbect;
      }).join('');//Use .join prototype
  };  
//test here
console.log(convertHTML("Dolce & Gabbana")); //should return Dolce &​amp; Gabbana.
console.log(convertHTML("Hamburgers < Pizza < Tacos")); //should return Hamburgers &​lt; Pizza &​lt; Tacos.
console.log(convertHTML("Sixty > twelve")); //should return Sixty &​gt; twelve.
console.log(convertHTML('Stuff in "quotation marks"')); //should return Stuff in &​quot;quotation marks&​quot;.
console.log(convertHTML("Schindler's List")); //should return Schindler&​apos;s List.
console.log(convertHTML("<>")); //should return &​lt;&​gt;.
console.log(convertHTML("abc")); //should return abc.
console.log("<----------------------next exercise------------------------->");
```
This one used elements from previous Challenges.

**Link(s) to work**

1. Started [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedSorted Union
* PassedConvert HTML Entities
All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)

## Day 20: August 13, Monday

**Today 's Progress**: I continue work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: I need to find out why its so hard to do these Challenges, again today I spent hours trying to get something I thought should work to actually work. I used to think I was pretty good at coming up with logical algorithms for solving problems but I am really struggling nothing seems to work, maybe there are too many options `for` vice `map` and the concept of `callbacks` is hard for me to grasp, I will keep trying, maybe it will get easier with practice.

```javascript
console.log("Pig Latin");
//Translate the provided string to pig latin. Pig Latin takes the first consonant (or consonant cluster) of an English word, moves it to the end of the word and suffixes an "ay". If a word begins with a vowel you just add "way" to the end. Input strings are guaranteed to be English words in all lowercase.
function translatePigLatin(str) {
  var pigLatin = '';
  var RegExp = /[aeiou]/gi;
  if (str[0].match(RegExp)) {
    pigLatin = str + 'way';
    //console.log('Test 1st letter is a aeiou');
  } else if(str.match(RegExp) === null) {//added to get last test to pass.
    pigLatin = str + 'ay';
    //console.log('Test there are only consonants');
  } else {
    var vowelIndex = str.indexOf(str.match(RegExp)[0]);
    //console.log(vowelIndex = str.indexOf(str.match(RegExp)[0]));
    pigLatin = str.substr(vowelIndex) + str.substr(0, vowelIndex) + 'ay';
  }  
  console.log(pigLatin);
  return pigLatin;
}
translatePigLatin("consonant");// should return "onsonantcay
translatePigLatin("california");// should return "aliforniacay".
translatePigLatin("paragraphs");// should return "aragraphspay".
translatePigLatin("glove");// should return "oveglay".
translatePigLatin("algorithm");// should return "algorithmway".
translatePigLatin("eight");// should return "eightway".
translatePigLatin("myclm");// should return "eightway".
translatePigLatin("shmmnd");// should return "eightway".
console.log("<----------------------next exercise------------------------->");
```
This one seemed at first pretty straight forward but I couldn't get the last test to pass. I finally looked at the hints and saw I wasn't checking for consonants, I finally got it to work... [String.prototype.match()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/match), [w3schools.com](https://www.w3schools.com/js/js_regexp.asp) and [Regular Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions).

**Link(s) to work**

1. Started [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedPig Latin
* PassedSearch and Replace
* PassedDNA Pairing
* PassedMissing letters

All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)


### Day 19: August 12, Sunday

**Today 's Progress**: I continue work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: One word AAAAARRRRRRRRRGGGGHHHH!!!!! These are maddening even the solutions I looked up when I was struggling didn't work:

```javascript
console.log("Spinal Tap Case");
//Convert a string to spinal case. Spinal case is all-lowercase-words-joined-by-dashes.
function spinalCase(str) {
  // Replace low-upper case to low-space-uppercase
  str = str.replace(/([a-z])([A-Z])/g, '$1 $2');
  // Split on whitespace and underscores and join with dash
  console.log(str.toLowerCase().split(/(?:_| )+/) .join('-'));
  return str.toLowerCase().split(/(?:_| )+/) .join('-');
}
// Unit test:
spinalCase("This Is Spinal Tap");// should return "this-is-spinal-tap".
spinalCase("thisIsSpinalTap");// should return "this-is-spinal-tap".
spinalCase("The_Andy_Griffith_Show");// should return "the-andy-griffith-show".
spinalCase("Teletubbies say Eh-oh");// should return "teletubbies-say-eh-oh".
spinalCase("AllThe-small Things");// should return "all-the-small-things".
console.log("<----------------------next exercise------------------------->");
```
This one hours finally I gave up and searched for a solution and even that needed altering to get it to work... [String.prototype.replace()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace)

**Link(s) to work**

1. Started [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedWherefore art thou
* PassedSpinal Tap Case

All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)


### Day 18: August 11, Saturday

**Today 's Progress**: I started work [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Thoughts**: These algorithm challenges are just as hard as the other algorithm challenge I took the approach of visualizing the requirements and array sets then walking though the JS steps. For example:

```javascript
console.log("Seek and Destroy");
//You will be provided with an initial array (the first argument in the destroyer function), followed by one or more arguments. Remove all elements from the initial array that are of the same value as these arguments. Note: You have to use the arguments object.
function destroyer(arr, a1, a2) {
  // Remove all the values
  console.log("Initial Array -->  " + arguments[0]);//Array argument 0  
  var args = Array.from(arguments).slice(1);
  console.log("Filter argument -->  " + (args = Array.from(arguments).slice(1)));//eval arguments
    return arr.filter(function(val) {
      return !args.includes(val);
    });
  return arr;
}
console.log(destroyer([1, 2, 3, 1, 2, 3], 2, 3)); //should return [1, 1].
console.log(destroyer([1, 2, 3, 5, 1, 2, 3], 2, 3)); //should return [1, 5, 1].
console.log(destroyer([3, 5, 1, 2, 2], 2, 3, 5)); //should return [1].
console.log(destroyer([2, 3, 2, 3], 2, 3)); //should return [].
console.log(destroyer(["tree", "hamburger", 53], "tree", 53)); //should return ["hamburger"].
console.log(destroyer(["possum", "trollo", 12, "safari", "hotdog", 92, 65, "grandma", "bugati", "trojan", "yacht"], "yacht", "possum", "trollo", "safari", "hotdog", "grandma", "bugati", "trojan")); //should return [12,92,65].
console.log("<----------------------next exercise------------------------->");
```
This one took some google searching and trying to figure out how to get `Array.from(arguments).slice` to work in my solution... [Arguments object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments)

**Link(s) to work**

1. Started [Intermediate Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting).

**Introduction to the Functional Programming Challenges**

* PassedSum All Numbers in a Range
* PassedDiff Two Arrays
* PassedSeek and Destroy

All code is in GitHub and repl.it here: [repl.it IntermediateAlgorithmScripting.js](https://repl.it/@JohnJohnson2/IntermediateAlgorithmScriptingjs) or [GitHub IntermediateAlgorithmScripting.js](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntermediateAlgorithmScripting.js)

### Day 17: August 10, Friday

**Today 's Progress**: I finished work [Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Thoughts**: Some of these Challenges continue to be pretty hard while others very simple, I am dealing with the aggravating ones as well as the easy ones.

For example an easy one:
```javascript
//Introduction to Currying and Partial Application
//Fill in the body of the add function so it uses currying to add parameters x, y, and z.
function add(x) {
  // Add your code below this line
    return function(y) {
      return function(z) {
        return x + y + z;
      }
    }  
  // Add your code above this line
}
console.log(add(10)(20)(30));//should return 60.
console.log(add(1)(2)(3)); //should return 6.
console.log(add(11)(22)(33)); //should return 66.
//Your code should include a final statement that returns x + y + z.
console.log("-------------------Next------------------------");
```
And a Aggravating one:
```JavaScript
//Apply Functional Programming to Convert Strings to URL Slugs
//Fill in the urlSlug function so it converts a string title and returns the hyphenated version for the URL. You can use any of the methods covered in this section, and don't use replace. Here are the requirements:
//The input is a string with spaces and title-cased words
//The output is a string with the spaces between words replaced by a hyphen (-)
//The output should be all lower-cased letters
//The output should not have any spaces
// the global variable
var globalTitle = "Winter Is Coming";
// Add your code below this line
function urlSlug(title) {
console.log("First --> "+ title);//DEbugging
var myTitle = title.split(/\W+/); //from previous excersize
console.log("Second  --> "+ myTitle);//DEbugging
var filterTitle = myTitle.filter(function(obj){// my solution-Mozilla.org
return /\S/.test(obj);// Mozilla.org
});
console.log("Third  --> "+ filterTitle.join("-").toLowerCase());//DEbugging
console.log("Finally Global  --> "+ globalTitle);//DEbugging
return filterTitle.join("-").toLowerCase();// StackOverflow!!!
};// ARRRGGGGGHHH!!!!! This was hard!!!!!
// Add your code above this line
var winterComing = urlSlug(globalTitle); // Should be "winter-is-coming"
//Additional tests....
urlSlug("A Mind Needs Books Like A Sword Needs A Whetstone");// should return "a-mind-needs-books-like-a-sword-needs-a-whetstone".
urlSlug("Hold The Door");// should return "hold-the-door".(https://stackoverflow.com/questions/6442327/using-split-join-to-replace-a-string-with-a-array)
//this challange sort of sucked!!! Took me a long time :(
//This helped https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/test
//and this https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter
console.log("-------------------Next------------------------");
```
This one took a few google searched and trying to figure out `split, filter, join` work togather... [StackOverflow.com]((https://stackoverflow.com/questions/6442327/using-split-join-to-replace-a-string-with-a-array))

**Link(s) to work**

1. Continued [Introduction to Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Introduction to the Functional Programming Challenges**

* PassedReturn a Sorted Array Without Changing the Original Array
* PassedSplit a String into an Array Using the split Method
* PassedCombine an Array into a String Using the join Method
* PassedApply Functional Programming to Convert Strings to URL Slugs
* PassedUse the every Method to Check that Every Element in an Array Meets a Criteria
* PassedUse the some Method to Check that Any Elements in an Array Meet a Criteria
* PassedIntroduction to Currying and Partial Application

All code is in GitHub and repl.it here: [repl.it FuncProg](https://repl.it/@JohnJohnson2/FCC-FunctionalProgrammingChallenges) or [GitHub FuncProg](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FunctionalProgramming.js)


### Day 16: August 09, Thursday

**Today 's Progress**: I continue to work [Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Thoughts**: Some of the FCC_Challenges were pretty hard others very simple, I am hanging in there.

![XKCD.com](https://imgs.xkcd.com/comics/code_quality_3.png)

```javascript
//Combine Two Arrays Using the concat Method
//Use the concat method in the nonMutatingConcat function to concatenate attach to the end of original. The function should return the concatenated array.
function nonMutatingConcat(original, attach) {
  // Add your code below this line
  console.log((original), (attach));
  console.log("  Now CONCAT!!!");
  let myArr= first.concat(attach);
  console.log(myArr);
  return myArr;
  // Add your code above this line
}
var first = [1, 2, 3];
var second = [4, 5];
nonMutatingConcat(first, second);
//[Array.prototype.concat()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat)
console.log("-------------------Next------------------------");
```
This one took a few google searched and trying to figure out `concat`... [Array.prototype.concat()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat)

**Link(s) to work**

1. Continued [Introduction to Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Introduction to the Functional Programming Challenges**

* PassedRemove Elements from an Array Using slice Instead of splice
* PassedCombine Two Arrays Using the concat Method
* PassedAdd Elements to the End of an Array Using concat Instead of push
* PassedUse the reduce Method to Analyze Data
* PassedSort an Array Alphabetically using the sort Method


All code is in GitHub and repl.it here: [repl.it FuncProg](https://repl.it/@JohnJohnson2/FCC-FunctionalProgrammingChallenges) or [GitHub FuncProg](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FunctionalProgramming.js)


### Day 15: August 08, Wednesday

**Today 's Progress**: I continue to work [Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Thoughts**: These FCC_Challenges are pretty tricky, thank goodness for google! :grin:

![XKCD.com](https://imgs.xkcd.com/comics/bad_code.png)

```javascript
//Implement the filter Method on a Prototype
//Write your own Array.prototype.myFilter(), which should behave exactly like Array.prototype.filter(). You may use a for loop or the Array.prototype.forEach() method.
// the global Array
var s = [23, 65, 98, 5];
Array.prototype.myFilter = function(callback){
  var newArray = [];
  // Add your code below this line
   //console.log("this -->" + s);//Debug  
   this.forEach(function(obj) { //My solution
    //console.log("this -->" + obj);//Debug  
     if (callback(obj) == true) { //My solution
       newArray.push(obj); } });//My solution
      //console.log("this -->" + newArray);//Debug  
  // Add your code above this line
  return newArray;
};
var new_s = s.myFilter(function(item){
  return item % 2 === 1;
});
// Resources for this exercise: [Array Map, Filter and Reduce in JS](https://atendesigngroup.com/blog/array-map-filter-and-reduce-js)
console.log("-------------------Next------------------------");
```
This one took a few google searched and trying to figure out `forEach` in conjunction with `callback`... [Array Map, Filter and Reduce in JS](https://atendesigngroup.com/blog/array-map-filter-and-reduce-js)

**Link(s) to work**

1. Continued [Introduction to Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Introduction to the Functional Programming Challenges**

* PassedImplement map on a Prototype
* PassedUse the filter Method to Extract Data from an Array
* PassedImplement the filter Method on a Prototype
* PassedReturn Part of an Array Using the slice Method to Extract Data from an Array


All code is in GitHub and repl.it here: [repl.it FuncProg](https://repl.it/@JohnJohnson2/FCC-FunctionalProgrammingChallenges) or [GitHub FuncProg](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FunctionalProgramming.js)


### Day 14: August 07, Tuesday

**Today 's Progress**: I finished the challenges in  [Object Oriented Programming](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming) section and started [Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Thoughts**: Oh no these FCC_Challenges are not at all straight forward, and there are no hints or examples it's very challenging and not a lot of fun Thank goodness there is google! You can really tell the folks who did the last round of challenges cared about passing on information rather than this round of challenges designed to trick the student and make things obscure and nerve wracking. Today it was all about dealing with these frustrating misleading challenges yuck!

![XKCD.com](https://imgs.xkcd.com/comics/code_quality.png)

```javascript
//Implement map on a Prototype
//Write your own Array.prototype.myMap(), which should behave exactly like Array.prototype.map(). You may use a for loop or the forEach method.
// the global Array
var s = [23, 65, 98, 5];
Array.prototype.myMap = function(callback){
  var newArray = [];
  // Add your code below this line
   for (let i = 0; i < this.length; i++) {
     newArray.push(callback(this[i]));
  };
  // Add your code above this line
  return newArray;
};
var new_s = s.myMap(function(item){
  return console.log(item * 2);
});
console.log("-------------------Next------------------------");
```
This one took a few google searched and trying to figure out callback...

**Link(s) to work**

1. Continued [Introduction to the Object Oriented Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming)

**Introduction to the Object Oriented Programming**

* PassedUse a Mixin to Add Common Behavior Between Unrelated Objects
* PassedUse Closure to Protect Properties Within an Object from Being Modified Externally
* PassedUnderstand the Immediately Invoked Function Expression (IIFE)
* PassedUse an IIFE to Create a Module

2. Continued [Introduction to Functional Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming).

**Introduction to the Functional Programming Challenges**

* PassedLearn About Functional Programming
* PassedUnderstand Functional Programming Terminology
* PassedUnderstand the Hazards of Using Imperative Code
* PassedAvoid Mutations and Side Effects Using Functional Programming
* PassedPass Arguments to Avoid External Dependence in a Function
* PassedRefactor Global Variables Out of Functions
* PassedUse the map Method to Extract Data from an Array


All code is in GitHub and repl.it here: [Repl.it OOP](https://repl.it/@JohnJohnson2/FCCObjectOrientedProgramming), [repl.it FuncProg](https://repl.it/@JohnJohnson2/FCC-FunctionalProgrammingChallenges) or [GitHub OOP](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FCC_Challenges/ObjectOrientedProgramming.js), [GitHub FuncProg](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FunctionalProgramming.js)

### Day 13: August 06, Monday

**Today 's Progress**: I worked on the challenges in  [Object Oriented Programming](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming) section.

**Thoughts**: I like these FCC_Challenges very straight forward I wish all were this way :grin:. Today it was all about Constructors and prototypes pretty cool stuff. Since today was such a good coding day I thought I would share my favorite cartoon series, enjoy! 

![XKCD.com](https://imgs.xkcd.com/comics/disaster_movie.png)

```javascript
//Add Methods After Inheritance
//Add all necessary code so the Dog object inherits from Animal and the Dog's prototype constructor is set to Dog. Then add a bark() method to the Dog object so that beagle can both eat() and bark(). The bark() method should print "Woof!" to the console.
function Animal() { }
Animal.prototype.eat = function() { console.log("nom nom nom"); };
function Dog() { }
// Add your code below this line
Dog.prototype = Object.create(Animal.prototype);// my solution
Dog.prototype.constructor = Dog;// my solution
Dog.prototype.bark = function() {// my solution
  console.log( "Woof!");// my solution
};
// Add your code above this line
let beagle8 = new Dog();
beagle8.eat(); // Should print "nom nom nom"
beagle8.bark(); // Should print "Woof!" 
console.log("--------------------------------------------");
```
and the last one my personal favorite `Mixin` :lol:
```javascript
//Use a Mixin to Add Common Behavior Between Unrelated Objects
//Create a mixin named glideMixin that defines a method named glide. Then use the glideMixin to give both bird and boat the ability to glide.
let bird = {
  name: "Donald",
  numLegs: 2
};
let boat = {
  name: "Warrior",
  type: "race-boat"
};
// Add your code below this line
let glideMixin = function(obj) {
  obj.glide = function() {
    console.log("Gliding, wooosh!");
  }
};
 glideMixin(bird);
 glideMixin(boat);
bird.glide(); // prints "Gliding, wooosh!"
boat.glide();
console.log(bird); // prints "Gliding, wooosh!"
console.log(boat); // prints "Gliding, wooosh!"
console.log("--------------------------------------------");
```
**Link(s) to work**

1. Continued [Introduction to the Object Oriented Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming)

**Introduction to the Object Oriented Programming**

* PassedIterate Over All Properties
* PassedUnderstand the Constructor Property
* PassedChange the Prototype to a New Object
* PassedRemember to Set the Constructor Property when Changing the Prototype
* PassedUnderstand Where an Object’s Prototype Comes From
* PassedUnderstand the Prototype Chain
* PassedUse Inheritance So You Don't Repeat Yourself
* PassedInherit Behaviors from a Supertype
* PassedSet the Child's Prototype to an Instance of the Parent
* PassedReset an Inherited Constructor Property
* PassedAdd Methods After Inheritance
* PassedOverride Inherited Methods


All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/FCCObjectOrientedProgramming) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FCC_Challenges/ObjectOrientedProgramming.js)

### Day 12: August 05, Sunday

**Today 's Progress**: I worked on the challenges in  [Object Oriented Programming](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming) section.

**Thoughts**: These FCC_Challenges were a lot different from the Challenges in the algorithm section that were so tough, there were plenty of good examples and instructions but I manages with the help of Stackoverflow to get them done OOP section seems easy Should get a lot done tomorrow. [resources: Mozella](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter) and [Stackoverflow](https://stackoverflow.com)

```javascript
//Use Prototype Properties to Reduce Duplicate Code
//Add a numLegs property to the prototype of Dog
function Dog(name) {
  this.name = name;
}
Dog.prototype.numLegs = 4;
// Add your code above this line
let beagle = new Dog("Snoopy");
console.log(beagle); // prints Snoopy
console.log(Dog); // prints Snoopy
console.log("--------------------------------------------");
```

**Link(s) to work**

1. Started [Introduction to the Object Oriented Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming)

**Introduction to the Object Oriented Programming**

* PassedUse Dot Notation to Access the Properties of an Object
* PassedCreate a Method on an Object
* PassedMake Code More Reusable with the this Keyword
* PassedDefine a Constructor Function
* PassedUse a Constructor to Create Objects
* PassedExtend Constructors to Receive Arguments
* PassedVerify an Object's Constructor with instanceof
* PassedUnderstand Own Properties
* PassedUse Prototype Properties to Reduce Duplicate Code


All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/FCCObjectOrientedProgramming) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FCC_Challenges/ObjectOrientedProgramming.js)

## Day 11: August 04, Saturday

**Today 's Progress**: I finished the challenges in [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting) and started the [Object Oriented Programming](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming) section.

**Thoughts**: Felt good finishing some FCC_Challenges! The Challenges in the algorithm section were tough, there were no examples and vague instructions but I manages with the help of Stackoverflow to get them done OOP section seems easy Should get a lot done tomorrow. [resources: Mozella](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter) and [Stackoverflow](https://stackoverflow.com)

```javascript
//Chunky Monkey
//Write a function that splits an array (first argument) into groups the length of size (second argument) and returns them as a two-dimensional array.
function chunkArrayInGroups(arr, size) {//My solution reusing slice and push
  var a = 0;      
  var result = [0];
  for(var i = 0; i < arr.length; i += size){
      console.log(a);//Debugging
      result.push(arr.slice(a, size +i));
      a += size;
  }
  console.log(result + " & " + arr); //Debugging
  return result;
}
console.log(chunkArrayInGroups(["a", "b", "c", "d","a", "b", "c", "d"], 2));
console.log("--------------------------------------------------");
```

**Link(s) to work**

1. Finished [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting)

   **Introduction to Basic Algorithm Scripting**

   * PassedChunky Monkey

2. Started [Introduction to the Object Oriented Programming Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/object-oriented-programming)

   **Introduction to the Object Oriented Programming**

   * PassedCreate a Basic JavaScript Object

All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/FCCObjectOrientedProgramming) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/FCC_Challenges/ObjectOrientedProgramming.js)

### Day 10: August 03, Friday

**Today 's Progress**: I continued working the challenges in [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting) I coded for 1.5 hours.

**Thoughts**: This week is done this has been a trying week with very rough commutes today I left early and still had a 3 hour commute. We did more labs in OpenShift and probes in  CLI as well as configuring the GUI. The weekend is here and I plan on resting and knocking some FCC_Challenges out! Starting tonight. The Challenges, well I got stuck on the second one, and had to read more on `.filter` after that and some false starts I nailed it. [resources: Mozella](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)

```javascript
// Falsy Bouncer
//Remove all falsy values from an array.
//Falsy values in JavaScript are false, null, 0, "", undefined, and NaN.
function bouncer(arr) {
  // Don't show a false ID to this bouncer.
  return arr.filter(object => object);
  //or....
  //return arr.filter(Boolean);  
}
console.log(bouncer([7, "ate", "", false, 9]));
console.log(bouncer(["a", "b", "c"])); //should return ["a", "b", "c"].
console.log(bouncer([false, null, 0, NaN, undefined, ""])); //should return [].
console.log(bouncer([1, null, NaN, 2, undefined])); //should return [1, 2].
console.log("--------------------------------------------------");
```

**Link(s) to work**

1. Continuing with [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting)

   **Introduction to Basic Algorithm Scripting**

* PassedSlice and Splice
* PassedFalsy Bouncer
* PassedWhere do I Belong
* PassedMutations
All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/BasicAlgorithmScripting) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicAlgorithmScripting.js)

### Day 9: August 02, Thursday

**Today 's Progress**: I continued working the challenges in [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting) I coded for 1.5 hours.

**Thoughts**: Due to dentist appointment no commute today Yay!!!! :smile: I did my homework for the OpenShift class I'm in this week and read over what they went over today. The Challenges continue to be difficult but I'm hanging in there with this 100-day coding challenge. JavaScript is a bit different from plain Java like the `findElement` of an array in Java it's `return Arrays.asList(arr).contains(targetValue);` and in Java script its `var found = array1.find(function(element)` Took me a while to get the one below.

```javascript
//Finders Keepers
//Create a function that looks through an array (first argument) and returns the first element in the array that passes a truth test (second argument). If no element passes the test, return undefined.
function findElement(arr, func) {
  var num;
  console.log(arr);// for Debugging
  //console.log(arr.find((num) => {return func(num)})); //for troubleshooting.
  return arr.find((num) => {return func(num)});
}
console.log(findElement([1, 2, 3, 4], num => num % 2 === 0));//should return 2.
console.log(findElement([1, 3, 5, 8, 9, 10], num => num % 2 === 0)); //should return 8.
console.log(findElement([1, 3, 5, 9], num => num % 2 === 0)); //should return undefined.
console.log("--------------------------------------------------");
```

**Link(s) to work**

1. Continuing with [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting)

   **Introduction to Basic Algorithm Scripting**

* PassedBooFinders Keepers
* PassedBoo who
* PassedTitle Case a Sentence

All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/BasicAlgorithmScripting) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicAlgorithmScripting.js)

### Day 8: August 01, Wednesday

**Today 's Progress**: I continued working the challanges in [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting) I coded for 1.5 hours.

**Thoughts**: This week is not getting any easier I had another long day at work (counting the hellish commute 2.5 hours to go 65 miles) we did more docker files in OpenShift and Dockerfiles CLI also RedHat's OpenShift GUI console. Tomorrow I have a dentist appointment and homework for the OpenShift class I'm in this week. The Challenges continue to be difficult but I'm hanging in there with this 100-day coding challenge.

```javascript
function confirmEnding(str, target) {
  // "Never give up and good luck will find you."
  // -- Falcor
  var sln = target.length;
  console.log(sln);//Debugging statment
  if(str.substr(-sln) === target){
    console.log(str.substr(-sln) + " = " + target);//Debugging statment
    return true;
  } else {
    return false;
  }
}
confirmEnding("Bastian", "n");
```

**Link(s) to work**

1. Continuing with [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting)

   **Introduction to Basic Algorithm Scripting**

* PassedConfirm the Ending
* PassedRepeat a String Repeat a String
* PassedTruncate a String

All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/BasicAlgorithmScripting) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicAlgorithmScripting.js)

### Day 7: July 31, Tuesday

**Today 's Progress**: I continued the challenges in [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting) I coded for 1.5 hours.

**Thoughts**: This week is a tough week I had another long day at work (counting the hellish commute) and was knee deep in Docker CLI and RedHat's OpenShift. I feel like I could sleep for a week. Tomorrow it’s another long commute day. These challenges seem hard, to me coming up with code from scratch is difficult I should try what I did in college and make a UML model of the user story before starting to write the code.

```javascript
//Find the Longest Word in a String
//Return the length of the longest word in the provided sentence.
function findLongestWordLength(str) {
    var obj = str.split(' ');// Split the words up
    var letterCount = 0; //variable for number of letters
    for (var i = 0; i < obj.length; i++) { //loop through the split string
        if (letterCount < obj[i].length) { // this looks ugly I'm sure there is a better way
            letterCount = obj[i].length;
        }
    }
    console.log(letterCount);
    return letterCount;    
} 
findLongestWordLength("The quick brown fox jumped over the lazy dog");
```

**Link(s) to work**
1.  Continuing with [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting)

Introduction to Basic Algorithm Scripting

* PassedFind the Longest Word in a String
* PassedReturn Largest Numbers in Arrays

All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/BasicAlgorithmScripting) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicAlgorithmScripting.js)

### Day 6: July 30, Monday

 **Today 's Progress**: I started challanges in [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting) I coded for 1 hour.

**Thoughts**: Today was a tough day I had a 15.5-hour day at work (counting the commute) and was knee deep in Docker CLI. I feel so tired but I managed to get some coding before bed. Tomorrow it’s Kubernetes and another long day. 

```javascript
//The algorithm to convert from Celsius to Fahrenheit is the temperature in Celsius times 9/5, plus 32.
function convertToF(celsius) {
  let fahrenheit = celsius * 9/5 + 32 ;// my solution
  return fahrenheit;
}
convertToF(30);
```

**Link(s) to work**
1.  Started [Introduction to Basic Algorithm Scripting](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting)

Introduction to Basic Algorithm Scripting

* PassedConvert Celsius to Fahrenheit
* PassedReverse a String
* PassedFactorialize a Number

All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/BasicAlgorithmScripting) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicAlgorithmScripting.js)

### Day 5: July 29, Sunday

 **Today 's Progress**: My goal today is to finnish the remaining challanges in [Introduction to the Basic Data Structure Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-data-structures).

**Thoughts**: Remembered NO OVER THINKING!!! I have a bad habit of over complicating simple instructions, well it says do "a" I think well should i get to "a" via `ax^2+ab+c=0` :smile:

Today didn’t disappoint I forgot to capitalize the "O" in "Object" and spent almost an hour trying to figure why the unit tests weren’t passing ARGGGGG!!!

```javascript
//Generate an Array of All Object Keys with Object.keys()
//Finish writing the getArrayOfUsers function so that it returns an array containing all the properties in the object it receives as an argument.
let users2 = {
  Alan: {
    age: 27,
    online: false
  },
  Jeff: {
    age: 32,
    online: true
  },
  Sarah: {
    age: 48,
    online: false
  },
  Ryan: {
    age: 19,
    online: true
  }
};
function getArrayOfUsers(obj) {
  // change code below this line
  return Object.keys(obj);//OH GOD!!! an hour just because I forgot to capitalize O
  // change code above this line
}
console.log(getArrayOfUsers(users2));
```

**Link(s) to work**
1. [Introduction to the Basic Data Structure Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-data-structures)

* PassedAdd Key-Value Pairs to JavaScript Objects
* PassedModify an Object Nested Within an Object
* PassedAccess Property Names with Bracket Notation
* PassedUse the delete Keyword to Remove Object Properties
* PassedCheck if an Object has a Property
* Passed Iterate Through the Keys of an Object with a for...in Statement
* PassedGenerate an Array of All Object Keys with Object.keys()
* PassedModify an Array Stored in an Object

All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/FCCBasicDataStructurs2) or [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicDataStructure.js)

### Day 4: July 28, Saturday

**Today's Progress**: I've gone through the next few exercises on FreeCodeCamp Basic Data Structures.

**Thoughts** I knew this was going to be tricky, I remembered over thinking a couple of the challenges yesterday but even though I tried to keep it simple, but once again I made at least one spaghetti code monster :monster: I had a hard time with one of the challenges, I usually rely on JS Libraries Writing your own JS can be challenging. :smile:

```javascript
//Copy Array Items Using slice()
function forecast(arr) {
// change code below this line
  return arr.slice(2, 4); //My solution
}
// do not change code below this line
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));
```
Another way of doing it (This was the first way I tried it)

I had to add debugging statements to find where i was missing the unit test.

```javascript
function forecastAlt(arr) {
// change code below this line
let myArr = arr.slice(2, 4) ;
console.log("This is the content of myArr = " + myArr); //for debugging
console.log("This is the content of arr = " + arr); //for debugging
return arr = myArr; //my solution 
//(after hours fighting code, once I put the debug statements in it was pretty clear)
}
// do not change code below this line
console.log(forecastAlt(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));
```

**Link(s) to work**
1. [Introduction to the Basic Data Structure Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-data-structures)

* PassedAdd Items Using splice()
* PassedCopy Array Items Using slice()
* PassedCopy an Array with the Spread Operator
* PassedCombine Arrays with the Spread Operator
* PassedCheck For The Presence of an Element With indexOf()
* PassedIterate Through All an Array's Items Using For Loops
* PassedCreate complex multi-dimensional arrays

All code is in GitHub and repl.it here: [Repl.it](https://repl.it/@JohnJohnson2/FCCBasicDataStructurs2) [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicDataStructure.js)

### Day 3: July 27, Friday

**Today's Progress**: I've gone through the first few exercises on FreeCodeCamp Basic Data Structures.

**Thoughts** I thought this was going to be easy, but yeah I over thought a couple of the challenges and spent a few hours trying to fix the spaghetti code monster I created pretty tricky there FCC. :smile:

```javascript
//Remove Items from an Array with pop() and shift()
function popShift(arr) {
  let popped = arr.pop(); // change this line (This was tricky I was over thinking it)
  let shifted = arr.shift(); // change this line
  return [shifted, popped];
}
// do not change code below this line
console.log(popShift(['challenge', 'is', 'not', 'complete']));
```

**Link(s) to work**
1. [Introduction to the Basic Data Structure Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-data-structures)

* PassedUse an Array to Store a Collection of Data
* PassedAccess an Array's Contents Using Bracket Notation
* PassedAdd Items to an Array with push() and unshift()
* PassedRemove Items from an Array with pop() and shift()
* PassedRemove Items Using splice()
HAll in GitHub and rep.it here: [Rep.it](https://repl.it/@JohnJohnson2/FCCBasicDataStructurs2) [GitHub](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/BasicDataStructure.js)

  ### Day 2: July 26, Thursday

**Today's Progress**: I've gone through the remaining exercises on FreeCodeCamp Debugging Project.

**Thoughts** I've had a lot of experiance debugging so was able to get though all the excersizes a couple we pretty tricky.

```javascript
//Debugging: Use Caution When Reinitializing Variables Inside a Loop
// original buggy code...

function zeroArray(m, n) {
  // Creates a 2-D array with m rows and n columns of zeroes
  let newArray = [];
  let row = [];
  for (let i = 0; i < m; i++) {
    // Adds the m-th row into newArray
    /**** //the offending code Loop****
    for (let j = 0; j < n; j++) {
      // Pushes n zeroes into the current row to create the columns
      row.push(0);
    }
    */
    // Pushes the current row, which now has n zeroes in it, to the array
    newArray.push(row);
  }
  for (let j = 0; j < n; j++) { //my solution move outside first loop
      // Pushes n zeroes into the current row to create the columns
      row.push(0);
    }
  return newArray;
}
let matrix = zeroArray(3, 2);
console.log(matrix);
```

**Link(s) to work**
1. [Introduction to the Debugging Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/debugging)
*  PassedCatch Misspelled Variable and Function Names
*  PassedCatch Unclosed Parentheses, Brackets, Braces and Quotes
*  PassedCatch Mixed Usage of Single and Double Quotes
*  PassedCatch Use of Assignment Operator Instead of Equality Operator
*  PassedCatch Missing Open and Closing Parenthesis After a Function Call
*  PassedCatch Arguments Passed in the Wrong Order When Calling a Function
*  PassedCatch Off By One Errors When Using Indexing
*  PassedUse Caution When Reinitializing Variables Inside a Loop
*  PassedPrevent Infinite Loops with a Valid Terminal Condition
[Code Here](https://github.com/Johnny2136/FCC-Projects/blob/master/FCC_Challenges/IntroductionToTheDebuggingChallenges.js)
and all in repl.it https://repl.it/@JohnJohnson2/DebuggingFCC

### Day 1: July 25, Wednesday

**Today's Progress**: I've gone through 3 exercises on FreeCodeCamp and did one project.

**Thoughts** II've had many coding classes in college and want to step up my game, I found out that coding is not like riding a bike you don’t just learn it and then know it from now on, I don’t code at work so my skills rusted up quite a bit. I want to revamp them and try and stay current with modern technology I started following students of [CodeClan](https://codeclan.com/) in Scotland and found Free Code Camp so I’m working through the course ware and once done hope to contribute to the project, and it's an awesome feeling when I finally solve an exercise challenge after a lot of failing unit tests that green banner appears and it’s like “YEEEESSSS!!!!!!”.

**Link(s) to work**
1. [Palindrome Checker](https://github.com/Johnny2136/FCC-Projects/blob/master/PalindromeChecker.js)
2. [Introduction to the Debugging Challenges](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/debugging)
  * PassedUse the JavaScript Console to Check the Value of a Variable
  * PassedUnderstanding the Differences between the freeCodeCamp and Browser Console
  * PassedUse typeof to Check the Type of a Variable (https://www.freecodecamp.com)
