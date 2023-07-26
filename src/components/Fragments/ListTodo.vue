<template>
  <ul class="menu bg-base-200 rounded-box mt-12 w-full">
    <li v-if="todos.length > 0" v-for="(todo, index) in todos" :key="index">
      <div class="flex flex-row justify-between items-center">
        <h2 class="text-slate-600 text-xl">
          <del v-if="todo.isDone">{{ index + 1 }}. {{ todo.title }}</del>
          <span v-else>{{ index + 1 }}. {{ todo.title }}</span>
        </h2>
        <app-button-todo
          :indexTodo="index"
          @delete-todo="deleteTodo"
          @todo-done="todoDone"
        />
      </div>
    </li>
    <span v-else class="text-center text-base text-slate-800 py-2"
      >No data todo</span
    >
  </ul>
</template>

<script>
import ButtonActionTodo from "../Elements/ButtonActionTodo.vue";
export default {
  emits: ["delete-todo"],
  components: {
    "app-button-todo": ButtonActionTodo,
  },
  props: {
    todos: {
      type: Array,
      required: true,
      default: [],
    },
  },
  methods: {
    deleteTodo(id) {
      this.$emit("delete-todo", id);
    },
    todoDone(id) {
      this.$emit("todo-done", id);
    },
  },
};
</script>
