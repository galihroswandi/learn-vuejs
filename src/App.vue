<template>
  <div class="p-5">
    <app-header />
    <main class="mt-5">
      <app-form @add-todo="addTodo" />
      <app-list
        :todos="todos"
        @delete-todo="deleteTodo"
        @todo-done="todoDone"
      />
      <span class="inline-block mt-5">Total todo: {{ totalTodos }}</span>
    </main>
  </div>
</template>

<script>
import Header from "./components/Fragments/Header.vue";
import FormInput from "./components/Fragments/Form.vue";
import ListTodo from "./components/Fragments/ListTodo.vue";

export default {
  components: {
    "app-header": Header,
    "app-form": FormInput,
    "app-list": ListTodo,
  },

  data() {
    return {
      todos: [],
    };
  },

  created() {
    this.todos = JSON.parse(localStorage.getItem("todos")) || [];
  },

  computed: {
    totalTodos() {
      return this.todos.length;
    },
  },

  methods: {
    addTodo(value) {
      this.todos.unshift({
        title: value,
        isDone: false,
      });
      this.saveToLocalstorage();
    },
    deleteTodo(id) {
      this.todos = this.todos.filter((item, index) => index !== id && item);
      this.saveToLocalstorage();
    },
    todoDone(id) {
      this.todos = this.todos.filter((item, index) => {
        index === id && (item.isDone = !item.isDone);
        return item;
      });
      this.saveToLocalstorage();
    },
    saveToLocalstorage() {
      localStorage.setItem("todos", JSON.stringify(this.todos));
    },
  },
};
</script>

<style></style>
