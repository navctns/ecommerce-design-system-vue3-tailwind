!<template>
  <div class="border flex items-center border-gray-300 text-black text-sm px-6 py-2 rounded-full hover:bg-gray-100 transition">
      <button @click="decrement" class="text-xl font-semibold">-</button>
      <div class="mx-5">{{ count }}</div>
      <button @click="increment" class="text-xl font-semibold">+</button>
    </div>
</template>

<script setup>
import {ref} from 'vue';
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