<template>
  <!-- <h2>{{ total }}</h2>
  <button @click="addTotalNum">+1</button>

  <br />
  <h2>{{ msg }}</h2>
  <button @click="changeMsg">更改訊息</button> -->

  <br />
  <!-- <h2>Name: {{ object.name }}</h2>
  <button @click="object.name += '～'">加入波浪符號</button> -->
  <!-- <h2>Age: {{ object.age }}</h2> -->
  <h2>salary: {{ object.job.salary.total }} K</h2>
  <!-- <button @click="object.name += '～'">加入波浪符號</button> -->
  <!-- <button @click="object.age++">age + 1</button> -->
  <button @click="object.job.salary.total++">salary +1</button>
</template>

<script>
import { reactive, watch } from 'vue';
export default {
  name: 'app',
  setup() {
    let object = reactive({
      name: 'ken',
      age: 18,
      job: {
        salary: {
          total: 10,
        },
      },
    });

    watch(
      () => object.job,
      (newValue, oldValue) => {
        console.log(`newValue=> ${newValue}`, `oldValue=> ${oldValue}`);
      },
      { deep: true }
    );

    return {
      object,
    };
  },
};
</script>



<style>
</style>
