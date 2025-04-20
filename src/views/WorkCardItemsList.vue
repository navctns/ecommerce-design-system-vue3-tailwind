<template>
  <div class="tab-slider flex overflow-x-auto pb-8 gap-6">
    <WorkCard 
      v-for="work in works" 
      :key="work.title"
      :work="work" 
    />
  </div>
</template>

<script>
import { defineComponent, ref } from 'vue'
import WorkCard from '@/components/WorkCard.vue'

export default defineComponent({
  name: 'WorkGallery',
  components: {
    WorkCard
  },
  setup() {
    const works = ref([
      {
        title: "EcoLife Brand Identity",
        description: "Complete branding package for sustainable lifestyle brand",
        imageUrl: "https://images.unsplash.com/photo-1635070041078-e363dbe005cb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80",
        tags: ["Logo Design", "Brand Guidelines"]
      },
      {
        title: "UrbanBrew Coffee",
        description: "Brand identity for specialty coffee shop chain",
        imageUrl: "https://images.unsplash.com/photo-1605000797499-95a51c5269ae?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1471&q=80",
        tags: ["Typography", "Color Palette"]
      }
    ])

    return {
      works
    }
  }
})
</script>

<style scoped>
.tab-slider {
  scrollbar-width: none; /* Firefox */
  -ms-overflow-style: none; /* IE/Edge */
}

.tab-slider::-webkit-scrollbar {
  display: none; /* Chrome/Safari */
}
</style>