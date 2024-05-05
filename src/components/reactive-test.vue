<template>
  <div class="reactive-test">
    <div>{{ car.name }}价格: {{ car.price }}w</div>
    <button @click="changeCarPrice">修改汽车价格</button>
    <div>
      <div v-for="(game, index) in games" :key="index">{{ game.name }}</div>
    </div>
    <button @click="changeFirstGameName">修改第一个游戏名</button>  
  </div>
</template>
<script lang='ts' setup>
import { reactive } from 'vue'
let car = reactive({
  name: '小米su7',
  price: 100
})

let games = reactive([
  { name: '飞车' },
  { name: 'cf' },
  { name: '王者' }
])

function changeCarPrice () {
  car.price += 10
}

function changeFirstGameName () {
  games[0].name = '土豆英雄'
}
</script>