<template>
  <div class="p-5">
    <h4>{{ nilai }}</h4>
    <button @click="add">Add</button>
  </div>
</template>

<script>
import { reactive, toRefs, ref, watch } from "vue";

export default {
  setup() {
    const count = reactive({
      nilai: 0,
      foo: "bar",
    });

    const num1 = ref(1);
    const num2 = ref(2);

    const add = () => {
      count.nilai++;
      num1.value++;
      num2.value++;
    };

    watch([num1, num2], (current, before) => {
      console.log(num1.value);
      console.log(current);
      console.log(before);
    });

    watch(
      () => count.nilai,
      (current, before) => {
        console.log({ current });
        console.log({ before });
      }
    );

    return { ...toRefs(count), add };
  },
};
</script>
