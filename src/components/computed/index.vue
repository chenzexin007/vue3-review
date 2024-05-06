<template>
  <div class="refs">
    <div>姓：{{ firstName }}</div>
    <div>名：{{ lastName }}</div>
    <div>
      全名：{{ fullName }}
    </div>
    <button @click="changeFirstName">修改姓</button>
  </div>
</template>
<script setup>
import { reactive, toRefs, computed } from 'vue'

let user = reactive({
  firstName: '张',
  lastName: '三'
})

let { firstName, lastName } = toRefs(user)

function changeFirstName () {
  firstName.value = '王'
  console.log(user, firstName, lastName, fullName)
}

function changeLastName () {
  lastName.value = '五'
}

let fullName = computed(() => {
  return firstName.value + '-' + lastName.value
})

</script>