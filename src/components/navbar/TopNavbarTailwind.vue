<template>
  <nav class="bg-white shadow-sm py-4 px-6">
    <div
      class="max-w-7xl mx-auto flex flex-col md:flex-row items-center justify-between"
    >
      <!-- Logo -->
      <div class="flex items-center mb-4 md:mb-0">
        <a href="#" class="text-2xl font-bold text-gray-900">SHOP.CO</a>
      </div>

      <!-- Navigation Links -->
      <div class="flex items-center space-x-6 mb-4 md:mb-0">
        <!-- Shop Dropdown -->
        <div class="relative group">
          <button
            class="text-gray-900 hover:text-gray-600 font-medium flex items-center"
          >
            Shop
            <svg
              class="w-4 h-4 ml-1"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M19 9l-7 7-7-7"
              ></path>
            </svg>
          </button>
          <div
            class="absolute left-0 w-48 bg-white rounded-md shadow-lg py-1 z-10 hidden group-hover:block"
          >
            <a href="#" class="block px-4 py-2 text-gray-700 hover:bg-gray-100"
              >Men</a
            >
            <a href="#" class="block px-4 py-2 text-gray-700 hover:bg-gray-100"
              >Women</a
            >
          </div>
        </div>

        <a href="#" class="text-gray-500 hover:text-gray-900 font-medium"
          >On Sale</a
        >
        <a href="#" class="text-gray-500 hover:text-gray-900 font-medium"
          >New Arrivals</a
        >
        <a href="#" class="text-gray-500 hover:text-gray-900 font-medium"
          >Brands</a
        >
      </div>

      <!-- Search Bar -->
      <div class="relative w-full md:w-auto">
        <input
          type="text"
          placeholder="Search for products..."
          class="w-full md:w-64 px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-gray-500 focus:border-transparent"
        />
        <svg
          class="absolute right-3 top-2.5 h-5 w-5 text-gray-400"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
          ></path>
        </svg>
      </div>
    </div>
  </nav>
</template>
