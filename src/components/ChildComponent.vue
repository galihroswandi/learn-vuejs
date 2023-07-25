<template>
  <header>Header</header>
  <slot :data="title" />
  <main>Kontent</main>
  <slot name="main" :data="content" />
  <footer>Footer</footer>
  <slot name="footer" :data="footer" />
</template>

<script>
export default {
  data() {
    return {
      title: "This is title",
      content: "This is content",
      footer: "This is footer",
    };
  },
};
</script>
