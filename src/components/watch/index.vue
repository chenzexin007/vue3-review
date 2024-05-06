<template>
  <div class="watch">
    <ref-base></ref-base>
    <ref-obj></ref-obj>
    <reactive-watch></reactive-watch>
  </div>
</template>
<script setup lang="ts">
import refBase from './ref-base.vue'
import refObj from './ref-obj.vue'
import reactiveWatch from './reactive.vue'
/**
 * watch 用于监听
 * 1.ref、reactive定义的数据
 * 2.函数返回一个值（getter函数）
 * 3.一个包含上述内容的数组
 */
</script>