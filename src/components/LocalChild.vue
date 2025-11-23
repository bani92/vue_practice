<template>
  <div>나는 Child Components 입니다. {{ c }}</div>

  <input type="text" ref="myInput" v-model="c" />
  <button @click="$emit('createPost', c)">부모 이벤트 호출</button>
</template>

<script>
export default {
  data() {
    return {
      c: 5,
    };
  },
};
</script>

<style scoped>
h1 {
  color: blue;
}
p {
  color: skyblue;
}
</style>
