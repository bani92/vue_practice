<template>
  <div>
    <ChildComponent @customEvent="handleCustomEvnet" />
  </div>
</template>

<script setup>
import ChildComponent from "./components/ChildComponent.vue";

const handleCustomEvnet = (message) => {
  console.log("Received event: ", message);
};
</script>

<style lang="scss" scoped></style>
