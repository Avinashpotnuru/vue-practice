<template>
  <!-- <HelloWorld/>
  <ButtonComponent/> -->
  <!-- <TodoList />

  <ChildOne />
  <input type="text" v-model="username" placeholder="write" />
  <Card title="avinash"/>
  <Card><h3>hello </h3></Card> -->
  <FetchingData/>
</template>

<script>
// import TodoList from "./components/TodoList.vue";
// import ChildOne from "./components/Child.vue";
// import Card from "./components/Card.vue";
import FetchingData from "./components/FetchingData.vue"

export default {
  name: "App",
  data() {
    return {
      username: "",
    };
  },
  components: {
    // HelloWorld,
    // ButtonComponent,
    // TodoList,
    // ChildOne,
    // Card,
    FetchingData
  },
  provide() {
    return {
      name: this.username,
      

    }

   
  },
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
