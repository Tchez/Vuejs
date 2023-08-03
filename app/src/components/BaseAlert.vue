<template>
  <div :class="alertClass">{{ message }}</div>
</template>

<script>
export default {
  props: {
    type: {
      type: String,
      default: "",
    },
    message: {
      type: String,
      default:
        "Mensagem padrão! Lembre-se de alterar usando a propriedade message",
    },
  },
  computed: {
    alertClass() {
      return ["alert", this.type ? `alert-${this.type}` : ""];
    },
  },
};
</script>

<style scoped>
.alert {
  padding: 5px;
  border-radius: 6px;
  color: gray;
  background-color: yellow;
}

.alert-success {
  background: #42b983;
  color: #fff;
}

.alert-danger {
  background: red;
  color: #fff;
}
</style>
