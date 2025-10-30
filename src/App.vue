<script setup>
import { onMounted, onUpdated } from 'vue'


onMounted(() => {
  console.log('App Mounted')
})

onUpdated(() => {
  console.log('App updated')
})

import { ref } from 'vue'
const message = ref("Hello from vue")
const link = ref("https://emanuel.ro")

const ClickHandler = () => {
  message.value = "Button clicked"
}

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
  <h1>You did it!</h1>
  <button @click="ClickHandler">Click me</button>
  <p>
    {{ message }}
  </p>
  <br>
  <input type="text" @change="console.log('text changed')"
    @input="console.log('you have typed: ' + $event.target.value)" @keydown="console.log('you pressed: ' + $event.key)">
  </input>
  <br>
  <a :href="link" target="_blank">Visit emanuel Website</a>
  <br></br>
  <hr>
  <br></br>
  <h3>Display a random number</h3>
  <button @click="updateRandomNumber">Get a random number {{ randomNumber }}</button>
  <div v-if="randomNumber">
    <div v-if="randomNumber >= 0.5">number is bigger than 0.5</div>
    <div v-else>number is lower than 0.5</div>
  </div>

  <br></br>
  <hr>
  <h3>Counter</h3>
  <button @click="counter++">Increment v1</button>
  <button @click="counter++">Increment v2</button>

  <div>{{ counter }}</div>
</template>

<style scoped></style>