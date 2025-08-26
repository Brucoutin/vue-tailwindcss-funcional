<template>
<div class="flex justify-center w-full">
  <div
    class="bg-blue-600 text-white rounded-lg shadow-md relative overflow-hidden flex items-center justify-center"
    style="width: 100%; max-width: 1500px; height: 500px;"
  >
    <button
      @click="prevImage"
      class="absolute left-4 bg-white text-blue-600 rounded-full w-8 h-8 flex items-center justify-center hover:bg-blue-100 z-10"
      aria-label="Anterior"
    >
      ‹
    </button>

    <img
      :src="images[currentIndex]"
      alt="Banner"
      class="w-full h-full object-contain"
    />

    <button
      @click="nextImage"
      class="absolute right-4 bg-white text-blue-600 rounded-full w-8 h-8 flex items-center justify-center hover:bg-blue-100 z-10"
      aria-label="Próximo"
    >
      ›
    </button>
  </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

// Importa todas as imagens da pasta assets/images
const images = Object.values(
  import.meta.glob('@/assets/images/*.{png,jpg,jpeg,gif,webp}', { eager: true, as: 'url' })
)

const currentIndex = ref(0)

function nextImage() {
  currentIndex.value = (currentIndex.value + 1) % images.length
}

function prevImage() {
  currentIndex.value = (currentIndex.value - 1 + images.length) % images.length
}
</script>
