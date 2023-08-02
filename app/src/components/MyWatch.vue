<template>
  <h2>Assistindo alteração de uma variável</h2>
  <input type="text" v-model="name" />
  <p>{{ name }}</p>

  <br />

  <h2>Assistindo alteração de um objeto</h2>

  <h3>Nome</h3>
  <input type="text" v-model="user.name" />
  <p>{{ user.name }}</p>

  <h3>Idade</h3>
  <input type="number" v-model="user.age" />
  <p>{{ user.age }}</p>
</template>

<script>
export default {
  name: "MyWatch",

  data() {
    return {
      name: "Name",
      user: {
        name: "Marco",
        age: 19,
      },
    };
  },

  beforeUnmount() {
    console.log("Before unmount");
  },

  unmounted() {
    console.log("Unmounted");
  },

  watch: {
    name(newValue, oldValue) {
      if (newValue.length >= 3) {
        this.select2(newValue, oldValue);
      }
    },
    user: {
      handler() {
        console.log("User alterado!");
      },
      deep: true,
    },
  },

  methods: {
    select2(newValue, oldValue) {
      console.log(`Novo valor: ${newValue}`);
      console.log(`Valor antigo: ${oldValue}`);
    },
  },
};
</script>

<style lang="scss" scoped></style>
