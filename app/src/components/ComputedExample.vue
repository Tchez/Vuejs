<template>
  <div>
    {{ fullName }}
  </div>
</template>

<script>
export default {
  name: "ComputedExample",

  data() {
    return {
      user: {
        first_name: "Marco",
        last_name: "Polo",
      },
    };
  },

  computed: {
    fullName() {
      return `Nome completo: ${this.user.first_name} ${this.user.last_name}`;
    },
  },
};
</script>

<style lang="scss" scoped></style>
