<template>
  <app-child-1 />
</template>

<script>
import Child1 from "./components/ChildComponent1.vue";
export default {
  components: { "app-child-1": Child1 },
  provide: {
    author: "Jhon Doe",
  },
};
</script>

<style>
body {
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
}
</style>
