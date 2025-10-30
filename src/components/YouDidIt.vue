<script setup>
import { ref } from 'vue'
const message = ref("Hello from vue")


const ClickHandler = () => {
  message.value = "Button clicked"
}
</script>

<template>
    <h1>You did it!</h1>
  <button @click="ClickHandler">Click me</button>

  <h1 class ='text-3xl font-bold underline'>
    Hello World!
  
  <i class ="bi bi-brightness-high" ></i>
  </h1>
  <p>
    {{ message }}
  </p>
  <br>
  <input type="text" @change="console.log('text changed')"
    @input="console.log('you have typed: ' + $event.target.value)" @keydown="console.log('you pressed: ' + $event.key)">
    </template>