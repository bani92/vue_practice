<template>
  <ul id="todo-list">
    <li
      v-for="(item, index) in todoList"
      :key="index"
      :class="{ completed: item.completed }"
    >
      {{ item.msg }}
      <button type="button" @click="todoUpdate(item.id)">Delete</button>
    </li>
  </ul>
</template>

<script>
export default {
  props: ["todoList"],
  methods: {
    todoUpdate(id) {
      this.$emit("todoUpdate", id);
    },
  },
};
</script>

<style lang="scss" scoped></style>
