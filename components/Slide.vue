<template>
  <div class="flex flex-col items-center">
    <div class="relative w-64 h-64">
      <img :src="images[currentIndex]" alt="Slide Image" class="w-full h-full object-cover">
      <button @click="prevSlide" class="absolute left-0 top-1/2 transform -translate-y-1/2 bg-white text-black p-2 rounded-full">Previous</button>
      <button @click="nextSlide" class="absolute right-0 top-1/2 transform -translate-y-1/2 bg-white text-black p-2 rounded-full">Next</button>
    </div>
    <div class="flex mt-4 space-x-2">
      <span v-for="(image, index) in images" :key="index" class="w-2 h-2 rounded-full" :class="{'bg-blue-500': currentIndex === index, 'bg-gray-300': currentIndex !== index}"></span>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data() {
    return {
      currentIndex: 0,
      images: [
        require('@/assets/images/google.png'),
        require('@/assets/images/hinh1.jpg'),
        require('@/assets/images/hinh2.jpg')
      ]
    }
  },
  methods: {
    nextSlide() {
      this.currentIndex = (this.currentIndex + 1) % this.images.length
    },
    prevSlide() {
      this.currentIndex = (this.currentIndex - 1 + this.images.length) % this.images.length
    }
  }
})
</script>

