<template>
  <TodoList />
  <!-- <TodoList2 /> -->
  <!-- <TodoList3 /> -->
</template>

<script>
// Vue v3 with Composition API
import TodoList from "./components/TodoList.vue";
// Vue v3 with experimental setup tag
// import TodoList2 from "./components/TodoList2.vue";
// Vue v2 with Options API
// import TodoList3 from "./components/TodoList3.vue";

export default {
  name: "App",
  components: {
    TodoList
    // TodoList2
    // TodoList3
  }
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
