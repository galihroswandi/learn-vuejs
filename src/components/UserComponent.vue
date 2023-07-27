<template>
  <div>
    <h1>{{ label }} : {{ users.name }}</h1>
    <h1>{{ description }}</h1>

    <button @click="submit">Submit</button>

    <hr />
    <slot />
  </div>
</template>

<script>
import { toRefs, computed, onMounted } from "vue";

export default {
  props: {
    label: {
      type: String,
      required: true,
      default: "",
    },
    users: {
      type: Object,
      required: true,
      default: () => {},
    },
  },

  setup(props, context) {
    const { label, users } = toRefs(props);
    const { attrs, slots, emit } = context;

    const description = computed(() => {
      return `${label.value} : ${users.value.name}`;
    });

    const submit = () => {
      emit("submit", "ini emit dari user component");
    };

    onMounted(() => {
      console.log({ attrs });
      console.log({ slots });
    });

    return { description, submit };
  },
};
</script>
