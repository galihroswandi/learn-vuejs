<template>
  <h1 id="rerender">Tulisan {{ message }}</h1>

  <button @click="message = 'Update !!'">Update !!</button>
</template>

<script>
export default {
  data() {
    return {
      message: "Dirender ulang",
    };
  },
  beforeCreate() {
    console.log("Before created");
  },
  created() {
    console.log("Created");
    console.log({ message: this.message });
    console.log({ component: document.getElementById("rerender") });
  },
  beforeMount() {
    console.log("Before mounted");
  },
  mounted() {
    console.log("Mounted");
    console.log({ message: this.message });
    console.log({ component: document.getElementById("rerender") });
  },
  beforeUpdate() {
    console.log("Before updated");
    console.log({ message: this.message });
    console.log({
      textContent: document.getElementById("rerender").textContent,
    });
  },
  updated() {
    console.log("Updated");
    console.log({ message: this.message });
    console.log({
      textContent: document.getElementById("rerender").textContent,
    });
  },
  beforeUnmount() {
    console.log("Before unmounted");
  },
  unmounted() {
    console.log("Unmounted");
  },
};
</script>
