<template>
  <h1>Todolist</h1>

  <ul>
    <li v-for="(todo, index) in todos" :key="todo.id">
      <span>{{ index + 1 }}.{{ todo.title }}</span>
      <button @click="deleteTodo(todo.id)">刪除</button>
    </li>
  </ul>
  <input type="text" placeholder="學習目標" v-model="newTodo" />
  <button @click="createTodo()">請輸入事項</button>
</template>

<style scoped>
</style>

<script>
export default {
  name: "Todolist",
  data() {
    return {
      newTodo: "",
      todos: [
        { id: "todo-1", title: "學習Vue.hs" },
        { id: "todo-2", title: "學習A.hs" },
      ],
    };
  },
  methods: {
    deleteTodo(id) {
      this.todos = this.todos.filter((todo) => todo.id !== id);
    },
    createTodo() {
      const todoTitle = this.newTodo;
      const todo = {
        title: todoTitle,
        id: "todo-" + this.todos.length + 1,
      };
      this.todos.push(todo);
      this.newTodo = "";
    },
  },
};
</script>



