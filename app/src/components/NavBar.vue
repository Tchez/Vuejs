<template>
  <header class="header">
    <nav>
      <slot>
        <!-- slot default -->
      </slot>
    </nav>
    <slot name="nomeado" class="nomeado"></slot>
  </header>
  <button v-if="$slots.botao">
    <!--
      Usar v-if="$slots.botao" faz com que só renderize o componente se for passado algum conteúdo
    -->
    <slot name="botao" class="botao"></slot>
  </button>
</template>

<script>
export default {
  mounted() {
    console.log(this.$slots);
  },
};
</script>

<style>
* {
  margin: 0;
}
.header {
  width: 100%;
  height: 4rem;
  background-color: rgb(116, 109, 109);
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-right: 15px;
}
.list {
  list-style: none;
  display: flex;
  justify-content: left;
  gap: 2.5rem;
}
.btn {
  font-size: 14px;
  padding: 6px 12px;
  margin-bottom: 0;
  background-color: transparent;
  border: 0;
  padding-right: 2rem;
  color: rgb(184, 177, 177);
  font-size: large;
}
</style>
