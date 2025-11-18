<template>
  <div>
    <p>{{ num }}</p>
    <!-- 보간법일때는 {{ increment() }} -->
    <!-- v-on 디렉토리일때는 @click= increment -->
    <button @click="increment">Increment number</button>
    <button v-on:click="decrement">Decrement number</button>
    <button @click.once="createAlert">알림</button>

    <input type="text" @keydown.s="getKey"></input>"
    <span>{{  kValue }}</span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: 0,
      click_yes: true,
      kValue: "",
    };
  },
  methods: {
    getKey(e) {
      this.kValue = e.key;
    },
    increment() {
      this.num++;
    },
    decrement() {
      this.num--;
    },
    createAlert() {
      alert("경고창이 떴습니다.");
    },
  },
};
</script>

<style lang="scss" scoped></style>
