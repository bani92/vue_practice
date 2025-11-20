<template>
  <div style="padding: 20px;">
    <h1>현재 변수 값: {{ myText }}</h1>
    <hr />

    <h3>1. v-bind (:value) - 짝사랑</h3>
    <p>여기에 글을 써도 위쪽 '변수 값'은 안 변해요!</p>
    <input :value="myText" style="padding: 5px;"></input>

    <br /><br />

    <h3>2. v-model - 서로 사랑</h3>
    <p>여기에 글을 쓰면 '변수 값'이 실시간으로 변해요</p>
    <input v-model="myText" style="padding: 5px;"></input>
  </div>
</template>

<script>
export default {
  data() {
    return {
      myText: "초기값"
    }
  }
}
</script>

<style lang="scss" scoped>

</style>