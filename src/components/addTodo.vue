<template>
  <form v-on:submit.prevent="$emit('submit-todo', todo)">
    <div class="input-group mb-3">
      <input type="text" v-model="todo">
      <button type="submit" name="button">Add Todo</button>
    </div>
  </form>
</template>

<script>
import axios from '../api/axios'

export default {
  data() {
    return {
      todo: ''
    }
  },
  methods: {
    addTodo() {
      axios.post
      this.$emit('submit-todo', this.todo)
    }
  }
}
</script>

<style lang="css" scoped>
</style>
