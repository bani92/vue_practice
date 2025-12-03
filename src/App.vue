<template>
  <div>
    <p>watchEffect</p>
    <p>count : {{ count }}</p>
    <p>name : {{ name }}</p>
    <button @click="counter">클릭</button>
    <button @click="updateName">이름변경</button>
  </div>
</template>

<script setup>
import { ref, watchEffect } from "vue";
const count = ref(1);
const name = ref("홍길동");

const counter = () => count.value++;
const updateName = () =>
  (name.value = name.value == "홍길동" ? "전우치" : "홍길동");
watchEffect(() => {
  console.log(`Count는 ${count.value} 입니다. 이름은 ${name.value} 입니다.`);
});
</script>

<style lang="scss" scoped></style>
