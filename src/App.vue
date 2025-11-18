<template>
  <h1>채널명 : {{ channel }}</h1>
  <!-- 머스태시 : 콧수염 문법 -->
  <!-- text interpolation 보간법  -->
  <h2>구독자수 : {{ subscribe }}</h2>
  <p>오늘의 행운 숫자 : {{ Math.ceil(Math.random() * 45) }}</p>
  <h1 v-text="channel"></h1>
  <h2 v-text="subscribe"></h2>
  <!-- <h2 v-text="subscribe">123</h2> 오류 -->

  <p v-html="channel2"></p>
  <!-- v-text 에는 html이 표시되어버림 , v-html은 html 문법 적용가능 -->
</template>

<script>
export default {
  data() {
    return {
      channel: "홈페이지 만들기",
      channel2: "<b>홈페이지2 </b>",
      subscribe: 2677,
    };
  },
};
</script>

<style lang="scss" scoped></style>
