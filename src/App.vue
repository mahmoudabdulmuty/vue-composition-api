<template>
  <div>
    <h2>
      {{ count }}
    </h2>
    <button @click="increment">Counter</button>
  </div>
</template>

<script>
import { reactive, toRefs } from 'vue';

export default {
  setup() {
    // const count = ref(0);
    const data = reactive({
      count: 0,
    });
    const increment = () => {
      data.count++;
    };
    return {
      ...toRefs(data),
      increment,
    };
  },
};
</script>

<style lang="scss" scoped></style>
