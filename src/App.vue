<template>
  <!--  inline 스타일 > 클래스 스타일 -->
  <div
    class="demo"
    @mouseover="initWidth"
    :style="{ width: myWidth + 'px' }"
  ></div>
  <button @click="incWidth">버튼을 클릭해보세요</button>
</template>

<script>
export default {
  data() {
    return {
      myWidth: 10,
    };
  },
  methods: {
    incWidth: function () {
      this.myWidth += 10;
    },
    initWidth: function () {
      this.myWidth = 10;
    },
  },
};
</script>

<style>
.demo {
  width: 100px;
  height: 100px;
  background-color: blueviolet;
}
</style>
