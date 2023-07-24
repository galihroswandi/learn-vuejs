<template>
  <div>{{ total }}</div>

  <input v-model="num1" type="number" />
  <input v-model="num2" type="number" />
</template>

<script>
export default {
  data() {
    return {
      num1: 0,
      num2: 0,
    };
  },
  computed: {
    total() {
      if (this.num1 > this.num2) {
        return "Number 1 lebih besar dari Number 2";
      } else {
        return "Number 1 lebih kecil dari Number 2";
      }
    },
  },
};
</script>
