<template>
  <h2>Todos em aberto</h2>

  <div v-for="todo in todos" :key="todo.id">
    <div v-if="todo.completed === false">
      <input type="checkbox" v-model="todo.completed" />
      {{ todo.title }}
    </div>
  </div>

  <h2>Todos completas</h2>
  <div v-for="todo in uncompletedTodos" :key="todo.id">
    <input type="checkbox" v-model="todo.completed" />
    {{ todo.title }}
  </div>
</template>

<script>
export default {
  data() {
    return {
      todos: [
        {
          userId: 1,
          id: 1,
          title: "delectus aut autem",
          completed: false,
        },
        {
          userId: 1,
          id: 2,
          title: "quis ut nam facilis et officia qui",
          completed: false,
        },
        {
          userId: 1,
          id: 3,
          title: "fugiat veniam minus",
          completed: false,
        },
        {
          userId: 1,
          id: 4,
          title: "et porro tempora",
          completed: true,
        },
        {
          userId: 1,
          id: 5,
          title:
            "laboriosam mollitia et enim quasi adipisci quia provident illum",
          completed: false,
        },
      ],
    };
  },

  computed: {
    uncompletedTodos() {
      return this.todos.filter((todo) => todo.completed);
    },
  },
};
</script>

<style lang="scss" scoped></style>
