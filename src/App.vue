<template>
  <h1 v-if="status">INI TAMPIL</h1>

  <button @click="setStatus">
    <span v-if="!status">Tampilkan Text</span>
    <span v-else-if="status">Hide Text</span>
    <span v-else>Else Text</span>
  </button>
</template>

<script>
export default {
  data() {
    return {
      status: false,
    };
  },
  methods: {
    setStatus() {
      this.status = !this.status;
    },
  },
};
</script>
