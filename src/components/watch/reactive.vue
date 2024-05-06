<template>
  <div class="reactive">
    <p>reactive-引用数据类型watch</p>
    <div>{{ person.age }}</div>
    <button @click="changeAge">修改age</button>
    <button @click="changePerson">修改整个person</button>
  </div>
</template>
<script setup>
import { reactive, watch } from 'vue'

let person = reactive({
  age: 18
})

/**
 * 1. 隐式开启深度监听deep， 无法断开监听， 也无法将deep设置为false
 * 2. reactive定义的引用数据类型，能监听到某个属性例如age的变化
 */
watch(person, (newVal, oldVal) => {
  console.log(newVal, oldVal)
})

function changeAge () {
  person.age += 1
}

function changePerson () {
  Object.assign(person, { age: 25 })
}
</script>