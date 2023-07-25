<template>
  <Child @child-clicked="clickMe" ref="childClicked" />

  <button @click="onClick">Button from parent</button>
</template>

<script>
import Child from "./components/ChildComponent.vue";
export default {
  components: { Child },
  methods: {
    clickMe() {
      console.log("click from child");
    },
    onClick() {
      this.$refs.childClicked.onParentClick();
    },
  },
};
</script>

<style>
body {
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
}
</style>
