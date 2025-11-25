<template>
  <div>
    <h1 :class="titleClass">나를 빨강게 만들어 보세요.</h1>
    <button @click="good1">클릭</button>
  </div>
</template>

<script setup>
import { ref } from "vue";

const titleClass = ref("");

const good1 = () => {
  titleClass.value = "title";
};
</script>

<style scoped>
.title {
  color: red;
}
</style>
