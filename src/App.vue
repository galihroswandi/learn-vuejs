<template>
  <h1>{{ message }}</h1>

  <input v-model="message" type="text" />

  <!-- v-model kependekan dari : -->
  <input type="text" :value="message" @input="message = $event.target.value" />
</template>

<script>
export default {
  data() {
    return {
      message: "say hi",
    };
  },
};
</script>
