<script setup>
import { inject } from 'vue';

const data=inject('mydata');

</script>

<template>
    <h2 class="text-2xl my-10 text-orange-500">Child Component</h2>
    <button @click="data.increase" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded m-1 ">+</button>
    <button @click="data.decrease" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded m-1">-</button>

</template>

<style scoped>

</style>