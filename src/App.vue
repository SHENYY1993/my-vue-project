<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <h1>To-Do List</h1>
  <ul>
    <li>
      <demo-component></demo-component>
      <demo-component label="My todo item"></demo-component>
    </li>
  </ul>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import DemoComponent from "./components/DemoComponent.vue";

export default {
  name: 'App',
  components: {
    // 本地注册组件
    HelloWorld,
    DemoComponent
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
