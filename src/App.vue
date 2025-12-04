<template>
  <div>
    <button @click="inputData">데이터 입력</button>
    <button @click="getData">데이터 가져오기</button>

    <div ref="table"></div>
  </div>
</template>

<script setup>
import axios from "axios";
import { ref } from "vue";

const table = ref(null);

const inputData = async () => {
  const res = await axios
    .post("http://localhost:3000/member", {
      name: "kang",
      email: "kang@gmail.com",
    })
    .then((res) => {
      console.log(res);
    });
  console.log("2번쨰");
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
