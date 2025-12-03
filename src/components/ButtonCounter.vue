<template>
  <div>버튼 카운트 컴포넌트입니다.</div>
  <p>title : {{ title }}</p>
  <p>Cont : {{ mainCont }}</p>
</template>

<script setup>
import { onMounted, ref } from "vue";

// const props = defineProps(["title", "mainCont"]);

// const props = defineProps({
//   title: String,
//   mainCont: String,
// });

const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  mainCont: {
    type: String,
    required: true,
  },
});
const title = ref("");
const cont = ref("");
onMounted(() => {
  title.value = props.title;
  cont.value = props.mainCont;
});
</script>

<style lang="scss" scoped></style>
