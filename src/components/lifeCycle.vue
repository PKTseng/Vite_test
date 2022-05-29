<template>
  <h2>{{ total }}</h2>
  <button @click="total++">+1</button>
</template>

<script>
// import { ref, onBeforeMount, onMounted, onBeforeUpdate, onUpdated, onBeforeUnmount, onUnmounted } from 'vue';
import { ref } from 'vue';
export default {
  name: 'lifeCycle',

  setup() {
    let total = ref(10);
    //   // Vue3 lifeCycle
    // console.log('Vue 3 生命週期鉤子 ＝> setup');
    // console.log('Vue 3 的 this ＝>', this);
    // onBeforeMount(() => {
    //   console.log('Vue 3 生命週期鉤子 ＝> onBeforeMount');
    // });
    // onMounted(() => {
    //   console.log('Vue 3 生命週期鉤子 ＝> onMounted');
    // });
    // onBeforeUpdate(() => {
    //   console.log('Vue 3 生命週期鉤子 ＝> onBeforeUpdate');
    // });
    // onUpdated(() => {
    //   console.log('Vue 3 生命週期鉤子 ＝> onUpdated');
    // });
    // onBeforeUnmount(() => {
    //   console.log('Vue 3 生命週期鉤子 ＝> onBeforeUnmount');
    // });
    // onUnmounted(() => {
    //   console.log('Vue 3 生命週期鉤子 ＝> onUnmounted');
    // });
    return { total };
  },

  // Vue2 lifeCycle
  // beforeCreate() {
  //   console.log('Vue 2 生命週期鉤子 ＝> beforeCreate');
  // },
  // created() {
  //   console.log('Vue 2 生命週期鉤子 ＝> created');
  // },
  // beforeMount() {
  //   console.log('Vue 2 生命週期鉤子 ＝> beforeMount');
  // },
  // mounted() {
  //   console.log('Vue 2 生命週期鉤子 ＝> mounted');
  // },
  // beforeUpdate() {
  //   console.log('Vue 2 生命週期鉤子 ＝> beforeUpdate');
  // },
  // updated() {
  //   console.log('Vue 2 生命週期鉤子 ＝> updated');
  // },
  // beforeDestroy() {
  //   console.log('Vue 2 生命週期鉤子 ＝> beforeDestroy');
  // },
  // destroyed() {
  //   console.log('Vue 2 生命週期鉤子 ＝> destroyed');
  // },
};
</script>



<style>
</style>
