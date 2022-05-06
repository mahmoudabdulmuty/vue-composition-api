<template>
  <h2>
    username is {{ firstName }}
    {{ lastName }}
  </h2>
  <h2>
    {{ heroName }}
  </h2>
</template>

<script>
import { reactive, toRefs } from 'vue';

export default {
  setup() {
    const data = reactive({
      firstName: 'Mahmoud',
      lastName: 'Abdulmuty',
      heroName: 'Moon Knight',
    });

    setTimeout(() => {
      (data.firstName = 'Mohamed'), (data.lastName = 'Abdullah');
    }, 2000);

    return toRefs(data);
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
