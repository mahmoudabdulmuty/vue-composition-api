<template>
  <div>
    <input placeholder="First Name" type="text" v-model="firstName" />
    <input placeholder="Last Name" type="text" v-model="lastName" />
    <input placeholder="age" type="number" v-model="options.age" />
    <!-- <h2>
      {{ fullName }}
    </h2> -->
  </div>
</template>

<script>
import { reactive, toRefs, watch } from 'vue';

export default {
  setup() {
    // const firstName = ref('');
    // const lastName = ref('');

    const data = reactive({
      firstName: '',
      lastName: '',
      options: {
        age: '',
      },
    });

    watch(
      () => structuredClone(data),
      (newValue, oldValue) => {
        console.log(newValue.options.age);
        console.log(oldValue.options.age);
      }
    );

    return {
      ...toRefs(data),
    };
  },
};
</script>

<style scoped></style>
