!<template>
  <div class="">
    <div class="flex justify-between items-center">
        <div>T Shirts</div>
        <button @click="toggleContent"><img src="../../assets/images/chevron-right.svg" alt=""></button>
    </div>
    <div class="accordion-content ml-2" v-if="showContent">
        <slot></slot>
    </div>
  </div>
</template>

<script setup>
import {ref} from 'vue';
const showContent = ref(false);
function toggleContent() {
  showContent.value = !showContent.value;
}
</script>

<style>

</style>