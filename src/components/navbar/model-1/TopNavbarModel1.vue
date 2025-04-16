<template>
    <nav class="bg-white shadow-sm">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between h-16 items-center">
          <!-- Logo -->
          <NavLogo />
          
          <!-- Desktop Navigation -->
          <div class="hidden md:flex md:items-center md:space-x-6 md:ml-6">
            <NavLinks :items="navItems" mode="desktop" />
          </div>
          
          <!-- Search Bar (Desktop) -->
          <NavSearch class="hidden md:block flex-1 max-w-md mx-4" />
          
          <!-- Mobile menu button -->
          <MobileMenuButton :isOpen="mobileMenuOpen" @toggle="toggleMobileMenu" />
        </div>
      </div>
      
      <!-- Mobile Menu -->
      <MobileMenu :isOpen="mobileMenuOpen" :items="navItems" />
    </nav>
  </template>
  
  <script>
  import { ref } from 'vue';
  import NavLogo from './NavLogo.vue';
  import NavLinks from './NavLinks.vue';
  import NavSearch from './NavSearch.vue';
  import MobileMenuButton from './MobileMenuButton.vue';
  import MobileMenu from './MobileMenu.vue';
  
  export default {
    components: {
      NavLogo,
      NavLinks,
      NavSearch,
      MobileMenuButton,
      MobileMenu
    },
    setup() {
      const mobileMenuOpen = ref(false);
      const navItems = ref([
        {
          text: 'Shop',
          href: '#',
          dropdown: [
            { text: 'Men', href: '#' },
            { text: 'Women', href: '#' }
          ]
        },
        { text: 'On Sale', href: '#' },
        { text: 'New Arrivals', href: '#' },
        { text: 'Brands', href: '#' }
      ]);
  
      const toggleMobileMenu = () => {
        mobileMenuOpen.value = !mobileMenuOpen.value;
      };
  
      return {
        mobileMenuOpen,
        navItems,
        toggleMobileMenu
      };
    }
  };
  </script>