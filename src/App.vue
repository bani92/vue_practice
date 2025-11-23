<template>
  <div>
    <h1>나는 부모</h1>
    <button @click="ageInc">age++</button>
    <ChildComponent v-bind:name="name" v-bind:age="age" />
  </div>
</template>

<script>
import ChildComponent from "./components/ChildComponent.vue";

export default {
  data() {
    return {
      name: "John",
      age: 30,
    };
  },
  methods: {
    ageInc() {
      this.age++;
    },
  },
  components: {
    ChildComponent,
  },
};
</script>

<style lang="scss" scoped></style>
