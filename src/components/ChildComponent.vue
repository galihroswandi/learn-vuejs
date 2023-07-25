<template>
  <h1>{{ message }}</h1>
  <h2>{{ number }}</h2>
</template>

<script>
export default {
  props: {
    message: "",
    number: {
      type: Number,
      default: 0,
    },
  },
};
</script>
