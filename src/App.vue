<template>
  <div>
    <h1>Profile</h1>
    <p>Name : {{ obj.name }}</p>
    <p>Age : {{ obj.age }}</p>
    <button @click="updateName">이름 변경</button>
  </div>
</template>

<script setup>
import { ref, watch } from "vue";

const obj = ref({ name: "홍길동", age: 30 });
const updateName = () => (obj.value.name = "도경우");

// 참조객체는 obj의 주소를 담고 있기때문에 주소가 바뀐게 아니라 감지를 못함
// 내부적으로 변경된건 감지 못함
// 감지를 하기위한 조치 deep : true
watch(
  obj,
  (newObj) => {
    console.log("이름 변경을 감지했습니다. 변경된 이름 : " + newObj.name);
  },
  { deep: true }
);
</script>

<style lang="scss" scoped></style>
