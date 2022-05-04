<template>
  firstName：<input type="text" v-model="person.firstName" />
  <br />
  lastName：<input type="text" v-model="person.lastName" />
  <br />
  fullName：<input type="text" v-model="person.fullName" />
</template>

<script>
import { computed, reactive } from 'vue';
export default {
  name: 'app',

  // computed: {
  //   fullName() {
  //     return this.person.firstName + ' - ' + this.person.lastName;
  //   },
  // },

  setup() {
    let person = reactive({
      firstName: 'Tseng',
      lastName: 'ken',
    });

    // let fullName = computed(()=>person.firstName + ' - ' + person.lastName)

    person.fullName = computed({
      get() {
        return person.firstName + ' - ' + person.lastName;
      },
      set(value) {
        [person.firstName, person.lastName] = value.split(' - ');

        // let name = value.split('-');
        // person.firstName = name[0];
        // person.lastName = name[1];
      },
    });

    return {
      person,
    };
  },
};
</script>



<style>
</style>
