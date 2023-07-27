<template>
  <div class="p-5">
    <app-user-component
      :label="label"
      :users="users"
      class="100"
      testingAttrs="testing"
      @submit="handleSubmit"
    >
      <h1>Ini slot</h1>
    </app-user-component>
    <button @click="changeBiodata">Change</button>
  </div>
</template>

<script>
import UserComponent from "./components/UserComponent.vue";
import { ref, watch, reactive } from "vue";

export default {
  components: {
    "app-user-component": UserComponent,
  },

  setup() {
    const label = ref("Biodata");
    const users = reactive({
      name: "Jhon Doe",
      age: 20,
    });

    const changeBiodata = () => {
      users.name = "JHON";
    };

    const handleSubmit = (param) => {
      console.log(param);
    };

    watch(label, (newValue, oldValue) => {
      console.log(newValue, oldValue);
    });

    return { label, users, changeBiodata, handleSubmit };
  },
};
</script>
