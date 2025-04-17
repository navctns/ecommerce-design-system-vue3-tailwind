<template>
  <a href="" class="">
    <div>
        <div class="bg-gray-200 p-2 rounded-lg">
            <img src="../../assets/images/t-shirt-img.jpg" class="img-fluid" alt="">
        </div>
        <div>{{ title }}</div>
    </div>
  </a>
</template>

<script setup>
const props = defineProps({
  title: {
    type: String,
    default:'Product title'
  }
});
console.log(props);
</script>

<style>

</style>