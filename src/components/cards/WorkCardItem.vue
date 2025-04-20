<template>
  <div class="work-card flex-shrink-0 w-80">
    <div 
      class="work-card-inner bg-white rounded-xl overflow-hidden shadow-md hover-scale"
      @mouseenter="isHovered = true"
      @mouseleave="isHovered = false"
      :style="hoverStyle"
    >
      <img 
        :src="work.imageUrl" 
        :alt="work.title" 
        class="w-full h-56 object-cover"
        loading="lazy"
      >
      <div class="p-6">
        <h3 class="font-bold text-xl mb-2">{{ work.title }}</h3>
        <p class="text-gray-600 mb-4">{{ work.description }}</p>
        <div class="flex flex-wrap gap-2">
          <span 
            v-for="(tag, index) in work.tags" 
            :key="tag"
            class="inline-block px-3 py-1 rounded-full text-sm"
            :class="getTagClass(index)"
          >
            {{ tag }}
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent, computed, ref } from 'vue'

export default defineComponent({
  name: 'WorkCard',
  props: {
    work: {
      type: Object,
      required: true,
      validator: (value) => {
        return [
          'title',
          'description',
          'imageUrl',
          'tags'
        ].every(prop => prop in value)
      }
    }
  },
  setup(props) {
    const isHovered = ref(false)
    const tagClasses = [
      'bg-blue-100 text-blue-600',
      'bg-green-100 text-green-600',
      'bg-purple-100 text-purple-600',
      'bg-yellow-100 text-yellow-600',
      'bg-pink-100 text-pink-600',
      'bg-indigo-100 text-indigo-600'
    ]

    const hoverStyle = computed(() => ({
      transform: isHovered.value ? 'rotateY(10deg)' : 'rotateY(0)',
      transition: 'transform 0.6s'
    }))

    const getTagClass = (index) => {
      return tagClasses[index % tagClasses.length]
    }

    return {
      isHovered,
      hoverStyle,
      getTagClass
    }
  }
})
</script>

<style scoped>
.hover-scale {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.hover-scale:hover {
  transform: scale(1.03);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
}

.work-card {
  perspective: 1000px;
}
</style>