<template>
  <h1 :class="classVar">Curso Vue 3</h1>
  <div>
    <div v-for="(obj, index) in todos" :key="index">
      <img v-if="obj.imgSrc" :src="obj.imgSrc" :alt="obj.imgAlt" />
      <br />
      {{ obj.title }}
    </div>
  </div>
</template>

<script>
export default {
  name: "TheHeader",
  data() {
    return {
      todos: [
        {
          userId: 1,
          id: 1,
          title: "delectus aut autem",
          completed: false,
          imgSrc: "https://via.placeholder.com/150",
          imgAlt: "Foto de exemplo",
        },
        {
          userId: 2,
          id: 2,
          title: "quis ut nam facilist et officia qui",
          completed: false,
          imgSrc: "https://via.placeholder.com/151",
          imgAlt: "Foto de exemplo",
        },
        {
          userId: 3,
          id: 3,
          title: "lorem ipsum dolor sit amet",
          completed: false,
        },
      ],
      classVar: "title",
    };
  },
};
</script>

<style>
.title {
  font-size: 20px;
  color: blue;
}
.header {
  background-color: #000;
  color: #fff;
}
</style>
