<template>
  <div>
    <input placeholder="First Name" type="text" v-model="firstName" />
    <input placeholder="Last Name" type="text" v-model="lastName" />
    <input placeholder="Hero Name" type="text" v-model="heroName" />
  </div>
</template>

<script>
import { reactive, ref, toRefs } from 'vue';

export default {
  setup() {
    const heroName = ref('');
    const fullName = reactive({
      firstName: '',
      lastName: '',
    });

    return {
      heroName,
      ...toRefs(fullName),
    };
  },
};
</script>

<style scoped></style>
