<template>
  <div class="refs">
    <div>姓：{{ firstName }}</div>
    <div>名：{{ lastName }}</div>
    <div>{{ age }}</div>
    <button @click="changeFirstName">修改姓</button>
    <button @click="changeLastName">修改名</button>
  </div>
</template>
<script setup>
import { reactive, toRefs, toRef } from 'vue'

let user = reactive({
  firstName: '张',
  lastName: '三',
  age: 18
})

let { firstName, lastName } = toRefs(user)
let age = toRef(user, 'age')

function changeFirstName () {
  firstName.value = '王'
}

function changeLastName () {
  lastName.value = '五'
}

</script>