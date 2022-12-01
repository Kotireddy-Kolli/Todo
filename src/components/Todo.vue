<template>
  <div>
    <div className="header">
      <h3>Todo App</h3>
    </div>
    <div className="user-todo-item">
      <label for="currentTodo">NewTodo</label>
      <input type="text" v-model="currentTodo" id="currentTodo" />
      <button @click="todo.push(currentTodo)">AddNew Todo</button>
    </div>
    <h3>Todo Items</h3>
    <div className="displayTodo">
      <p v-for="(item, index) in todo" :key="index">{{ item }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Todo",
  data() {
    return {
      currentTodo: "",
      todo: [],
    };
  },
};
</script>

<style>
</style>