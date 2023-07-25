<template>
  <teleport to="#target-teleport">
    <app-home />
  </teleport>
</template>

<script>
import HomeComp from "./components/Home.vue";

export default {
  components: { "app-home": HomeComp },
};
</script>

<style>
body {
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
}
</style>
