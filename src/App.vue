/* eslint-disable no-console */
<template>
  <div id="app">
    <HelloWorld msg="HelloWorld"/>
    <Todo/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Todo from './components/Todo.vue'


export default {
  name: 'app',
  components: {
    HelloWorld, Todo
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
