<template>
  <Child>
    <main>
      <p>Children 1</p>
      <p>Children 2</p>
      <p>Children 3</p>
      <p>Children 4</p>
      <p>Children 5</p>
    </main>
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
