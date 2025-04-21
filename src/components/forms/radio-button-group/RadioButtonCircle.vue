<template>
  <form class="p-4 space-y-3">
    <label class="block text-gray-700 font-medium mb-2">Select Colors</label>
  
    <div class="flex gap-4">
      <!-- Color 1 -->
      <label class="relative cursor-pointer w-10 h-10">
        <input type="radio" name="color" value="#4D4430" class="sr-only peer" checked />
        <div class="w-full h-full rounded-full bg-[#4D4430] 
                    peer-checked:ring-2 peer-checked:ring-offset-2 peer-checked:ring-[#4D4430] 
                    transition-all duration-200">
        </div>
        <!-- Tick icon overlay -->
        <div class="absolute -top-1 -right-1 bg-white rounded-full p-1 hidden peer-checked:block shadow-md">
          <svg class="h-4 w-4 text-green-600" xmlns="http://www.w3.org/2000/svg" fill="none"
            viewBox="0 0 24 24" stroke="currentColor" stroke-width="3">
            <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
          </svg>
        </div>
      </label>
  
      <!-- Color 2 -->
      <label class="relative cursor-pointer w-10 h-10">
        <input type="radio" name="color" value="#314C48" class="sr-only peer" />
        <div class="w-full h-full rounded-full bg-[#314C48] 
                    peer-checked:ring-2 peer-checked:ring-offset-2 peer-checked:ring-[#314C48] 
                    transition-all duration-200">
        </div>
        <div class="absolute -top-1 -right-1 bg-white rounded-full p-1 hidden peer-checked:block shadow-md">
          <svg class="h-4 w-4 text-green-600" xmlns="http://www.w3.org/2000/svg" fill="none"
            viewBox="0 0 24 24" stroke="currentColor" stroke-width="3">
            <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
          </svg>
        </div>
      </label>
  
      <!-- Color 3 -->
      <label class="relative cursor-pointer w-10 h-10">
        <input type="radio" name="color" value="#2D2E49" class="sr-only peer" />
        <div class="w-full h-full rounded-full bg-[#2D2E49] 
                    peer-checked:ring-2 peer-checked:ring-offset-2 peer-checked:ring-[#2D2E49] 
                    transition-all duration-200">
        </div>
        <div class="absolute -top-1 -right-1 bg-white rounded-full p-1 hidden peer-checked:block shadow-md">
          <svg class="h-4 w-4 text-green-600" xmlns="http://www.w3.org/2000/svg" fill="none"
            viewBox="0 0 24 24" stroke="currentColor" stroke-width="3">
            <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
          </svg>
        </div>
      </label>
    </div>
  </form>  
</template>

<script>
</script>

<style>

</style>