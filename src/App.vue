<template>
  <!-- <parent></parent> -->
  <!-- <reactive-test></reactive-test> -->
  <!-- <refs-test></refs-test> -->
  <!-- <computed-test></computed-test> -->
  <watch-test></watch-test>
</template>
<script setup lang="ts">
// import reactiveTest from './components/reactive-test.vue'
// import refsTest from './components/refs/index.vue'
// import computedTest from './components/computed/index.vue'
import watchTest from './components/watch/index.vue'
</script>

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
