<template>
  <TodoList />
  <!-- <TodoList2 /> -->
</template>

<script>
// Vue v2 with Options API
import TodoList from "./components/TodoList.vue";
// Vue v3 with Composition API
// import TodoList2 from "./components/TodoList2.vue";

export default {
  name: "App",
  components: {
    TodoList
    // TodoList2
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
