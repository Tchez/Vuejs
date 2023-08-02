<template>
  <ComputedExample />
  <TodosList />
</template>

<script>
import ComputedExample from "./components/ComputedExample.vue";
import TodosList from "./components/TodosList.vue";
export default {
  name: "App",

  components: {
    ComputedExample,
    TodosList,
  },

  data() {
    return {};
  },

  computed: {},
};
</script>

<style></style>
