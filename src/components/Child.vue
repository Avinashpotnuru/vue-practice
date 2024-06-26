<template>
  <div>
    <h1>{{ name }}</h1>
  </div>
</template>

<script>
export default {
  name: "ChildOne",

  inject: ['name'],
};
</script>

<style lang="scss" scoped></style>
