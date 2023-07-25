<template>
  <div>{{ message }}</div>

  <input v-model="message" type="text" />
</template>

<script>
export default {
  data() {
    return {
      message: "Hello Vue 3!",
    };
  },
  watch: {
    message(value) {
      console.log({ perubahanDiMessage: value });
    },
  },
};
</script>
