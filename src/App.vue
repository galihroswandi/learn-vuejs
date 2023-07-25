<template>
  <h1>My Todos</h1>
  <ul v-if="todos">
    <li v-for="todo in todos">
      {{ todo.title }} - {{ todo.completed ? "completed" : "not completed" }}
    </li>
  </ul>
  <div>
    <input type="text" v-model="title" />
    <button @click="addTodo">+ Todo</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      todos: [],
      title: "",
    };
  },
  methods: {
    addTodo() {
      this.todos.push({
        title: this.title,
        completed: false,
      });
    },
  },
};
</script>
