<template>
  <div v-html="message"></div>
</template>

<script>
export default {
  data() {
    return {
      message:
        "<span style='color: blue; font-size: 5rem;'>Dirender ulang</span>",
    };
  },
};
</script>
