<script setup>
import { ref, onBeforeMount, onMounted, onBeforeUnmount, onUnmounted } from 'vue'

// onBeforeMount(() => {
//   console.log('1: Child Call onBeforeMount');
// });

// onMounted(() => {
//   console.log('2: Child Call onMounted');
// });

onBeforeUnmount(() => {
  console.log('5: Call onBeforeUnmount');
});

onUnmounted(() => {
  console.log('6: Call onUnmounted');
});

</script>

<template>
  <p>Child</p>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
