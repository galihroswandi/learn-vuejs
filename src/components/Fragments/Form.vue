<template>
  <div class="join">
    <input
      v-model="inputValue"
      class="input input-bordered mr-2"
      placeholder="Activity..."
      @keyup.enter="addTodo"
    />
    <button class="btn btn-outline btn-primary" @click="addTodo">Add</button>
  </div>
</template>

<script>
export default {
  emits: ["add-todo"],
  data() {
    return {
      inputValue: "",
    };
  },
  methods: {
    addTodo() {
      this.$emit("add-todo", this.inputValue);
      this.inputValue = "";
    },
  },
};
</script>
