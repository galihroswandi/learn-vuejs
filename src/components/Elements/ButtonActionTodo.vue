<template>
  <div class="flex items-center gap-x-3">
    <button
      class="btn btn-outline btn-info btn-sm text-slate-50"
      @click="todoDone(indexTodo)"
    >
      Done
    </button>
    <button
      class="btn btn-circle btn-secondary btn-sm text-slate-50"
      @click="deleteTodo(indexTodo)"
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="h-6 w-6"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M6 18L18 6M6 6l12 12"
        />
      </svg>
    </button>
  </div>
</template>

<script>
export default {
  emits: ["delete-todo"],
  props: {
    indexTodo: {
      type: Number,
      required: true,
      default: 0,
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
