<template lang="html">
  <div>
    <h1> {{ message }} </h1>
    <addTodo v-on:submit-todo="submitTodo"></addTodo>

    <div class="mt-5">
      <div class="row">
        <div class="col-4 mb-3" v-for="todo in todos">
          <todoCard v-bind:task="todo"></todoCard>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import todoCard from './components/todo';
import addTodo from './components/addTodo';

export default {
  data() {
    return {
      message: 'Hello Vue Component, nice to meet you! I hope we will get along',
      todos: []
    }
  },
  components: {
    todoCard,
    addTodo
  },
  methods: {
    submitTodo(task) {
      // console.log("kepanggil dari anak saya ", task);
      this.todos.push(task);
    }
  }
}
</script>

<style lang="css" scoped>
</style>
