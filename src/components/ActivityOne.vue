<script setup>
import { ref } from "vue";
//  const ✅
//  let ✅
// @click ✅
// function ✅
let number = ref(0);

function increment(num) {
  number.value += num;
}

function decrement(num) {
  number.value-=num;
}

</script>

<template>
  <div class="number">{{ number }}</div>
  <div class="wrapper">
    <button @click="increment(1)">Increment</button>
    <button @click="decrement(1)">Decrement</button>

    <button @click="increment(2)">Increment</button>
    <button @click="decrement(2)">Decrement</button>

    <button @click="increment(3)">Increment</button>
    <button @click="decrement(3)">Decrement</button>

  </div>
</template>

<style>
.number {
  color: white;
  font-size: 50px;
  font-weight: bold;
  margin-bottom: 20px;
  text-align: center;
  padding: 10px;
  background-color: green;
}

.wrapper {
  display: flex;
  grid-gap: 40px;
}
</style>
