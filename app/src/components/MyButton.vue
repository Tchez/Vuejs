<template>
  <button @click="click">Botão</button>
  <br />
  <div @mouseover="onMouseover">Houver {{ hoverColor }}</div>
  <br />
  <div @mouseout="onMouseout">Houver {{ hoverColor }}</div>
  <br />
  <form action="https://google.com" @submit.prevent="onSubmit">
    <input type="text" @keyup="onKeyup" />
    <input type="text" @keyup.enter="onKeyupEnter" />
    <button type="submit">Enviar</button>
  </form>
</template>

<script>
export default {
  name: "MyButton",
  data() {
    return {
      hoverColor: "black",
    };
  },
  methods: {
    click() {
      alert("Clicou!");
    },
    onMouseover() {
      this.hoverColor == "red"
        ? (this.hoverColor = "black")
        : (this.hoverColor = "red");
      console.log("Entrou no botão");
    },
    onMouseout() {
      console.log("Saiu do botão");
    },
    onSubmit($event) {
      console.log("Formulário enviado");
      console.log($event);
    },
    onKeyup($event) {
      console.log("Tecla pressionada");
      console.log($event);
    },
    onKeyupEnter() {
      console.log("Enter pressionado!");
    },
  },
};
</script>

<style lang="scss" scoped></style>
