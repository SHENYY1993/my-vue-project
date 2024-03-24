<script>
export default {
  name: "ToDoForm",
  methods: {
    onSubmit() {
      if(this.label === ""){
        console.log('Label is empty')
        return;
      }
      console.log('Label value: ', this.label);
      this.$emit("todo-added", this.label);
      this.label = "";
    },
  },
  data() {
    return {
      label: "",
    }
  }
}
</script>

<template>
  <form v-on:submit.prevent="onSubmit">
    <label for="new-todo-input"> What needs to be done? </label>
    <input
        type="text"
        id="new-todo-input"
        name="new-todo"
        autocomplete="off"
        v-model.lazy.trim="label"/>
    <button type="submit">Add</button>
  </form>
</template>


<style scoped>

</style>