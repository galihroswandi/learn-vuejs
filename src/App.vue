<template>
  <h1>Ini adalah parent component</h1>
  <ChildComponent text="Hallo" />
  <ChildComponent :text="text" />
</template>

<script>
import ChildComponent from "./components/ChildComponent.vue";
export default {
  data() {
    return {
      text: "ini component kedua.",
    };
  },
  components: { ChildComponent },
};
</script>
