<template>
  <div class="p-5">
    <h4>{{ nilai }}</h4>
    <button @click="add">Add</button>
  </div>
</template>

<script>
import { ref, reactive, toRefs } from "vue";

export default {
  setup() {
    const count = reactive({
      nilai: 0,
    });

    const add = () => {
      count.nilai++;
    };

    return { ...toRefs(count), add };
  },
};
</script>
