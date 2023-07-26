<template>
  <div class="p-5">
    <h1 class="text-4xl">{{ message }}</h1>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const message = ref("Hello Jhon Doe");

    setTimeout(() => {
      message.value = "Hello John Doe";
    }, 2000);

    return { message };
  },
};
</script>
