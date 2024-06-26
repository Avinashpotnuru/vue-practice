<template>
  <h1 :class="headingClass" id="header">{{ message }}</h1>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Header",
  data() {
    return {
      message: "Hello, world!",
      headingClass: "heading"
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.heading {
  background-color: red;
}
</style>
