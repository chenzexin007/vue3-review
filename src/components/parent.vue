<template>
  <div class='parent'>
    <span>姓名： {{ name }}</span>
    <span>年龄： {{ age }}</span>
    <button @click='changeName'>修改名称</button>
    <button @click='changeAge'>修改年龄</button>
  </div>
</template>
<script setup lang='ts' name='parent123'>
import { ref } from 'vue'
let name = ref('张三')
let age = ref(18)

function changeName () {
  name.value += 1
}

function changeAge () {
  age.value += 1
}

</script>
<style scoped>

</style>