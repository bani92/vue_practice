<template>
  <div>
    <p>cnt : {{ cnt }}</p>
    <p>old : {{ obj.oldValue }} / new : {{ obj.newValue }}</p>
    <button @click="counter">클릭</button>
  </div>
</template>

<script setup>
import { ref, reactive, watch } from "vue";

const cnt = ref(1);
const obj = reactive({
  oldValue: null,
  newValue: null,
});
const counter = () => cnt.value++;

watch(cnt, (newValue, oldValue) => {
  obj.oldValue = oldValue;
  obj.newValue = newValue;
});
</script>

<style lang="scss" scoped></style>
