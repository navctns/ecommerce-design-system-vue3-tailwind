!<template>
          <div class="flex items-center justify-between">
            <!-- Previous Button -->
            <button class="px-4 py-2 border rounded-l-lg border-gray-300 bg-white text-gray-700 hover:bg-gray-50 disabled:opacity-50 disabled:cursor-not-allowed" disabled>
                Previous
            </button>
            
            <!-- Page Numbers -->
            <div class="flex">
                <button class="px-4 py-2 border-t border-b border-l border-gray-300 bg-blue-500 text-white">
                    1
                </button>
                <button class="px-4 py-2 border-t border-b border-l border-gray-300 bg-white text-gray-700 hover:bg-gray-50">
                    2
                </button>
                <button class="px-4 py-2 border-t border-b border-l border-gray-300 bg-white text-gray-700 hover:bg-gray-50">
                    3
                </button>
                <span class="px-4 py-2 border-t border-b border-l border-gray-300 bg-white text-gray-700">
                    ...
                </span>
                <button class="px-4 py-2 border-t border-b border-l border-gray-300 bg-white text-gray-700 hover:bg-gray-50">
                    8
                </button>
            </div>
            
            <!-- Next Button -->
            <button class="px-4 py-2 border rounded-r-lg border-gray-300 bg-white text-gray-700 hover:bg-gray-50">
                Next
            </button>
        </div>
</template>

<style>

</style>