<template>
  <h1>Todoist wannabe3</h1>
  <form @submit.prevent="addTodo">
    <label>New Todo</label>
    <input v-model="newTodo" name="newTodo" />
    <button>Add Todo</button>
  </form>

  <ul>
    <li v-for="(todo, index) in todosList" :key="todo.id" class="todo">
      <h3 :class="{ done: todo.done }" @click="toggleDone(todo)">
        {{ todo.content }}
      </h3>
      <button @click="removeTodo(index)">Remove Todo</button>
    </li>
  </ul>
</template>

<script>
// Vue v2
import { v4 as uuid } from "uuid";

export default {
  data() {
    return {
      newTodo: "",
      todosList: []
    };
  },
  methods: {
    addTodo() {
      this.todosList.push({
        id: uuid(),
        done: false,
        content: this.newTodo
      });
      this.newTodo.value = "";
    },
    toggleDone(todo) {
      todo.done = !todo.done;
    },
    removeTodo(index) {
      this.todosList.splice(index, 1);
    }
  },
  computed: {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
body {
  font-family: sans-serif;
  padding-top: 1em;
  padding-bottom: 1em;
  font-size: 2em;
  width: 80%;
  margin: 0 auto;
}
input,
textarea,
button,
p,
div,
section,
article,
select {
  display: "block";
  width: 100%;
  font-family: sans-serif;
  font-size: 1em;
  margin: 0.5em;
}
.todo {
  cursor: pointer;
}
.done {
  text-decoration: line-through;
}
</style>
