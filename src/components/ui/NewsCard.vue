<template>
  <div class="bg-white rounded-lg shadow-md overflow-hidden transition-transform transform hover:scale-105 group ">
    <img :src="image" :alt="title" class="w-full h-48 object-cover">
    
    <div class="p-4">
      <div class=" flex items-center justify-between text-gray-500 text-sm mb-2">
        <span class="font-bold  bg-azul text-white px-2 py-1 rounded-2xl">{{ tag }}</span>
        <span>{{ date }}</span>
      </div>

      <h3 class="text-xl font-semibold text-gray-800 mb-2 transition-colors duration-200 group-hover:text-azul">{{ title }}</h3>
      <p class="text-gray-600 mb-4">{{ description }}</p>

      <a :href="link" class="bg-white text-azul font-semibold flex items-center w-fit border-1 border-gray-300 rounded-lg px-4 py-2 transition-colors duration-200 hover:bg-azul hover:text-white">
        Leia Mais 
        <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-1 transition-transform transform group-hover:translate-x-1" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round" d="M9 5l7 7-7 7" />
        </svg>
      </a>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'NewsCard',
  props: {
    image: {
      type: String,
      required: true,
    },
    tag: {
      type: String,
      required: true,
    },
    date: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    link: {
      type: String,
      required: true,
    },
  },
});
</script>