<template>
  <div class="refs">
    <div>姓：{{ firstName }}</div>
    <div>名：{{ lastName }}</div>
    <button @click="changeFirstName">修改姓</button>
    <button @click="changeLastName">修改名</button>
  </div>
</template>
<script setup>
import { reactive, toRefs } from 'vue'

let user = reactive({
  firstName: '张',
  lastName: '三'
})

let { firstName, lastName } = toRefs(user)

function changeFirstName () {
  firstName.value = '王'
}

function changeLastName () {
  lastName.value = '五'
}

</script>