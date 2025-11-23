<template>
  <div>
    <h1>안녕하세요.</h1>
    <FirstChild />
  </div>
</template>

<script>
import FirstChild from "./components/FirstChild.vue";

export default {
  data() {
    return {
      gift: "장난감",
    };
  },
  components: {
    FirstChild,
  },
  provide() {
    return {
      gift: this.gift,
    };
  },
};
</script>

<style scoped>
h1 {
  color: red;
}
span {
  margin-left: 20px;
}
</style>
