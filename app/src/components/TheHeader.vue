<template>
  <div>
    <div v-for="(obj, index) in array" v-bind:key="index">
      {{ obj.name }}
    </div>
  </div>
</template>

<script>
export default {
  name: "TheHeader",
  data() {
    return {
      array: [{ name: "Marco" }, { name: "Antônio" }, { name: "Martins" }],
    };
  },
};
</script>

<style>
.header {
  background-color: #000;
  color: #fff;
}
</style>
