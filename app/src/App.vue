<template>
  <button @click="showMyWatch = !showMyWatch">Toggle MyWatch</button>
  <br />
  <MyWatch v-if="showMyWatch" />
</template>

<script>
import MyWatch from "./components/MyWatch.vue";
export default {
  name: "App",

  components: {
    MyWatch,
  },

  data() {
    return {
      variavel: "carregou!",
      showMyWatch: false,
    };
  },

  beforeUpdate() {
    console.log("Before update");
    console.log("Variável:", this.variavel);
    console.log("DOM:", this.$el);
  },

  updated() {
    console.log("Updated");
    console.log("Variável:", this.variavel);
    console.log("DOM:", this.$el);
  },

  beforeCreate() {
    console.log("Before create");
    console.log("Variável:", this.variavel);
    console.log("DOM:", this.$el);
  },

  created() {
    console.log("Created");
    console.log("Variável:", this.variavel);
    console.log("DOM:", this.$el);
  },

  beforeMount() {
    console.log("Before mount");
    console.log("Variável:", this.variavel);
    console.log("DOM:", this.$el);
  },

  mounted() {
    console.log("Mounted");
    console.log("Variável:", this.variavel);
    console.log("DOM:", this.$el);
  },

  watch: {},

  computed: {},

  methods: {},
};
</script>

<style></style>
