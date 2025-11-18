<template>
  <ul>
    <li v-for="(item, index) in sports" key:index>{{ index }} {{ item }}</li>
  </ul>
  <p>{{ "count : " + count }}</p>
  <button @click="count++">숫자 증가</button>
  <button @click="count--">숫자 감소</button>
  <button v-on:mouseover="count = 0">0으로 초기화</button>
</template>

<script>
export default {
  data() {
    return {
      sports: ["Baseball", "Football", "Volleyball"],
      count: 0,
    };
  },
};
</script>

<style lang="scss" scoped></style>
