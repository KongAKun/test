<script lang="ts" setup>
import axios from 'axios';
import HelloWorld from './components/HelloWorld.vue';
import { ref, watchEffect } from 'vue';
let msg = ref("");
watchEffect(() => {
  console.log(msg.value);
});
const cha = () => {
  msg.value = "kongaokun";
}
const cli = () => {
  axios.post('https://www.baidu.com', {
    name: 'John Doe',
    age: 30,
    email: 'johndoe@example.com'
  });
}
</script>
<template>
  <input type="text" v-model="msg">
  <button @click="cha">改变</button>
  <HelloWorld :title="'kong'">
    <template v-slot>孔傲坤</template>
  </HelloWorld>
  <HelloWorld :title="'ao'" />
  <HelloWorld :title="'kun'" />
  <form @submit.prevent="cli">
    <input type="text">
    <input type="submit" value="Submit">
  </form>
</template>
<style lang="less" scoped></style>