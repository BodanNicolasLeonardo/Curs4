<script setup>

import { onMounted } from 'vue';

onMounted(() => {
  console.log('App mounted');
});

onUpdated(() => {
  console.log('App updated');
})

const message = "Hello from vue 3";

const clickHandler =() => {
  const message = 'Button Clicked'
  

}

</script>

<template>
  <h1>You did it!</h1>
  <button>@click"console.log('Button Clicked')">Click Me</button>
  <p>
    {{  message }}
  </p>
  <br />
  <input type = text @change="console.log('Text Changed')" 
  @input ="console.log('You have typed:' + $event.target.value)"></input>
</template>

<style scoped></style>
