<template>
  <h2>
    username is {{ data.firstName }}
    {{ data.lastName }}
  </h2>
  <h2>
    {{ greet }}
    {{ data.heroName }}
  </h2>
</template>

<script>
import { reactive, ref } from 'vue';

export default {
  setup() {
    const firstName = ref('Mahmoud');
    const greet = `Hello ${firstName.value}`;

    const data = reactive({
      firstName: 'Mahmoud',
      lastName: 'Abdulmuty',
      heroName: 'Moon Knight',
    });

    return {
      firstName,
      greet,
      data,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
