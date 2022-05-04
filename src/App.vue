<template>
  <Children @emitFatherMsg="emitFatherMsg" :msg="data.msg" :general="data.general"></Children>
</template>

<script>
import { reactive } from '@vue/reactivity';
import Children from './components/Child.vue';
export default {
  name: 'app',
  components: { Children },
  setup() {
    let data = reactive({
      msg: 'hello',
      general: 'boy',
    });

    function emitFatherMsg() {
      alert('emitFatherMsg');
    }

    return {
      data,
      emitFatherMsg,
    };
  },
};
</script>



<style>
</style>
