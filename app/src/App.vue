<template>
  <NavBar>
    <ul class="list">
      <li>
        <h1>Home</h1>
      </li>
      <li>
        <h1>Sobre</h1>
      </li>
    </ul>
    <template v-slot:nomeado>
      <button class="btn">Login</button>
    </template>
  </NavBar>

  <BaseCard />
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import BaseCard from "@/components/BaseCard.vue";
export default {
  name: "App",

  components: {
    NavBar,
    BaseCard,
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
