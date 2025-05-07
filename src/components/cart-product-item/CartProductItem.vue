<template>
  <div class="p-4 bg-white rounded-2xl shadow-md flex">
    <div class="w-32">
        <img src="../../assets/images/t-shirt-img.jpg" alt="Skinny Fit Jeans" class="rounded-lg w-full mb-4" />
    </div>
    <div class="flex justify-between w-full">
        <div class="ms-3">
    <h2 class="text-lg font-semibold text-gray-900">Skinny Fit Jeans</h2>
    <div><span>Size:</span><span class="text-gray-400">Large</span></div>
    <div><span>Color:</span><span class="text-gray-400">White</span></div>
    <span class="text-xl font-bold text-gray-900 mt-3">$240</span>
    <span class="text-lg font-semibold text-gray-400 line-through mt-3">$260</span>
  </div>
    <div class="h-full flex flex-col justify-between">
        <div>del btn</div>
        <CountSetter/>
    </div>
</div>

</div>
</template>

<script setup>
import CountSetter from '../buttons/CountSetter.vue';
</script>

<style>

</style>