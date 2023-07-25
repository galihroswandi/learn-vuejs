<template>
  <nav>
    <button v-for="(tab, index) in tabs" :key="index" @click="currentTab = tab">
      {{ tab }}
    </button>
  </nav>

  <KeepAlive>
    <component :is="currenTabComponent" />
  </KeepAlive>
</template>

<script>
import home from "./components/Home.vue";
import about from "./components/About.vue";
import post from "./components/Post.vue";

export default {
  components: {
    home,
    post,
    about,
  },
  data() {
    return {
      currentTab: "Home",
      tabs: ["Home", "Post", "About"],
    };
  },
  computed: {
    currenTabComponent() {
      return this.currentTab.toLowerCase();
    },
  },
};
</script>

<style>
body {
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
}
</style>
