<template>
  <h1>{{ name }}</h1>
  <h1>{{ age }}</h1>
  <button type="button" @click="changeInfo">更改訊息</button>
</template>

<script>
import { ref } from 'vue';
export default {
  name: 'app',
  setup() {
    let name = ref('ken');
    let age = ref('10');

    function changeInfo() {
      name.value = 'kevin';
      age.value = '20';
      console.log(name);
      console.log(age);
    }

    return {
      name,
      age,
      changeInfo,
    };
  },
};
</script>



<style>
</style>
