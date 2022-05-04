<template>
  <h1>{{ person.name }}</h1>
  <h1>{{ person.age }}</h1>
  <button @click="emitMsg">emitMsg</button>
  <slot></slot>
</template>

<script>
import { reactive } from 'vue';
export default {
  name: 'app',
  props: {
    msg: {
      type: String,
    },
    general: {
      type: String,
    },
  },
  emits: ['emitFatherMsg'],
  setup(props, context) {
    console.log('props', props);
    console.log('context', context);
    console.log('context', context.slots);
    let person = reactive({
      name: 'ken',
      age: '12',
    });
    function emitMsg() {
      console.log(props);
      context.emit('emitFatherMsg', 'testMsg');
    }

    return {
      person,
      emitMsg,
    };
  },
};
</script>



<style>
</style>
