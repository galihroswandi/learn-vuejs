<template>
  <h1>{{ message }}</h1>

  <a :title="message">Hover Me 3 Second</a>
</template>

<script>
export default {
  data() {
    return {
      message: "Hi, World!",
    };
  },
};
</script>
