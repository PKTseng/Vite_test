<template>
  <button @click="showStatus = !showStatus">顯示/隱藏</button>
  <LifeCycle v-if="showStatus" />
</template>

<script>
import LifeCycle from './components/lifeCycle.vue';

import { ref } from 'vue';
export default {
  name: 'app',
  components: { LifeCycle },
  setup() {
    let showStatus = ref(true);

    return { showStatus };
  },
};
</script>



<style>
</style>
