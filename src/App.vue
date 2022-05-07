<template>
  <div>
    <input type="text" placeholder="first name" v-model="fName" />
    <input type="text" placeholder="last name" v-model="lName" />
    <ChildComponent :fName="fName" :lName="lName" />
  </div>
</template>

<script setup>
import { ref } from 'vue';
import ChildComponent from './components/child-component.vue';

const fName = ref('');
const lName = ref('');
</script>

<style lang="scss" scoped></style>
