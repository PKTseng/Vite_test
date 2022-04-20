<template>
  <h1>{{ person.name }}</h1>
  <h1>{{ person.age }}</h1>

  <h2>{{ person.job.type }}</h2>
  <h2>{{ person.job.salary }}</h2>

  <h2>{{ person.jobList }}</h2>
  <button type="button" @click="changeInfo">更改訊息</button>
</template>

<script>
import { reactive, ref } from 'vue';
export default {
  name: 'app',
  setup() {
    let person = reactive({
      name: 'ken',
      age: '12',

      job: {
        type: 'frontend',
        salary: '3k',
      },

      jobList: ['frontend', 'backend', 'devOps'],
    });

    function changeInfo() {
      person.name = 'kevin';
      person.age = '20';
      person.job.type = 'devOPssss';
      person.job.salary = '200000';

      person.jobList[0] = 'UI/UX';
    }

    return {
      person,
      changeInfo,
    };
  },
};
</script>



<style>
</style>
