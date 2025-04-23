!<template>
  <div class="w-full max-w-md px-6">
    <div class="relative h-12">
      <!-- Range track background -->
      <div
        class="absolute top-1/2 transform -translate-y-1/2 w-full h-1 bg-gray-300 rounded"
      ></div>
      <!-- Range track active (black between thumbs) -->
      <div
        id="range-progress"
        class="absolute top-1/2 transform -translate-y-1/2 h-1 bg-black rounded"
      ></div>

      <!-- Input sliders -->
      <input
        type="range"
        id="min-range"
        min="0"
        max="500"
        value="50"
        step="1"
      />
      <input
        type="range"
        id="max-range"
        min="0"
        max="500"
        value="200"
        step="1"
      />
    </div>
    <div class="flex justify-between mt-4 text-lg font-medium">
      <span id="min-val">$50</span>
      <span id="max-val">$200</span>
    </div>
  </div>
</template>

<script setup>
import {ref} from 'vue';
const minRange = document.getElementById("min-range");
const maxRange = document.getElementById("max-range");
const minVal = document.getElementById("min-val");
const maxVal = document.getElementById("max-val");
const progress = document.getElementById("range-progress");

function updateRange() {
  let min = parseInt(minRange.value);
  let max = parseInt(maxRange.value);
  const minRange = ref(0);
  // Prevent overlap
  if (max - min < 10) {
    if (event.target.id === "min-range") minRange.value = max - 10;
    else maxRange.value = min + 10;
    min = parseInt(minRange.value);
    max = parseInt(maxRange.value);
  }

  minVal.textContent = `$${min}`;
  maxVal.textContent = `$${max}`;

  const percentMin = (min / 500) * 100;
  const percentMax = (max / 500) * 100;

  progress.style.left = percentMin + "%";
  progress.style.width = percentMax - percentMin + "%";
}

minRange.addEventListener("input", updateRange);
maxRange.addEventListener("input", updateRange);

updateRange(); // initialize
</script>

<style scoped>
input[type="range"]::-webkit-slider-thumb {
  -webkit-appearance: none;
  height: 20px;
  width: 20px;
  background-color: black;
  border-radius: 50%;
  cursor: pointer;
  position: relative;
  z-index: 2;
}
input[type="range"] {
  -webkit-appearance: none;
  width: 100%;
  height: 4px;
  background: transparent;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  z-index: 1;
}
</style>