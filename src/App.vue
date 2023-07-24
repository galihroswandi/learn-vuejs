<template>
  <h1>Ini adalah parent component</h1>

  <ChildComponent v-for="(todo, index) in todos" :key="index" :text="todo" />
</template>

<script>
import ChildComponent from "./components/ChildComponent.vue";
export default {
  data() {
    return {
      text: "ini component kedua.",
      todos: ["pertama", "kedua", "ketiga"],
    };
  },
  components: { ChildComponent },
};
</script>
