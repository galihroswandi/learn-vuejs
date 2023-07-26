<template>
  <div class="p-5">
    <h4>{{ nilai }}</h4>
    <button @click="add">Add</button>

    <h4>Result: {{ result }}</h4>
  </div>
</template>

<script>
import { ref, reactive, toRefs, watchEffect, computed } from "vue";

export default {
  setup() {
    const count = reactive({
      nilai: 0,
      foo: "bar",
    });

    const addNum = ref(1);

    const result = computed({
      get: () => count.nilai + addNum.value,
      set: (newVal) => {
        addNum.value = newVal;
      },
    });

    watchEffect(
      () => {
        console.log(count.nilai);
      },
      {
        flush: "post",
        onTrigger(e) {
          console.log({ onTrigger: e });
        },
        onTrack(e) {
          console.log({ onTrack: e });
        },
      }
    );

    const add = () => {
      result.value = 5;
      count.nilai++;
    };

    return { ...toRefs(count), add, result };
  },
};
</script>
