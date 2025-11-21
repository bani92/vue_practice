<template>
  <div>
    <h1>App.Vue</h1>
    <!-- 파스칼 케이스  -->
    <LocalChild />
    <GlobalChild />
  </div>
</template>

<script>
import LocalChild from "./components/LocalChild.vue";
export default {
  components: {
    LocalChild,
  },
};
</script>

<style lang="scss" scoped></style>
