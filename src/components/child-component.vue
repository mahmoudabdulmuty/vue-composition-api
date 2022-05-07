<template>
  <div>Hello {{ fullName }}</div>
</template>

<script setup>
import { computed } from 'vue';

const props = defineProps({
  fName: String,
  lName: String,
});
const fullName = computed(() => {
  return `${props.fName} ${props.lName}`;
});
</script>

<style lang="scss" scoped></style>
