<template>
  <div class="p-5">
    <h1 class="text-4xl">Name : {{ user.name }}</h1>
    <p class="text-xl">Age : {{ user.age }}</p>
  </div>
</template>

<script>
import { ref, reactive } from "vue";

export default {
  setup() {
    const user = reactive({
      name: "Jhon Doe",
      age: 25,
    });

    setTimeout(() => {
      user.name = "JHON";
    }, 2000);

    return { user };
  },
};
</script>
