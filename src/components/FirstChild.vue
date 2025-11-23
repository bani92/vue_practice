<template>
  <div>
    <h1>자식 컴포넌트</h1>
    반가워요. 저는 자식 컴포넌트입니다
    <SecondChild />
  </div>
</template>

<script>
import SecondChild from "./SecondChild.vue";

export default {
  components: {
    SecondChild,
  },
};
</script>

<style scoped>
h1 {
  color: blue;
}
div {
  width: 400px;
  height: 300px;
  border: 1px solid red;
}
</style>
