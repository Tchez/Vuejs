<template>
  <BaseAlert />
  <BaseAlert type="danger" message="Teste" />
  <BaseAlert type="success" />
</template>

<script>
import BaseAlert from "./components/BaseAlert.vue";
export default {
  name: "App",

  components: {
    BaseAlert,
  },

  data() {
    return {};
  },

  watch: {},

  computed: {},

  methods: {},
};
</script>

<style></style>
