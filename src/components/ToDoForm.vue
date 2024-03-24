<template>
  <form v-on:submit.prevent="onSubmit">
    <h2 class="label-wrapper">
      <label for="new-todo-input" class="label__lg">
        What needs to be done?
      </label>
    </h2>
    <input
        class="input__lg"
        type="text"
        id="new-todo-input"
        name="new-todo"
        autocomplete="off"
        v-model.lazy.trim="label"/>
    <button class="btn btn__primary btn__lg" type="submit">Add</button>
  </form>
</template>

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

<style scoped>

</style>