<template>
  <Child>
    <template v-slot:default>This is header</template>
    <template v-slot:main>This is main content</template>
    <template v-slot:footer>This is footer</template>
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
