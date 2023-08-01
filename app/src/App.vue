<template>
  <TheHeader v-if="showHeader" />

  <div v-show="showName">
    Nome: {{ firstName }}
    <br />
    Sobrenome: {{ lastName }}
  </div>

  <div v-if="accessLevel === 'adm'">adm</div>
  <div v-else-if="accessLevel === 'mrk'">marketing</div>
  <div v-else>user</div>

  <MyInput />
</template>

<script>
import MyInput from "./components/MyInput.vue";
import TheHeader from "./components/TheHeader.vue";

export default {
  name: "App",
  components: {
    TheHeader,
    MyInput,
  },
  data() {
    return {
      showHeader: true,
      firstName: "Marco Antônio",
      lastName: "Martins",
      showName: false,
      accessLevel: "mrk",
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
