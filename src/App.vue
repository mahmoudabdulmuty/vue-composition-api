<template>
  <h2>username is {{ firstName }}</h2>
  <h2>{{ greet }}</h2>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const firstName = ref('Mahmoud');
    const greet = `Hello ${firstName.value}`;
    return {
      firstName,
      greet,
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
