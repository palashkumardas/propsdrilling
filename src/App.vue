<script setup>
import { ref,reactive,provide } from 'vue';
import ParentComponet from './components/ParentComponet.vue';

const data=reactive({
    message:'This props drilling',
    count:0,
    increase(){
        this.count++;
    },
    decrease(){
        this.count--;
    }
})

provide('mydata',data);

</script>

<template>
  <h2 class="text-2xl my-10">Props Drilling</h2>
  <p class="text-red-500 my-10">
    {{ data.message }} | {{ data.count }}
  </p>
    <ParentComponet/>
</template>

<style scoped>

</style>
