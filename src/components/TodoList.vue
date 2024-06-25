<template>
  <div>
    <h1>todo</h1>

    <form @submit.prevent="addTodo">
      <input v-model="todo" placeholder="Add a new todo" required />
      <button type="submit">Add</button>
    </form>

    <template v-for="(item,index ) in todoList" :key="index">
      <h1>{{ item }}</h1>
      <button @click="deleteTodo(index)">delete</button>
    </template>
  </div>
</template>

<script>
export default {
  name: "TodoListComponent",
  data() {
    return {
      todo: "",
      todoList: [],
    };
  },
  methods: {
    addTodo() {
      console.log(this.todo);
      this.todoList = [...this.todoList, this.todo];
      this.todo = "";
    },
    deleteTodo(id) {
      this.todoList = this.todoList.filter((item,idx) => idx !==id );
    },
  },
};
</script>

<style scoped></style>
