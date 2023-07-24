<template>
  <div class="wrapper" style="display: flex; align-items: center; gap: 1rem">
    <button @click="minCount">-</button>
    <h1>{{ count }}</h1>
    <button @click="count++">+</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    minCount() {
      if (this.count > 0) {
        this.count--;
      }
    },
  },
};
</script>
