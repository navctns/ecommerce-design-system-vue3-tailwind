<template>
  <div class="w-full max-w-md px-6">
    <div class="relative h-12">
      <!-- Track background -->
      <div
        class="absolute top-1/2 transform -translate-y-1/2 w-full h-1 bg-gray-300 rounded"
      ></div>
      <!-- Track progress -->
      <div
        class="absolute top-1/2 transform -translate-y-1/2 h-1 bg-black rounded"
        :style="progressStyle"
      ></div>

      <!-- Range inputs -->
      <input
        type="range"
        min="0"
        max="500"
        step="1"
        v-model.number="min"
        @input="handleInput('min')"
      />
      <input
        type="range"
        min="0"
        max="500"
        step="1"
        v-model.number="max"
        @input="handleInput('max')"
      />
    </div>
    <div class="flex justify-between mt-4 text-lg font-medium">
      <span>\${{ min }}</span>
      <span>\${{ max }}</span>
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from "vue";

const min = ref(50);
const max = ref(200);
const minGap = 10;
const maxRange = 500;

const handleInput = (type) => {
  if (max.value - min.value < minGap) {
    if (type === "min") min.value = max.value - minGap;
    else max.value = min.value + minGap;
  }
};

const progressStyle = computed(() => {
  const left = (min.value / maxRange) * 100;
  const right = (max.value / maxRange) * 100;
  return {
    left: `${left}%`,
    width: `${right - left}%`,
  };
});
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