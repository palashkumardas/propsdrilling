<script setup>
import { ref,reactive } from 'vue';
import ButtonComponent from './components/ButtonComponent.vue';
import SlotComponent from './components/SlotComponent.vue';
const message=ref("Hello World");

function clickHandlerOne(){
    message.value="Click One";
}
function clickHandlerTwo(){
    message.value="Click Two";
}
</script>

<template>
  <h2 class="text-2xl my-10">Slot</h2>
    <p class="my-10">{{ message }}</p>
    <ButtonComponent :clickHandler="clickHandlerOne">
        <em class="text-white-400">Button One</em>
    </ButtonComponent>

    <ButtonComponent :clickHandler="clickHandlerTwo">
        <em class="text-white-400">Button Two</em>
    </ButtonComponent>

    <p>
        <SlotComponent>
            <template v-slot:header>This is header content</template>
            <template v-slot:default>default</template>
            <template v-slot:footer>This is footer content</template>
        </SlotComponent>
    </p>
</template>

<style scoped>

</style>
