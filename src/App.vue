<template>
  <h1>Ini adalah parent component</h1>
  <ChildComponent />
</template>

<script>
import ChildComponent from "./components/ChildComponent.vue";
export default {
  components: { ChildComponent },
};
</script>
