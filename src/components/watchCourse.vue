<template>
  <h2>{{ total }}</h2>
  <button @click="addTotalNum">+1</button>

  <br />
  <h2>{{ msg }}</h2>
  <button @click="changeMsg">更改訊息</button>
</template>

<script>
import { ref, watch } from 'vue';
export default {
  name: 'app',
  watch: {
    // total(newValue, oldValue) {
    //   console.log(`newValue=> ${newValue}`, `oldValue=> ${oldValue}`);
    // },
    // total: {
    //   handler(newValue, oldValue) {
    //     console.log(`newValue=> ${newValue}`, `oldValue=> ${oldValue}`);
    //   },
    //   immediate: true,
    // },
  },
  setup() {
    let total = ref(0);
    let msg = ref('原始為更改訊息');

    // watch(total, (newValue, oldValue) => {
    //   console.log(`newValue=> ${newValue}`, `oldValue=> ${oldValue}`);
    // });

    // watch(msg, (newValue, oldValue) => {
    //   console.log(`newValue=> ${newValue}`, `oldValue=> ${oldValue}`);
    // });

    watch([total, msg], (newValue, oldValue) => {
      console.log(`newValue=> ${newValue}`, `oldValue=> ${oldValue}`);
    });

    function addTotalNum() {
      total.value++;
    }

    function changeMsg() {
      msg.value = msg.value + '!';
    }

    return {
      total,
      msg,
      addTotalNum,
      changeMsg,
    };
  },
};
</script>



<style>
</style>
