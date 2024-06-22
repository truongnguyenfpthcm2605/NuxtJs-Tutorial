<template>
  <div >
    <h1 class="text-3xl font-bold font-lg">Hello, Tailwind CSS!</h1>
    <div class="mt-4">
      <p class="text-2xl">Current Number: {{ number }}</p>
      <button @click="increment" class="mt-2 p-2 bg-blue-500 text-white rounded">Increase</button>
      <button @click="decrement" class="mt-2 p-2 bg-red-500 text-white rounded">Decrease</button>

    </div>
    <div>
      <img src="@/assets/images/google.png" alt="Hình 1" class="w-[200px]">
    </div>
    <div class="mt-8">
      <Slide />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Slide from '@/components/Slide.vue'

export default Vue.extend({
  name: 'IndexPage',
  data() {
    return {
      number: 0
    }
  },
  methods: {
    increment() {
      this.number += 1
    },
    decrement() {
      this.number -= 1
    }
  }
})
</script>

<style>
/* Các kiểu tùy chỉnh nếu cần */
</style>
