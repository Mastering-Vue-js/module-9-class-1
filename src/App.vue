<script setup>
import { ref, onBeforeMount, onMounted, onBeforeUpdate, onUpdated } from 'vue';
import HelloWorld from './components/HelloWorld.vue';

const count = ref(0);
const status = ref(true);

onBeforeMount(() => {
  console.log('1: Call onBeforeMount');
});

onMounted(() => {
  console.log('2: Call onMounted');
});

onBeforeUpdate(() => {
  console.log('3: Call onBeforeUpdate');
});

onUpdated(() => {
  console.log('4: Call onUpdated');
});

// console.log('0: call setup');

</script>

<template>
  <p>Parent</p>
  <div class="card">
    <button type="button" @click="count++">count is {{ count }}</button>
  </div>
  <div class="card">
    <button type="button" @click="status = !status">Toggle Child</button>
  </div>
  <HelloWorld v-if="status"/>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
