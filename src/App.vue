<template>
  
  <!-- <HelloWorld/>
  <ButtonComponent/> -->
  <TodoList/>
  
  
</template>

<script>


import TodoList from './components/TodoList.vue';




export default {
  name: 'App',
  components: {
    // HelloWorld,
    // ButtonComponent,
    TodoList
    
  }
}
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
