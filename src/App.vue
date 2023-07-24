<template>
  <!-- v-once artinya render satu kali jadi ketika ada perubahan komponent ini tidak akan dirender ulang -->
  <h1 v-once>Tulisan {{ message }}</h1>

  <button @click="message = 'Updated !!'">Update !!</button>
</template>

<script>
export default {
  data() {
    return {
      message: "Dirender ulang",
    };
  },
};
</script>
