<template>
    <template v-for="(item, index) in items" :key="index">
      <div v-if="item.dropdown" class="relative group">
        <a :href="item.href" class="text-gray-900 hover:text-gray-600 font-medium flex items-center">
          {{ item.text }}
          <svg class="w-4 h-4 ml-1 transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
          </svg>
        </a>
        <div class="absolute left-0 mt-2 w-48 bg-white rounded-md shadow-lg py-1 z-10 hidden group-hover:block">
          <a v-for="(subItem, subIndex) in item.dropdown" :key="subIndex" 
             :href="subItem.href" 
             class="block px-4 py-2 text-gray-700 hover:bg-gray-100">
            {{ subItem.text }}
          </a>
        </div>
      </div>
      <a v-else :href="item.href" class="text-gray-500 hover:text-gray-900 font-medium">
        {{ item.text }}
      </a>
    </template>
  </template>
  
  <script>
  export default {
    name: 'NavLinks',
    props: {
      items: {
        type: Array,
        required: true
      },
      mode: {
        type: String,
        default: 'desktop' // or 'mobile'
      }
    }
  }
  </script>