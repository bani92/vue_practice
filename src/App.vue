<template>
  <div>
    <!-- <form v-on:submit.prevent="addItem"> -->
      <form>
      <p>품목 : <input type="text" required v-model="itemName"></input></p>
      <p>수량 : <select v-model="itemCnt">
        <option value="1">1개</option>
        <option value="2">2개</option>
        <option value="3">3개</option>
        <option value="4">4개</option>
        <option value="5">5개</option>
      </select></p>
      <button v-on:click.prevent="btnAddItem">상품추가</button>
    </form>
    <p> 구입할 품목 : </p>
    <ul>
      <li v-for="item in sList">{{ item.name }} ({{ item.cnt }}개)</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      itemName: null,
      itemCnt: 1,
      sList: [
        { name : '감귤', cnt: 2}
      ]
    }
  },
  methods: {
    addItem() {
      let item = {
        name: this.itemName,
        cnt : this.itemCnt,
      }
      this.sList.push(item);
      this.itemName = null;
      this.itemCnt = 1
    },
    btnAddItem() {
       let item = {
        name: this.itemName,
        cnt : this.itemCnt,
      }
      this.sList.push(item);
      this.itemName = null;
      this.itemCnt = 1
    }
  }
}
</script>

<style lang="scss" scoped>

</style>