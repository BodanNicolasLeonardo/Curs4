<script setup>
import { onMounted, onUpdated } from 'vue'

onMounted(() => {
  console.log('App Mounted')
})

onUpdated(() => {
  console.log('App updated')
})

import { ref } from 'vue'
import YouDidIt from './components/YouDidIt.vue'
const link = ref("https://emanuel.ro")

const randomNumber = ref(null)
const updateRandomNumber = () => {
  randomNumber.value = Math.random()
}

const counter = ref(0)
const incrementCounter = () => {
  counter.value++
}

const students = ref([
  {name: "Miriam", grade:10},
  {name: "Leo", grade:7},
  {name: "Ana", grade:6},
  {name: "Emanuel", grade:8}
  ])
</script>


<template>
  <YouDidIt>

  </YouDidIt>
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
  <hr>
 
   <h3> Bootstrap Icons <i class="bi bi-airplane"></i></h3>
  <hr>
  <h3>Test v-for</h3>
  <ul>
    <li v-for ="(student, index) of students" :key="index">
      Name: {{student.name}}, Grade: {{ student.grade }}
    </li>
  </ul>
</template>

<style scoped>
@import "bootstrap-icons";
/*@import "tailwindcss";*/
</style>