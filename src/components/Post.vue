<template>
  <div>
    <div v-if="data.length > 0" v-for="item in data" :key="item.id">
      <h4>{{ item.title }}</h4>
      <p>{{ item.body }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      data: [],
    };
  },
  async created() {
    const res = await fetch("https://jsonplaceholder.typicode.com/posts");
    const data = await res.json();
    this.data = data;
  },
};
</script>
