<template>
  <input
    type="text"
    :value="value"
    @input="$emit('update:value-emit', $event.target.value)"
  />
</template>

<script>
export default {
  props: ["value"],
};
</script>
