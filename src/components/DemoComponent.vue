<template>
  <div>
    <!--    <input type="checkbox" id="todo-item" checked="checked"/>-->
    <!--    <input type="checkbox" id="todo-item" v-bind:checked="isDone"/>-->
    <input type="checkbox" :id="id" v-bind:checked="isDone"/>
<!--    <label for="todo-item">{{ label }}</label>-->
    <label :for="id">{{ label }}</label>
  </div>
</template>

<script>
import uniqueId from "lodash.uniqueid";

export default {
  // props就是父级component使用该component时可以传入的参数
  props: {
    label: {required: true, type: String, default: 'New item'},
    done: {default: false, type: Boolean}
  },
  data() {
    return {
      isDone: this.done,
      id: uniqueId("todo-"),
    };
  },
};
</script>