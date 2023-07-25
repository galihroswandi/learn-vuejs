<template>
  <h1>Ini Child Component</h1>

  <button @click="onPress">Click Me</button>
</template>

<script>
export default {
  emits: ["child-clicked"],
  methods: {
    onPress() {
      this.$emit("child-clicked");
    },
    onParentClick() {
      console.log("click dari parent");
    },
  },
};
</script>
