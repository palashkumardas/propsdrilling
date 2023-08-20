<script setup>
import { ref, reactive } from 'vue';
defineProps(['clickHandler']);
</script>

<template>
    <button @click="clickHandler" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded m-1">
    <slot></slot>

    </button>
 
</template>

<style scoped>

</style>
