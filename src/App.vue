<template>
  <div>
    <p>Count : {{ count }}</p>
    <button @click="increment">Increment</button>
    <p>{{ y }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
      y: "짝수",
    };
  },
  methods: {
    increment() {
      this.count++;
    },
  },
  watch: {
    count(newVal, oldVal) {
      console.log(`Count changed from ${oldVal} to ${newVal}`);
      if (newVal % 2 === 0) {
        this.y = "짝수";
      } else {
        this.y = "홀수";
      }
    },
  },
};
</script>

<style lang="scss" scoped></style>
