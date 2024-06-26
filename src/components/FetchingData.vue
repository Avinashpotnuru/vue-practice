<template>
  <div v-if="isLoading">
    <h1>loading....</h1>
  </div>
  <div v-else-if="errorMessage">
    <h1>{{ errorMessage }}</h1>
  </div>

  <div v-else>
    <div v-for="item in dataFromBackend" :key="item.id">
        <p1>{{item.title}}</p1>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "FetchingData",
  data() {
    return {
      dataFromBackend: [],
      isLoading: false,
      errorMessage: "",
    };
  },
  created() {
    this.getPosts();
    console.log(this.dataFromBackend)
  },
  methods: {
    getPosts() {
        this.isLoading = true;
        this.errorMessage = "";
      axios
        .get("https://jsonplaceholder.typicode.com/todos")
        .then((res) => {
         
          if (res.status === 200) {
            console.log(res);
            this.isLoading = false;

            return res.data;
          }
        })
        .then((data) => (this.dataFromBackend = data))
        .catch((error) => {
          this.errorMessage =  error.message;
          this.isLoading = false;
        });
    },
  },
};
</script>

<style scoped></style>
