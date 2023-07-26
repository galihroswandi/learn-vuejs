<template>
  <div class="p-5">
    <h1 class="text-4xl">Name : {{ name }}</h1>
    <p class="text-xl">Age : {{ age }}</p>
  </div>
</template>

<script>
import { ref, reactive, toRefs } from "vue";

export default {
  setup() {
    const user = reactive({
      name: "Jhon Doe",
      age: 25,
    });

    setTimeout(() => {
      user.name = "JHON";
    }, 2000);

    return { ...toRefs(user) }; //! Fungsi toRefs untuk mengeluarkan property object menjadi ref masing masing
  },
};
</script>
