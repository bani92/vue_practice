<template>
  <h1>나는 App.vue</h1>
  <MainLayout>
    <template v-slot:header>
      <h1>Header</h1>
    </template>
    <template #contents>
      <h1>Contents</h1>
    </template>
    <template v-slot:footer>
      <h1>Footer</h1>
    </template>
  </MainLayout>

  <FancyButton v-slot="{ buttonName }"> {{ buttonName }} </FancyButton>
</template>

<script>
import FancyButton from "./components/FancyButton.vue";
import MainLayout from "./components/MainLayout.vue";
export default {
  data() {
    return {
      buttonName: "클릭클릭",
    };
  },
  components: {
    FancyButton,
    MainLayout,
  },
};
</script>

<style scoped></style>
