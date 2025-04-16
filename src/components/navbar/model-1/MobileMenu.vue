<template>
    <div v-if="isOpen" class="md:hidden border-t border-gray-200">
      <div class="px-2 pt-2 pb-3 space-y-1">
        <template v-for="(item, index) in items" :key="index">
          <div v-if="item.dropdown" class="relative">
            <button 
              @click="toggleDropdown(index)"
              class="w-full flex justify-between items-center px-3 py-2 text-base font-medium text-gray-900 hover:text-gray-600"
            >
              <span>{{ item.text }}</span>
              <svg 
                class="w-4 h-4 ml-1 transition-transform" 
                :class="{ 'rotate-180': openDropdown === index }"
                fill="none" 
                stroke="currentColor" 
                viewBox="0 0 24 24"
              >
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
              </svg>
            </button>
            <div v-if="openDropdown === index" class="pl-4">
              <a 
                v-for="(subItem, subIndex) in item.dropdown" 
                :key="subIndex" 
                :href="subItem.href" 
                class="block px-3 py-2 text-base font-medium text-gray-500 hover:text-gray-900"
              >
                {{ subItem.text }}
              </a>
            </div>
          </div>
          <a 
            v-else 
            :href="item.href" 
            class="block px-3 py-2 text-base font-medium text-gray-500 hover:text-gray-900"
          >
            {{ item.text }}
          </a>
        </template>
      </div>
      
      <!-- Mobile Search -->
      <div class="px-4 py-3 border-t border-gray-200">
        <NavSearch />
      </div>
    </div>
  </template>
  
  <script>
  import NavSearch from './NavSearch.vue';
  
  export default {
    name: 'MobileMenu',
    components: {
      NavSearch
    },
    props: {
      isOpen: {
        type: Boolean,
        required: true
      },
      items: {
        type: Array,
        required: true
      }
    },
    data() {
      return {
        openDropdown: null
      };
    },
    methods: {
      toggleDropdown(index) {
        this.openDropdown = this.openDropdown === index ? null : index;
      }
    },
    watch: {
      isOpen(newVal) {
        if (!newVal) {
          this.openDropdown = null;
        }
      }
    }
  }
  </script>