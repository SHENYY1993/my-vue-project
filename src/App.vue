<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <h1>To-Do List</h1>
  <ul>
    <li v-for="item in ToDoItems" :key="item.id">
      <to-do-item :label="item.label" :done="true" :id="item.id"></to-do-item>
    </li>
  </ul>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
// import DemoComponent from "./components/DemoComponent.vue";
import ToDoItem from "./components/ToDoItem.vue";
import uniqueId from "lodash.uniqueid";

export default {
  name: 'App',
  components: {
    // 本地注册组件
    HelloWorld,
    ToDoItem,
  },
  data() {
    return {
      ToDoItems: [
        {
          id: uniqueId("todo-"),
          label: "Learn Vue",
          done: false
        },
        {
          id: uniqueId("todo-"),
          label: "Create a Vue project with the CLI",
          done: true,
        },
        {
          id: uniqueId("todo-"),
          label: "Have fun",
          done: true
        },
        {
          id: uniqueId("todo-"),
          label: "Create a to-do list",
          done: false
        },
      ],
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
