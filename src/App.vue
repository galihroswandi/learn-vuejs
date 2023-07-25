<template>
  <h1 :class="status ? 'success' : 'failed'">STATUS</h1>

  <button @click="status = !status">Change Status !</button>

  <h1 :class="[greenClass, boldClass]">MULTIPLE CLASS</h1>
</template>

<script>
export default {
  data() {
    return {
      status: true,
      greenClass: "success",
      boldClass: "bold",
    };
  },
};
</script>

<style>
body {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}
.success {
  color: green;
  transition: all 0.5s ease-in-out;
}
.failed {
  color: red;
  transition: all 0.5s ease-in-out;
}
.bold {
  font-weight: 700;
}
</style>
