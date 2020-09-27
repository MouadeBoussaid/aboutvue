<template>
  <h1>Todoist wannabe2</h1>
  <form v-on:submit.prevent="addTodo">
    <label>New Todo</label>
    <input v-model="newTodo" name="newTodo" />
    <button>Add Todo</button>
  </form>

  <ul>
    <li v-for="(todo, index) in todosList" v-bind:key="todo.id" class="todo">
      <h3 v-bind:class="{ done: todo.done }" v-on:click="toggleDone(todo)">
        {{ todo.content }}
      </h3>
      <button v-on:click="removeTodo(index)">Remove Todo</button>
    </li>
  </ul>
</template>

<script setup>
// Vue v3 experimental setup tag
import { ref } from "vue";
import { v4 as uuid } from "uuid";

export const newTodo = ref("");
export const todosList = ref([]);

export const addTodo = () => {
  todosList.value.push({
    id: uuid(),
    done: false,
    content: newTodo.value
  });
  newTodo.value = "";
};

export const toggleDone = todo => {
  todo.done = !todo.done;
};

export const removeTodo = index => {
  todosList.value.splice(index, 1);
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
