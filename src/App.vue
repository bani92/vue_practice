<template>
  <div class="container">
    <button @click="isInputMode = true" class="btn btn-primary ms-3 mt-3">데이터 입력</button>
    <button @click="getData" class="btn btn-success ms-3 mt-3">데이터 가져오기</button>
    <div v-show="isInputMode">
      <form autocomplete="off">
        <label class="form-level">Name</label>
        <input type="text" class="form-control" v-model="name">
        <label class="form-level">Email</label>
        <input type="text" class="form-control" v-model="email"></input>
        <button type="button" class="btn btn-success me-3 mt-3" @click="inputData">입력 확인</button>
        <button type="button" class="btn btn-secondary mt-3" @click="isInputMode = false">취소</button>
        
      </form>
    </div>

    <div ref="table"></div>
  </div>
</template>

<script setup>
import axios from "axios";
import { ref } from "vue";

const table = ref(null);
const isInputMode = ref(false);
const name = ref('')
const email = ref('')


const inputData = async () => {
  const res = await axios
    .post("http://localhost:3000/member", {
      name: name.value,
      email: email.value,
    })
    .then((res) => {
      console.log(res);
    });
  name.value = '';
  email.value = '';
  isInputMode.value = false;
  getData();
};

const getData = () => {
  axios.get("http://localhost:3000/member").then((res) => {
    // console.log(res);
    const members = res.data;
    let htmlContent = `<table border="1">
      <tr>
         <th>id</th>
         <th>Name</th>
         <th>Email</th>
      </tr>
      `;
    members.forEach((member) => {
      htmlContent += `
        <tr>
          <td>${member.id}</td>
          <td>${member.name}</td>
          <td>${member.email}</td>
        </tr>
      `;
    });
    htmlContent += "</table>";
    table.value.innerHTML = htmlContent;
  });
};
</script>

<style lang="scss" scoped></style>
