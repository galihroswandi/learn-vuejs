<template>
  <h1>Ini adalah child component hi.</h1>
  <p>{{ text }}</p>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      default: "",
    },
  },
};
</script>
