<script setup>
import {ref} from 'vue'
const randomNumber = ref(null)
const updateRandomNumber = () => {
  randomNumber.value = Math.random()
}

const counter = ref(0)
const incrementCounter = () => {
  counter.value++
}
</script>

<template>
     <h3>Display a random number</h3>
  <button @click="updateRandomNumber">Get a random number {{ randomNumber }}</button>
  <div v-if="randomNumber">
    <div v-if="randomNumber >= 0.5">number is bigger than 0.5</div>
    <div v-else>number is lower than 0.5</div>
  </div>
</template>