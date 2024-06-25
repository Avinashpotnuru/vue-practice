<template lang="">
  <div>
    <button @click="changeToggle">toggle</button>

    <template v-if="isToggle">
      <h1>{{ name }}</h1>
    </template>
    <input v-model="text" placeholder="enter your name" />

    <h1>{{ text }}</h1>

    <h1>{{ text.length }}</h1>

    <template v-for="item in familyData" :key="item">
        <h1>{{item}}</h1>

    </template>
    <h2 v-for="item in familyData" :key="item">{{item}}</h2>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: "avinash",
      isToggle: true,
      text: "",

      familyData: ["gandhi", "pramila rani", "aditya", "avinash", "jessy"],
    };
  },
  methods: {
    changeToggle() {
      this.isToggle = !this.isToggle;
    },

    changeName() {},
  },
};
</script>
<style lang=""></style>
