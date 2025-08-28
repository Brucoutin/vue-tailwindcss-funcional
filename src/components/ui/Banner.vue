<template>
  <div class="flex justify-center w-full mt-5">
    <div
      class="
        bg-white rounded-lg shadow-md relative overflow-hidden flex items-center justify-center 
        w-full max-w-[1500px] 
        h-[250px] sm:h-[300px] md:h-[400px] lg:h-[500px]
      "
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
        class="w-full h-full object-cover"
      />
      <!-- class="w-full h-full object-contain sm:object-cover"-->
      
      <button
        @click="nextImage"
        class="absolute right-4 bg-white text-blue-600 rounded-full w-8 h-8 flex items-center justify-center hover:bg-blue-100 z-10"
        aria-label="Próximo"
      >
        ›
      </button>
      <div class="absolute bottom-4 flex space-x-2 z-10">
        <button
          v-for="(image, index) in images"
          :key="index"
          @click="currentIndex = index"
          class="w-3 h-3 rounded-full transition-colors duration-300"
          :class="{ 'bg-blue-600': currentIndex === index, 'bg-gray-300': currentIndex !== index }"
          :aria-label="'Ver imagem ' + (index + 1)"
        ></button>
      </div>
    </div>
  </div>

</template>


<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'

const images = Object.values(
  import.meta.glob('@/assets/images/*.{png,jpg,jpeg,gif,webp}', { eager: true, as: 'url' })
)

const currentIndex = ref(0)
let intervalId: number | undefined = undefined

function nextImage() {
  currentIndex.value = (currentIndex.value + 1) % images.length
}

function prevImage() {
  currentIndex.value = (currentIndex.value - 1 + images.length) % images.length
}

function startAutoSlide() {
  intervalId = setInterval(() => {
    nextImage()
  }, 3000)
}

function stopAutoSlide() {
  if (intervalId !== undefined) {
    clearInterval(intervalId)
  }
}

onMounted(() => {
  startAutoSlide()
})

onUnmounted(() => {
  stopAutoSlide()
})
</script>