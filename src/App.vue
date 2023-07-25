<template>
  <div>{{ discount }}</div>

  <input v-model="num1" type="number" />
  <input v-model="num2" type="number" />

  <button @click="addDiscount">+ Dicount</button>
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
    discount: {
      get() {
        return parseInt(this.num1) + parseInt(this.num2);
      },
      set(value) {
        this.num1 -= value;
        this.num2 -= value;
      },
    },
  },
  methods: {
    addDiscount() {
      this.discount = 200;
    },
  },
};
</script>
