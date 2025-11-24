<template>
  <button class="fancy-btn">
    <slot :buttonName>디폴트 문자</slot>
  </button>
</template>

<script>
export default {
  data() {
    return {
      buttonName: "잘가요",
    };
  },
};
</script>
