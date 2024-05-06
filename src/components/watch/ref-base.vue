<template>
  <div class="ref-base">
    <p>ref-基础类型watch</p>
    <div>{{ age }}</div>
    <button @click="changeAge">修改age</button>
  </div>
</template>
<script setup>
import { ref, watch } from 'vue'

let age = ref(18)

// 可以主动断开监听
let stopWatch = watch(age, (newVal, oldVal) => {
  console.log(newVal, oldVal)
  if (newVal > 20) {
    stopWatch()
  }
})

function changeAge () {
  age.value += 1
}
</script>