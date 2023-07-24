<template>
  <ul>
    <li v-for="(todo, index) in todos" :key="todo.id">
      {{ index + 1 + " - " + todo.activity }}
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      todos: [
        { id: 1, activity: "Olahraga" },
        { id: 2, activity: "Masak" },
        { id: 3, activity: "Mandi" },
        { id: 4, activity: "Makan" },
      ],
    };
  },
};
</script>
