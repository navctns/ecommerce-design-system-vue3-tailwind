!<template>
  <div class="border flex border-gray-300 text-black text-sm px-6 py-2 rounded-full hover:bg-gray-100 transition">
      <button @click="decrement">-</button>
      <div class="mx-2">{{ count }}</div>
      <button @click="increment">+</button>
    </div>
</template>

<script setup>
import {ref} from 'vue';
// const props = defineProps({
//     count:{
//         type: Number,
//         default: 1
//     }
// })
const count = ref(1);
function increment(){
    count.value++;
}
function decrement(){
    count.value--;
}
</script>

<style>

</style>