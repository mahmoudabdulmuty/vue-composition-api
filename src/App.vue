<template>
  <div>
    <h2>
      {{ count }}
    </h2>
    <h2>
      {{ firstName }}
    </h2>
    <h2>
      {{ lastName }}
    </h2>
    <button @click="changeName">change Name</button>
    <button @click="increment">Counter</button>
  </div>
</template>

<script>
import { reactive, ref, toRefs } from 'vue';

export default {
  setup() {
    const count = ref(0);
    const increment = () => {
      count.value++;
    };

    const data = reactive({
      firstName: 'Mahmoud',
      lastName: 'Abdulmuty',
    });

    const changeName = () => {
      (data.firstName = 'Moemen'), (data.lastName = 'Yasser');
    };

    return {
      ...toRefs(data),
      count,
      increment,
      changeName,
    };
  },
};
</script>

<style lang="scss" scoped></style>
