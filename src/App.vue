<template>
  <pre>{{ $data }}</pre>
</template>

<script>
import basic from "./mixins/basic";
import merge from "./mixins/merge";

export default {
  mixins: [basic, merge],
  data() {
    return {
      name: "Jhon Doe",
    };
  },
};
</script>

<style>
body {
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
}
</style>
