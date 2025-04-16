<template>
    <div class="md:hidden flex items-center">
      <button 
        @click="$emit('toggle')"
        type="button" 
        class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none"
      >
        <svg v-if="!isOpen" class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
        </svg>
        <svg v-else class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
        </svg>
      </button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'MobileMenuButton',
    props: {
      isOpen: {
        type: Boolean,
        required: true
      }
    },
    emits: ['toggle']
  }
  </script>