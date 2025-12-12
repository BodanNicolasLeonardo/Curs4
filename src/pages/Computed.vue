<script setup>
import FullName from '@/components/Computed/FullName.vue';
import PriceCalculator from '@/components/Computed/PriceCalculator.vue';
import SupplierList from '@/components/Computed/SupplierList.vue';

import { ref } from "vue";
const fullName = ref(""); 

const addToList = () => {

};
</script>

<template>
 <h2 class="text-xl font-bold">Test Computed in VueJs</h2>
 <FullName @update:fullName="fN => fullName = fN" />
 <p>Your full name from parent component: {{ fullName }}</p>
 <hr class="my-4" />
 <PriceCalculator />
 <hr class="my-4" />
    <button type="button" class="bg-blue-500 text-white px-4 py-2 ml-4 rounded cursor-pointer"  @click="addToList">Add to list of Suppliers</button>
 <hr class="my-4" />
 <SupplierList />
</template>
 
<style>
 @import "bootstrap-icons";
 @import "tailwindcss";
</style>