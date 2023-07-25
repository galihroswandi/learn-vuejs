<template>
  <input type="text" v-model="value" />
</template>

<script>
export default {
  props: {
    value: {
      type: String,
    },
  },
  computed: {
    value: {
      get() {
        return this.value;
      },
      set(value) {
        this.$emit("update:value-emit", value);
      },
    },
  },
};
</script>
