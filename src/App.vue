<template>
  <div class="p-5">
    <h4>{{ nilai }}</h4>
    <button @click="add">Add</button>

    <h4>Result: {{ result }}</h4>
  </div>
</template>

<script>
import { ref, reactive, toRefs, computed } from "vue";

export default {
  setup() {
    const count = reactive({
      nilai: 0,
    });

    const addNum = ref(1);

    const result = computed(() => count.nilai + addNum.value);

    const add = () => {
      count.nilai++;
    };

    return { ...toRefs(count), add, result };
  },
};
</script>
