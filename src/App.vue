<template>
  <Child>
    <template v-slot:default="{ data }">Header : {{ data }}</template>
    <template v-slot:main="{ data }">Content : {{ data }}</template>
    <template v-slot:footer="{ data }">Footer : {{ data }}</template>
  </Child>
</template>

<script>
import Child from "./components/ChildComponent.vue";
export default {
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
