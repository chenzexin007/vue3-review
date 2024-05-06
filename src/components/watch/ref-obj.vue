<template>
  <div class="ref-obj">
    <p>ref-引用数据类型watch</p>
    <div>{{ person.age }}</div>
    <button @click="changeAge">修改age</button>
    <button @click="changePerson">修改整个person</button>
  </div>
</template>
<script setup>
import { ref, watch } from 'vue'

let person = ref({
  age: 18
})

/**
 * 1. 可以主动断开监听
 * 2. ref定义的引用数据类型，需要开启deep才能监听到某个属性例如age的变化
 * 3. 不开启deep的话，只能监听整个对象.value地址的变化
 */
let stopWatch = watch(person, (newVal, oldVal) => {
  console.log(newVal, oldVal)
  if (newVal.age > 20) {
    stopWatch()
  }
}, {
  deep: true,
  immediate: true
})

function changeAge () {
  person.value.age += 1
}

function changePerson () {
  person.value = { age: 25 }
}
</script>