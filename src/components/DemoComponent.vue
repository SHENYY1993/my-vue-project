<template>
  <div>
    <input type="checkbox" id="todo-item" checked="false"/>
    <label for="todo-item">{{ label }}</label>
  </div>
</template>

<script>
export default {
  props: {
    label: {required: true, type: String, default: 'New item'},
    done: {default: false, type: Boolean}
  }
};
</script>