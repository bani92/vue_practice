<template>
  <div>
    <button @click="handleClick">Click me</button>
  </div>
</template>

<script setup>
import { defineEmits } from "vue";

const emit = defineEmits(["customEvent"]);
const handleClick = () => {
  emit("customEvent", "Button clicked!");
};
</script>

<style lang="scss" scoped></style>
