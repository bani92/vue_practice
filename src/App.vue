<template>
  <div>
    <p>count : {{ count }}</p>
    <p>obj1 : {{ obj1.name }} / {{ obj1.age }}</p>
    <button @click="good">클릭</button>
  </div>
</template>

<script setup>
import { ref, reactive } from "vue";

const count = ref(0);

const obj1 = reactive({
  name: "kim",
  age: 33,
});

const good = () => {
  // count.value++;
  obj1.name = "Lee";
};
</script>

<style lang="scss" scoped></style>
