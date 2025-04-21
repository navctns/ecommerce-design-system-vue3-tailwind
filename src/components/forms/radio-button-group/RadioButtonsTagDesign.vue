!<template>
    <div class="text-center">
    <h2 class="text-gray-700 mb-4 text-lg font-medium">Choose Size</h2>
    <div class="flex gap-4 justify-center" id="radioGroup">
      <!-- Radio Option -->
      <label class="cursor-pointer">
        <input type="radio" name="size" value="Small" class="peer hidden" />
        <div class="peer-checked:bg-black peer-checked:text-white bg-gray-100 text-gray-700 px-5 py-2 rounded-full transition-colors">
          Small
        </div>
      </label>

      <label class="cursor-pointer">
        <input type="radio" name="size" value="Medium" class="peer hidden" />
        <div class="peer-checked:bg-black peer-checked:text-white bg-gray-100 text-gray-700 px-5 py-2 rounded-full transition-colors">
          Medium
        </div>
      </label>

      <label class="cursor-pointer">
        <input type="radio" name="size" value="Large" class="peer hidden" checked />
        <div class="peer-checked:bg-black peer-checked:text-white bg-gray-100 text-gray-700 px-5 py-2 rounded-full transition-colors">
          Large
        </div>
      </label>

      <label class="cursor-pointer">
        <input type="radio" name="size" value="X-Large" class="peer hidden" />
        <div class="peer-checked:bg-black peer-checked:text-white bg-gray-100 text-gray-700 px-5 py-2 rounded-full transition-colors">
          X-Large
        </div>
      </label>
    </div>
  </div>
</template>

<script>

</script>

<style>

</style>