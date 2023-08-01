<template>
  <h1>Input de Nome</h1>
  <label for="input">Nome</label>
  <br />
  <input v-model="name" id="input" type="text" />
  <br />
  {{ name }}
  <div>
    <label>Sports</label>
    <br />
    <select v-model="sports">
      <option value="">Escolha uma opção</option>
      <option value="futebol">futebol</option>
      <option value="vôlei">vôlei</option>
      <option value="basquete">basquete</option>
    </select>
    {{ sports }}
  </div>

  <br />

  <div>
    <label>Newsletter</label>
    <br />
    <input type="radio" value="sim" v-model="newsletter" /> Sim
    <br />
    <input type="radio" value="não" v-model="newsletter" /> Não
    <br />
    {{ newsletter }}
  </div>

  <br />

  <div>
    <label>Contrato</label>
    <br />
    <input type="checkbox" v-model="contract" /> Aceita nossos termos?
    <br />
    {{ contract }}
  </div>

  <br />

  <div>
    <label>Cores legais</label>
    <br />
    <input type="checkbox" v-model="colors" value="azul" /> Azul
    <br />
    <input type="checkbox" v-model="colors" value="vermelho" /> Vermelho
    <br />
    <input type="checkbox" v-model="colors" value="verde" /> Verde
    <br />
    {{ colors }}
  </div>
</template>

<script>
export default {
  name: "MyInput",
  data() {
    return {
      name: "",
      sports: "",
      newsletter: "",
      contract: false,
      colors: [],
    };
  },
};
</script>

<style lang="scss" scoped></style>
