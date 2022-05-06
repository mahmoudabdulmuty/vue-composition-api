<template>
  <div>
    <input placeholder="First Name" type="text" v-model="firstName" />
    <input placeholder="Last Name" type="text" v-model="lastName" />
    <h2>
      {{ fullName }}
    </h2>
  </div>
</template>

<script>
import { computed, reactive, toRefs } from 'vue';

export default {
  setup() {
    const formData = reactive({
      firstName: '',
      lastName: '',
    });

    const fullName = computed(() => {
      return `${formData.firstName} ${formData.lastName}`;
    });

    return {
      ...toRefs(formData),
      fullName,
    };
  },
};
</script>

<style scoped></style>
