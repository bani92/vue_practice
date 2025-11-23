<template>
  <div>
    <h1>나는 부모 컴포넌트 ({{ c }})</h1>
    <!-- 자식 컴포넌트에서 emit으로 정의를 한다 -->
    <!-- 부모 컴포넌트에서는 자식컴포넌트를 쓰고 있는 요소에 @text 적은 후 함수를 정의한다. -->
    <LocalChild @create-post="callFunction" />
  </div>
</template>

<script>
import LocalChild from "./components/LocalChild.vue";

export default {
  data() {
    return {
      c: 0,
    };
  },

  components: {
    LocalChild,
  },
  methods: {
    callFunction(var1) {
      console.log("자식 컴포넌트에서 보낸 이벤트를 수신했어요" + var1);
      this.c = var1;
    },
  },
};
</script>

<style lang="scss" scoped></style>
