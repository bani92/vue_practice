<template>
  <div>
    <h1>Child component</h1>
    <h2>{{ name }}</h2>
    <h2>{{ age }}</h2>
  </div>
</template>

<script>
export default {
  props: ["name", "age"],
  created() {
    console.log(this.name);
  },
};
</script>

<style lang="scss" scoped></style>
