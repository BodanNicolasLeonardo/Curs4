<script setup>
import GreenFlower from './Flowers/GreenFlower.vue'

</script>

<template>
<h3>Growth</h3>
<hr></hr>
<div class ="2-5/6 mx-auto"></div>
<div class ="flex-justify-center">
    <GreenFlower v-for="flower  in [0, 1, 2]" :key="flower" />
</div>
<h3>Earth</h3>
</template>

<style scoped>
@import "bootstrap-icons";
@import "tailwindcss";

</style>