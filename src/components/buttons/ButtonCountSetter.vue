!<template>
  <div class="border fl-x border-gray-300 text-black text-sm px-6 py-2 rounded-full hover:bg-gray-100 transition">
      <button>-</button>
      <div>{{ count }}</div>
      <button>+</button>
    </div>
</template>

<script setup>
defineProps({
    count:{
        type: Number
    }
})
</script>

<style>

</style>