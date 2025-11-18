<template>
  <h1 v-if="score >= 90">평점 : A</h1>
  <h1 v-else-if="score >= 80">평점 : B</h1>
  <h1 v-else-if="score >= 70">평점 : C</h1>
  <h1 v-else>평점 : D</h1>
  <h1 v-if="score != 60">이 영역은 v-if에서 관리</h1>
  <h1 v-show="score != 60">이 영역은 v-show에서 관리</h1>
  <!-- v-show는 개발자 도구에서 false라도 확인 가능 -->
  <!-- 자주 변경되면 v-show, 변경 안되면 v-if -->
</template>

<script>
export default {
  data() {
    return {
      channel: "홈페이지 만들기",
      score: 60,
      subscribe: 2677,
    };
  },
};
</script>

<style lang="scss" scoped></style>
