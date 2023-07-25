<template>
  <h1>{{ message }}</h1>

  <!-- Cara susah -->
  <Child :value="message" @update:value-emit="message = $event" />

  <!-- Cara gampang -->
  <!-- <Child v-model="message" /> -->
</template>

<script>
import Child from "./components/ChildComponent.vue";
export default {
  data() {
    return {
      message: "No Message",
    };
  },
  components: {
    Child,
  },
};
</script>

<style>
body {
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
}
</style>
